# Ejemplos - Módulo 4

## Ejemplo de workflow básico

```yaml
name: Hello Workflow

on:
  workflow_dispatch:

jobs:
  hello:
    runs-on: ubuntu-latest
    steps:
      - name: Saludar
        run: echo "Hola desde GitHub Actions"
