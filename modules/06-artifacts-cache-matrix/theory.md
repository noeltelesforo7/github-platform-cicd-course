# Teoría: Artefactos, cache y matrix

## ¿Qué es cache en GitHub Actions?

Cache permite reutilizar archivos entre ejecuciones de un workflow para evitar trabajo repetido. Se usa mucho para dependencias, como las de Node.js.

## ¿Por qué usar cache?

Cache ayuda a:

- reducir tiempos de ejecución
- evitar reinstalar dependencias desde cero en cada run
- mejorar eficiencia del pipeline

## Ejemplo común de cache en Node.js

Un caso frecuente es cachear dependencias asociadas a `npm`, usando `actions/setup-node` con soporte de cache o usando `actions/cache`.

## ¿Qué es un artefacto?

Un artefacto es un archivo o conjunto de archivos que un workflow guarda después de ejecutarse.

## ¿Para qué sirven los artefactos?

Los artefactos ayudan a:

- conservar resultados de build
- compartir salidas entre jobs
- descargar evidencias de ejecución
- guardar reportes o paquetes generados

## Ejemplos de artefactos

- un archivo compilado
- un reporte de pruebas
- un paquete `.zip`
- un archivo de salida generado por build

## ¿Qué es matrix strategy?

Matrix strategy permite ejecutar un mismo job en múltiples combinaciones de variables.

## ¿Para qué sirve matrix?

Matrix se usa para:

- probar varias versiones de Node.js
- validar múltiples sistemas operativos
- ampliar cobertura del pipeline sin duplicar YAML

## Ejemplo conceptual

En lugar de definir varios jobs manuales, matrix permite decir:
- ejecuta este job con Node 18
- ejecuta este job con Node 20

## Buenas prácticas iniciales

- usar cache cuando el proyecto tenga instalación repetitiva
- guardar solo artefactos útiles
- no abusar de artefactos pesados sin necesidad
- usar matrix para ampliar validación de forma ordenada
- mantener nombres claros en los jobs y artefactos

## Errores comunes

- pensar que cache y artefactos son lo mismo
- guardar demasiados archivos innecesarios
- crear matrices complejas demasiado pronto
- no revisar si el cache realmente aporta valor
