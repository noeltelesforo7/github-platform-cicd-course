# Teoría: Ramas y Pull Requests

## ¿Qué es una rama?

Una rama es una línea de trabajo independiente dentro de un repositorio. Permite realizar cambios sin afectar directamente la rama principal.

## ¿Por qué usar ramas?

Las ramas permiten:

- trabajar cambios de forma aislada
- desarrollar nuevas funcionalidades
- corregir errores sin alterar trabajo estable
- colaborar con otras personas de manera ordenada

## Rama principal

En muchos repositorios la rama principal se llama `main`. Normalmente representa la versión más estable o integrada del proyecto.

## Buenas prácticas al crear ramas

- usar una rama por cambio o tarea
- elegir nombres descriptivos
- evitar trabajar directamente en `main`
- mantener ramas pequeñas y enfocadas

## Ejemplos de nombres de ramas

- `feature/login-page`
- `fix/readme-typo`
- `docs/module-2-content`

## ¿Qué es un Pull Request?

Un Pull Request, o PR, es una solicitud para integrar cambios de una rama hacia otra. En GitHub también sirve para revisar, discutir y aprobar esos cambios antes del merge.

## ¿Qué contiene un Pull Request?

Un pull request suele incluir:

- título
- descripción
- rama de origen
- rama de destino
- lista de commits
- archivos modificados
- conversación o comentarios
- estado de checks o validaciones

## ¿Por qué usar Pull Requests?

Los pull requests ayudan a:

- revisar cambios antes de integrarlos
- discutir decisiones técnicas
- detectar errores
- dejar trazabilidad
- mantener calidad en el repositorio

## ¿Qué es merge?

Merge es la acción de integrar los cambios de una rama en otra.

## Formas comunes de merge en GitHub

- Create a merge commit
- Squash and merge
- Rebase and merge

## Buenas prácticas con Pull Requests

- crear PRs pequeños y fáciles de revisar
- escribir títulos claros
- describir qué cambió y por qué
- vincular PRs con tareas o issues cuando aplique
- revisar antes de hacer merge

## Errores comunes

- crear ramas con cambios no relacionados
- abrir PRs demasiado grandes
- no describir el propósito del cambio
- hacer merge sin revisar el contenido
