# Teoría: Deployments y environments

## ¿Qué es CD?

CD puede referirse a Continuous Delivery o Continuous Deployment, según el nivel de automatización del despliegue.

### Continuous Delivery
Los cambios quedan listos para desplegar, pero normalmente requieren una aprobación o acción manual antes de llegar a producción.

### Continuous Deployment
Los cambios se despliegan automáticamente sin intervención manual una vez que superan las validaciones necesarias.

## ¿Qué es un deployment?

Un deployment es la acción de publicar o entregar una versión de la aplicación en un entorno determinado.

## Ejemplos de entornos

- `development`
- `staging`
- `production`

## ¿Qué es un environment en GitHub?

Un environment en GitHub es una configuración que permite asociar despliegues a un entorno lógico y aplicar controles como:

- secrets específicos del entorno
- reglas de protección
- aprobaciones manuales
- restricciones

## ¿Por qué separar staging y production?

Separar entornos ayuda a:

- validar antes de llegar a producción
- reducir riesgo
- probar configuraciones
- controlar mejor la entrega

## Flujo común de CD

Un flujo básico puede verse así:

1. se hace merge a `main`
2. corre CI
3. si CI pasa, se habilita el despliegue
4. se despliega a `staging`
5. se valida el resultado
6. se aprueba despliegue a `production`

## ¿Qué papel juega GitHub Actions?

GitHub Actions permite automatizar el flujo de despliegue con workflows que se disparan por eventos como:

- `push`
- `workflow_dispatch`
- `release`

## Buenas prácticas iniciales

- separar CI y CD en workflows distintos
- proteger producción con approvals
- usar environments para distinguir entornos
- no mezclar despliegues de staging y producción sin control
- mantener logs claros del proceso de despliegue

## Errores comunes

- desplegar directamente a producción sin validaciones
- no usar environments
- usar los mismos secretos para todos los entornos
- acoplar demasiado CI y CD en un solo workflow
