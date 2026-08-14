# Ejemplos - Módulo 6

## Ejemplo de workflow con cache, artefactos y matrix

```yaml
name: Node.js CI Advanced

on:
  push:
  pull_request:

jobs:
  ci:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [18, 20]

    defaults:
      run:
        working-directory: shared/sample-app-node

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: ${{ matrix.node-version }}
          cache: npm
          cache-dependency-path: shared/sample-app-node/package-lock.json

      - name: Install dependencies
        run: npm ci

      - name: Run lint
        run: npm run lint

      - name: Run tests
        run: npm test

      - name: Run build
        run: npm run build

      - name: Create build output
        run: echo "Build completado con Node.js ${{ matrix.node-version }}" > build-output.txt

      - name: Upload artifact
        uses: actions/upload-artifact@v4
        with:
          name: build-output-node-${{ matrix.node-version }}
          path: shared/sample-app-node/build-output.txt
