# Herramientas y Setup QA – Proyecto Primarket

## Herramientas principales utilizadas

| Herramienta | Propósito                      |
| ----------- | ------------------------------ |
| Cypress     | Automatización de pruebas UI   |
| Postman     | Testing de APIs REST           |
| JMeter      | Pruebas de carga y rendimiento |
| Clickup     | Gestión de tareas y bugs       |
| GitHub      | Versionado y documentación     |

## Configuración de entorno local QA

* Requisitos: Node.js, npm, Cypress instalado global o en proyecto
* Repositorio QA: `https://github.com/usuario/primarket-qa` ???*
* Configuraciones para `cypress.config.js` documentadas en `docs/cypress_tests.md`

## Accesos y entornos

| Ambiente | URL base (a definir)                                   | Notas                  |
| -------- | ------------------------------------------------------ | ---------------------- |
| DEV      | [https://dev.primarket.com](https://dev.primarket.com) | Entorno de desarrollo  |
| QA       | [https://qa.primarket.com](https://qa.primarket.com)   | Principal para testing |
| PROD     | [https://primarket.com](https://primarket.com)         | No usado por QA        |

> Todos los testers deben tener configurado su entorno con acceso a QA, conexión a red y permisos de ejecución.
