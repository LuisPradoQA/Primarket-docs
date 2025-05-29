# Cypress – Automatización UI

## Setup básico del entorno Cypress

```bash
npm install cypress --save-dev
npx cypress open
```

## Estructura recomendada de carpetas

```
cypress/
├── e2e/
│   ├── login.cy.js
│   └── favoritos.cy.js
├── fixtures/
├── support/
│   └── commands.js
```

## Tests sugeridos para automatizar

| Nombre               | Prioridad | Estado |
| -------------------- | --------- | ------ |
| Login válido         | Alta      | ✅      |
| Agregar a favoritos  | Media     | ⏳      |
| Recuperar contraseña | Alta      | ⏳      |

## Configuración (`cypress.config.js`)

```js
const { defineConfig } = require('cypress')
module.exports = defineConfig({
  e2e: {
    baseUrl: 'https://qa.primarket.com',
    supportFile: 'cypress/support/commands.js',
  }
})
```

<!--- > Los resultados de ejecución pueden integrarse en el reporte de evidencias por sprint. --->