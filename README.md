# demo-github-actions
# Demo: GitHub Actions y Buenas Prácticas

Este repositorio muestra cómo usar GitHub Actions junto con buenas prácticas como el uso de ramas, pull requests y protección de la rama principal.

---

## ✅ Pasos Realizados

### 1. Crear el Repositorio
- Se creó este repositorio en GitHub.
- Se agregó un archivo `README.md` como contenido inicial.

### 2. Crear una nueva rama
- Se creó una rama llamada `rama-actions` para no trabajar directamente en `main`.

### 3. Crear el archivo de GitHub Actions
- En la ruta `.github/workflows/`, se creó un archivo llamado `saludo.yml`.

```yaml
name: Demo CI

on:
  pull_request:
    branches: [ main ]

jobs:
  saludo:
    runs-on: ubuntu-latest
    steps:
      - name: Mostrar saludo
        run: echo "¡Hola! Esto es una ejecución automática de GitHub Actions desde un pull request."

