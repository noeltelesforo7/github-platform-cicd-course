# Ejemplos - Módulo 2

## Ejemplo de flujo con ramas y Pull Requests

```bash
git checkout -b docs/module-2-update
echo "Nuevo contenido para el módulo 2" >> modules/02-branches-and-pull-requests/README.md
git add modules/02-branches-and-pull-requests/README.md
git commit -m "docs: update module 2 overview"
git push origin docs/module-2-update
