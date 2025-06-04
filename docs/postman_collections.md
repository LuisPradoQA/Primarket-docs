# Postman – Validación de APIs REST

## Setup básico

1. Descargar Postman: [https://www.postman.com/downloads/](https://www.postman.com/downloads/)
2. Importar colección `Primarket QA API Collection` desde archivo `.json` o enlace compartido por el equipo Dev
3. Definir variables de entorno:

   * `base_url = https://qa.primarket.com/api` (a definir)
   * `token` (opcional)

## Estructura sugerida de colección

```
Primarket QA Collection
├── Auth
│   ├── Login (POST)
│   └── Registro (POST)
├── Productos
│   ├── Publicar (POST)
│   ├── Obtener todos (GET)
│   └── Editar producto (PUT)
├── Usuarios
│   ├── Datos perfil (GET)
│   └── Favoritos (GET/POST)
```

## Buenas prácticas

* Incluir tests automáticos en cada request (`pm.expect(...)`)
* Usar variables para tokens y parámetros dinámicos
* Organizar en carpetas por módulo

## Evidencias sugeridas

* Capturas de respuesta JSON
* Exportación de tests pasados como PDF
* Reporte generado con [newman](https://github.com/postmanlabs/newman) (CLI)
asdasdasd
