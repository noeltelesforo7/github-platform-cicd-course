# Ejemplos - Módulo 1

## Ejemplo de flujo básico con Git

```bash
git clone https://github.com/noeltelesforo7/github-platform-cicd-course
cd github-platform-ci/cd-course
git checkout -b feature/primer-modulo
echo "Aprendiendo GitHub" >> README.md
git add README.md
git commit -m "docs: agregar descripción inicial al README"
git push origin feature/primer-modulo
