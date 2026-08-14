# Ejemplos - Módulo 7

## Ejemplo de despliegue a staging

```yaml
name: Deploy to Staging

on:
  push:
    branches:
      - main

jobs:
  deploy-staging:
    runs-on: ubuntu-latest
    environment: staging

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Simulate staging deploy
        run: echo "Desplegando a staging..."
