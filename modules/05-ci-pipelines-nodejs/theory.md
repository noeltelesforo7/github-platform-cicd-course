# Teoría: CI pipelines con Node.js

## ¿Qué es CI?

CI significa Continuous Integration, o Integración Continua. Es la práctica de integrar cambios frecuentemente en una rama compartida y validarlos automáticamente.

## ¿Por qué es importante?

CI ayuda a:

- detectar errores temprano
- validar cambios antes del merge
- mantener estabilidad en el repositorio
- automatizar tareas repetitivas
- dar confianza al equipo al integrar cambios

## ¿Qué suele hacer un pipeline de CI?

Un pipeline de CI normalmente ejecuta tareas como:

- instalar dependencias
- validar formato o estilo
- ejecutar lint
- correr pruebas
- construir la aplicación

## ¿Por qué usar Node.js para practicar CI?

Node.js permite crear ejemplos simples y rápidos de validar. Con un `package.json` se pueden definir scripts estándar para automatizar tareas como `lint`, `test` y `build`.

## Scripts comunes en un proyecto Node.js

En un proyecto Node.js es común tener scripts como:

- `npm run lint`
- `npm test`
- `npm run build`

## Eventos comunes para CI en GitHub Actions

Los eventos más usados para CI son:

- `push`
- `pull_request`

### `push`
Permite validar cambios cuando se suben commits a una rama.

### `pull_request`
Permite validar cambios antes de hacer merge hacia una rama como `main`.

## Flujo típico de CI con Pull Requests

1. se crea una rama
2. se hacen cambios
3. se abre un pull request
4. GitHub Actions ejecuta el pipeline
5. se revisan resultados
6. si todo está bien, se hace merge

## Buenas prácticas iniciales

- ejecutar CI al menos en `pull_request`
- usar nombres claros en jobs y steps
- mantener el pipeline simple al inicio
- separar instalación, validación y build
- revisar logs cuando algo falla

## Errores comunes

- no definir scripts en `package.json`
- mezclar demasiadas tareas en un solo step
- correr CI solo después del merge
- no revisar la causa real de un fallo en logs
