# Teoría: GitHub Actions desde cero

## ¿Qué es GitHub Actions?

GitHub Actions es la plataforma de automatización de GitHub. Permite ejecutar tareas automáticamente dentro de un repositorio cuando ocurre un evento determinado.

## ¿Para qué sirve?

GitHub Actions puede usarse para:

- validar cambios
- ejecutar pruebas
- construir artefactos
- desplegar aplicaciones
- automatizar tareas repetitivas
- integrar flujos de CI/CD

## ¿Qué es un workflow?

Un workflow es un archivo YAML que define una automatización. Normalmente se guarda dentro de:

`/.github/workflows/`

## ¿Qué puede disparar un workflow?

Un workflow puede ejecutarse cuando ocurre un evento, por ejemplo:

- `push`
- `pull_request`
- `workflow_dispatch`

## ¿Qué es un job?

Un job es un conjunto de pasos que se ejecutan en un mismo runner.

## ¿Qué es un step?

Un step es una acción individual dentro de un job. Puede ser:

- ejecutar un comando
- usar una action existente
- preparar dependencias
- validar archivos

## ¿Qué es un runner?

Un runner es la máquina donde se ejecuta el workflow. GitHub ofrece runners administrados como:

- `ubuntu-latest`
- `windows-latest`
- `macos-latest`

## Estructura básica de un workflow

Un workflow suele incluir:

- nombre
- evento que lo dispara
- jobs
- steps

## Ejemplo mínimo

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
