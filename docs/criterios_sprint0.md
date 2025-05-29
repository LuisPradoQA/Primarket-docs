# 📋 Criterios de Aceptación – Sprint 0

## Introducción

Este documento reúne los **criterios de aceptación** y la **Definition of Done (DoD)** para las historias de usuario incluidas en el Sprint 0 del proyecto **Primarket**.

Los criterios de aceptación están redactados de forma clara, objetiva y verificable. Su propósito es alinear las expectativas del equipo de desarrollo, producto y QA para asegurar que cada historia cumpla con las condiciones necesarias para ser considerada “hecha”.

Cada entrada incluye:

- 🧾 La historia de usuario correspondiente.

- ✅ Criterios de aceptación (funcionales y técnicos).

- 🧪 Definition of Done (DoD): checklist mínimo de calidad y entregables.
---

Este documento sirve como **base para el diseño de casos de prueba**, revisión de historias, seguimiento de avances y validación previa al cierre de cada tarea.

---


### 🧾 HU-001 – Agregar productos a favoritos

**Historia de Usuario:**  
Como usuario común, quiero poder agregar productos a una lista de favoritos para guardarlos y comprarlos más tarde.

---

#### ✅ Criterios de Aceptación

- [ ] El usuario puede agregar productos a favoritos haciendo clic en el ícono de corazón en la tarjeta del producto.
- [ ] El usuario puede quitar productos de favoritos haciendo clic nuevamente en el corazón.
- [ ] Los productos favoritos son accesibles desde el perfil del usuario.
- [ ] El menú desplegable en el ícono de corazón del navbar muestra los últimos 5 productos favoritos agregados.
- [ ] Al hacer clic en “Ver más”, el usuario es dirigido a la página completa de favoritos.
- [ ] Los productos agregados se guardan en la base de datos del usuario para mantenerlos disponibles en diferentes sesiones o dispositivos.

---

#### 🧪 Definition of Done (DoD)

- [ ] Todos los criterios de aceptación fueron validados por QA y PO.
- [ ] Se ejecutaron pruebas funcionales en desktop y mobile.
- [ ] Se validó la persistencia de datos en base de datos.
- [ ] Se incluyeron pruebas de regresión para agregar/quitar favoritos.
- [ ] No existen errores abiertos en estado “Alta” o superior relacionados a favoritos.
- [ ] La funcionalidad fue desplegada en el entorno QA y validada.

---

### 🧾 HU-002 – Panel de Administración Interno

**Historia de Usuario:**
Como administrador de la plataforma, quiero acceder a un panel de administración interno donde pueda gestionar usuarios, publicaciones y reportes, visualizar estadísticas de actividad y hacer seguimiento de cuentas sospechosas, para mantener un entorno seguro y bien controlado.

---

### ✅ Criterios de Aceptación
- [ ] El administrador debe poder iniciar sesión en el panel con credenciales exclusivas.
- [ ] El dashboard debe permitir visualizar y gestionar usuarios (banear, verificar, editar).
- [ ] El administrador debe poder acceder a todas las publicaciones y modelarlas (editar, eliminar, marcar como sospechosas).
- [ ] Las denuncias deben estar accesibles para revisión con estado actualizado (pendiente, resuelto, en revisión).
- [ ] Se deben mostrar estadísticas como: cantidad de usuarios activos, productos publicados, denuncias recibidas, compras realizadas, etc.
- [ ] El sistema debe mostrar alertas automáticas sobre actividad inusual (usuarios con muchas denuncias, publicaciones repetidas sospechosas).
- [ ] El administrador debe poder acceder a un historial de acciones tomadas sobre cuentas o publicaciones.

---

### 🧪 Definition of Done (DoD)
- [ ] Historia validada por el equipo de QA y aprobada por el PO.
- [ ] El administrador puede iniciar sesión en el panel utilizando credenciales exclusivas de administrador.
- [ ] El sistema valida correctamente las credenciales y maneja errores de autenticación (credenciales incorrectas, cuenta bloqueada, etc.).
- [ ] Código revisado y aprobado por al menos otro miembro del equipo
- [ ] Se ha probado en los navegadores/entornos definidos como soporte mínimo.
- [ ] Seguridad validada: no hay fugas de información, validación del lado del servidor

---



### 🧾 HU-004 – Seguridad y Prevención de Fraude.

**Historia de Usuario:**
Como plataforma, quiero contar con mecanismos de seguridad y prevención de fraude que garanticen transacciones seguras y la integridad del ecosistema, evitando operaciones fuera del sistema y detectando comportamientos sospechosos.

--- 

### ✅ Criterios de Aceptación
- [ ] El sistema debe advertir al usuario que no se permite operar fuera de la plataforma.
- [ ] Los usuarios deben poder reportar comportamientos sospechosos o contenido indebido desde cualquier publicación o chat.
- [ ] El contenido sospechoso debe ser filtrado automáticamente usando palabras clave o patrones definidos.
- [ ] Las denuncias deben generar una alerta al equipo de moderación para su revisión manual.
- [ ] Deben existir canales de soporte oficiales accesibles desde el perfil o menú principal.
- [ ] Debe haber una sección para que el usuario consulte el estado de sus reportes.

---

### 🧪 Definition of Done (DoD)
- [ ] Historia validada por el equipo de QA y aprobada por el PO.
- [ ] El sistema muestra advertencias claras y visibles al usuario indicando que no está permitido realizar transacciones fuera de la plataforma.
- [ ] La interfaz de reporte es accesible, intuitiva y permite describir el motivo del reporte.
- [ ] El contenido que coincide con estos criterios se etiqueta como sospechoso y puede ser: Ser bloqueado automáticamente, Generar un aviso al usuario o Activar un flujo de revisión manual.
- [ ] Se implementaron pruebas unitarias y de integración
- [ ] Cumple con estándares de accesibilidad y usabilidad.
- [ ] Se habilitan canales de soporte accesibles desde el perfil y desde el menú principal.

---

### 🧾 HU-005 – Publicación de Productos

**Historia de Usuario:**  
Como usuario vendedor, quiero poder publicar productos en la plataforma completando todos los datos necesarios, subiendo imágenes y archivos técnicos, y estableciendo las condiciones de entrega, para que mis productos sean visibles y confiables para los potenciales compradores.

---

#### ✅ Criterios de Aceptación

- [ ] El formulario de publicación incluye campos obligatorios: título, categoría, estado del producto, unidad de venta, precio y descripción técnica.
- [ ] El usuario puede subir entre 1 y 10 imágenes por producto (formatos admitidos: JPG, PNG).
- [ ] Se debe indicar la ubicación del producto (localidad y provincia).
- [ ] El usuario puede seleccionar condiciones de entrega: retiro en domicilio, logística propia o envío acordado con el comprador.
- [ ] El usuario puede adjuntar una ficha técnica en formato PDF o como imagen adicional.
- [ ] Toda publicación pasa por una revisión automática (validaciones básicas).
- [ ] Luego se aplica una moderación manual antes de que el producto sea visible públicamente.
- [ ] El usuario recibe una notificación si su publicación es aprobada, rechazada o requiere cambios.

---

#### 🧪 Definition of Done (DoD)

- [ ] Validación completa del formulario de publicación con campos obligatorios y formatos admitidos.
- [ ] Subida y visualización de imágenes correctamente testeada en distintos navegadores.
- [ ] Se probaron las tres opciones de entrega en el frontend y backend.
- [ ] Validación de archivo técnico adjunto (PDF o imagen).
- [ ] Simulación de estados de publicación (en revisión, rechazada, publicada).
- [ ] Pruebas de notificaciones (visualización o envío por email).
- [ ] Historia verificada por QA en entorno QA y validada por PO.

---


### 🧾 HU-006 – Calificación y Reputación

**Historia de Usuario:**
Como usuario de la plataforma, quiero poder calificar las operaciones realizadas con otros usuarios y ver su reputación pública, para tomar decisiones más informadas y seguras al comprar o vender productos.

---

### ✅ Criterios de Aceptación
- [ ] Tanto el comprador como el vendedor deben poder calificar la operación con un puntaje de 1 a 5 estrellas al finalizarla.
- [ ] La calificación debe estar disponible únicamente una vez que la transacción esté confirmada como finalizada.
- [ ] El sistema debe permitir dejar un comentario opcional junto con la calificación.
- [ ] La reputación promedio del usuario (basada en estrellas) debe mostrarse públicamente en su perfil.
- [ ] Los comentarios deben estar visibles públicamente con nombre, rol (comprador o vendedor) y fecha.
- [ ] El usuario no puede calificar más de una vez la misma operación.
- [ ] El sistema debe evitar comentarios ofensivos o fuera de lugar mediante moderación automática/manual.

---

### 🧪 Definition of Done (DoD)
- [ ] Historia validada por el equipo de QA y aprobada por el PO.
- [ ] Al finalizar una transacción confirmada, tanto el comprador como el vendedor pueden calificar al otro usuario con un puntaje de 1 a 5 estrellas.
- [ ] El sistema valida que la calificación solo esté habilitada una vez que la operación esté marcada como finalizada.
- [ ] Cada perfil de usuario muestra públicamente su reputación promedio basada en todas las calificaciones recibidas.
- [ ] El usuario puede añadir un comentario de texto junto con la calificación.
- [ ] Se implementa un sistema de moderación automática de comentarios ofensivos o inapropiados (mediante listas negras, detección de lenguaje, etc.).
- [ ] Los comentarios potencialmente ofensivos se bloquean, ocultan o se derivan a moderación manual.
- [ ] La visualización pública de reputación y comentarios es responsiva y accesible.

---


### 🧾 HU-007 – Registro y Creación de Cuenta

**Historia de Usuario:**  
Como nuevo usuario, quiero poder registrarme fácilmente en la plataforma mediante correo electrónico o cuenta de Google, y validar mi identidad si soy una empresa, para comenzar a utilizar los servicios de manera segura.

---

#### ✅ Criterios de Aceptación

- [ ] El usuario puede registrarse con un correo electrónico y una contraseña.
- [ ] Tras el registro, el usuario recibe un correo con un enlace de confirmación de cuenta.
- [ ] El usuario tiene la opción de registrarse mediante cuenta de Google usando OAuth.
- [ ] Si el usuario se registra como empresa, debe completar los siguientes datos:
  - [ ] CUIT
  - [ ] Razón social
  - [ ] Nombre del representante legal
  - [ ] Subida de comprobante de inscripción AFIP o constancia de monotributo/responsable inscripto
- [ ] Si el usuario se registra como comprador particular, la validación de identidad es opcional.
- [ ] Todos los usuarios deben aceptar los Términos y Condiciones y la Política de Privacidad antes de enviar el formulario.
- [ ] El sistema valida todos los campos obligatorios antes de permitir el envío del formulario.

---

#### 🧪 Definition of Done (DoD)

- [ ] Historia validada por el equipo de QA y aprobada por el PO.
- [ ] El flujo de registro fue probado con email y OAuth.
- [ ] Se validó la carga y validación de documentos para empresas.
- [ ] Se probaron los errores de validación por campos incompletos.
- [ ] Se validó la persistencia de datos y envío de correo de confirmación.
- [ ] No existen errores bloqueantes ni de alta severidad abiertos.
- [ ] La historia fue desplegada correctamente en entorno QA y verificada.

---


### 🧾 HU-008 – Proceso de Compra 

**Historia de Usuario:**
Como comprador, quiero poder comunicarme con el vendedor dentro de la plataforma, solicitar cotizaciones para compras grandes, negociar precios por volumen, y confirmar la recepción del producto para liberar el pago de forma segura, incluyendo el comprobante fiscal correspondiente, para asegurar una compra confiable y transparente.

---

### ✅ Criterios de Aceptación
- [ ] El comprador debe poder iniciar una conversación con el vendedor desde la página del producto o desde su perfil
- [ ] Debe existir un chat interno para la comunicación entre ambas partes.
- [ ] El comprador debe poder solicitar una cotización especial para grandes volúmenes.
- [ ] La plataforma debe gestionar el pago en modalidad escrow y liberarlo una vez que el comprador confirme la entrega.
- [ ] El sistema debe permitir subir o generar factura electrónica tipo A o B según corresponda a la operación.
- [ ] Debe haber una opción de mostrar precios escalonados según volumen (por ejemplo: 1-10 unidades, 11-50, 51+).
- [ ] Las condiciones pactadas (precio, cantidad, entrega) deben estar visibles para ambas partes antes de confirmar la operación.

---

### 🧪 Definition of Done (DoD)
- [ ] Historia validada por el equipo de QA y aprobada por el PO.
- [ ] El comprador puede iniciar una conversación desde: La página del producto y el perfil del vendedor
- [ ] Existe un chat interno funcional con: Mensajería en tiempo real o con actualización dinámica, historial accesible, identificación clara de roles (comprador/vendedor) y soporte para mensajes de texto, enlaces y solicitudes de cotización
- [ ] El vendedor puede responder con una cotización ajustada.
- [ ] El sistema permite al comprador marcar la operación como "entrega confirmada"
- [ ] Solo tras la confirmación se libera el pago al vendedor.
- [ ] El sistema permite subir o generar factura electrónica tipo A o B según corresponda (definido por tipo de usuario o CUIT).
- [ ] La aceptación de las condiciones queda registrada como parte de la operación.
- [ ] La factura está disponible para ambas partes desde el resumen de operación.
- [ ] Se validan los datos fiscales requeridos antes de generar el comprobante.
- [ ] Interfaz validada para accesibilidad y experiencia de usuario

---


### 🧾 HU-009 - Navegación y Búsqueda

**Historia de Usuario:**
Como usuario comprador, quiero poder buscar productos fácilmente mediante palabras clave y aplicar filtros relevantes, para encontrar rápidamente lo que necesito en base a categoría, ubicación, precio, tipo y estado del producto. Además, quiero poder cambiar entre vista de lista o cuadrícula para visualizar los resultados de la manera que prefiera.

---

### ✅ Criterios de Aceptación
- [ ] El usuario debe poder buscar productos mediante un campo de búsqueda con palabras clave.
- [ ] El sistema debe mostrar resultados relevantes en tiempo real o al presionar "Enter".
- [ ] El usuario debe poder aplicar filtros combinados: categoría, ubicación, rango de precio, tipo de producto y estado.
- [ ] Los resultados deben poder visualizarse en formato lista o cuadrícula, según la preferencia del usuario.
- [ ] La vista seleccionada debe mantenerse al navegar entre páginas (persistencia).
- [ ] Si no hay resultados, debe mostrarse un mensaje claro indicando que no se encontraron productos.

---

### 🧪 Definition of Done (DoD)
- [ ] Historia validada por el equipo de QA y aprobada por el PO.
- [ ] Existe un campo de búsqueda accesible y visible en la interfaz principal.
- [ ] El usuario puede ingresar palabras clave para buscar productos.
- [ ] El sistema muestra resultados relevantes al presionar "Enter" o en tiempo real (autosuggest o autocompletado si aplica).
- [ ] El usuario puede aplicar múltiples filtros a la vez, incluyendo:
  - Categoría del producto
  - Ubicación (por ciudad, provincia o región)
  - Rango de precios (mínimo – máximo)
  - Tipo de producto (nuevo, usado, etc.)
- Estado del producto (excelente, bueno, regular, etc.)
- [ ] Los filtros aplicados se reflejan de forma clara en la interfaz.
- [ ] Se puede borrar individualmente cada filtro o todos a la vez con un botón de "limpiar filtros".
- [ ] El cambio de vista es inmediato y sin recarga completa de página.
- [ ] Si la búsqueda no arroja coincidencias, se muestra un mensaje claro y empático como:
“No se encontraron productos para tu búsqueda. Intenta modificar los filtros o palabras clave.”
- [ ] Se valida el rendimiento del sistema de búsqueda (respuestas rápidas, sin recarga completa).
- [ ] Se asegura la compatibilidad con dispositivos móviles y accesibilidad
- [ ] Se validó que los filtros no rompen la navegación ni generan inconsistencias en los resultados

---


### 🧾 HU-010 – Perfil del Usuario

**Historia de Usuario:**  
Como usuario de la plataforma, quiero tener un perfil donde pueda gestionar mi información personal y comercial, visualizar mi historial de actividad y mostrar ciertos datos públicos que refuercen mi reputación y credibilidad en la comunidad.

---

#### ✅ Criterios de Aceptación

- [ ] El usuario puede visualizar sus datos públicos: razón social o nombre comercial, ubicación general y reputación.
- [ ] Los datos privados (correo electrónico, teléfono, CUIT, nombre del responsable) solo son visibles para el usuario y el sistema.
- [ ] El perfil permite visualizar el historial de compras, ventas y calificaciones.
- [ ] El usuario puede subir un logo de su empresa, agregar un sitio web y seleccionar un rubro comercial.
- [ ] El tipo de usuario se muestra claramente en el perfil (Vendedor Empresa, Comprador Particular, Comprador Empresa).
- [ ] Otros usuarios pueden consultar datos públicos del perfil en contextos como productos, empresas o historial.
- [ ] La edición de datos privados solo puede hacerse desde un área segura del perfil (requiere sesión iniciada).

---

#### 🧪 Definition of Done (DoD)

- [ ] Visualización y separación correcta entre datos públicos y privados.
- [ ] Pruebas de visibilidad según tipo de usuario y rol.
- [ ] Flujo completo de edición probado (con campos obligatorios y validaciones).
- [ ] Subida de imágenes (logo) validada en entorno QA.
- [ ] Pruebas de seguridad para prevenir acceso no autorizado a datos privados.
- [ ] Validación cruzada de historial de actividad con base de datos.
- [ ] Historia aprobada por QA y PO.

---


### 🧾 HU-011 – Inicio de Sesión y Seguridad

**Historia de Usuario:**  
Como usuario registrado, quiero poder iniciar sesión de forma segura utilizando mi correo electrónico y contraseña, con medidas de protección como reCAPTCHA y autenticación de dos factores, y tener la opción de recuperar el acceso si olvido mi contraseña.

---

#### ✅ Criterios de Aceptación

- [ ] El usuario puede iniciar sesión con correo electrónico y contraseña válidos.
- [ ] El formulario de inicio de sesión incluye reCAPTCHA para bloquear intentos automatizados.
- [ ] Si el usuario tiene 2FA activado, el sistema envía un código de verificación por correo electrónico luego de ingresar las credenciales correctas.
- [ ] El usuario no puede acceder a su cuenta sin ingresar correctamente el código 2FA.
- [ ] El formulario incluye la opción “¿Olvidaste tu contraseña?”.
- [ ] Al solicitar recuperación, el usuario recibe un correo con un enlace seguro.
- [ ] El enlace lleva a una pantalla protegida donde el usuario puede establecer una nueva contraseña.
- [ ] El sistema valida que el correo esté previamente verificado antes de permitir la recuperación.


#### 🧪 Definition of Done (DoD)

- [ ] Pruebas funcionales realizadas con y sin 2FA.
- [ ] Validación del envío de correos (2FA y recuperación) en entorno QA.
- [ ] Pruebas de seguridad con reCAPTCHA correctamente implementado.
- [ ] Pruebas de flujo completo de recuperación de contraseña.
- [ ] Validación del bloqueo de acceso si el código 2FA no es ingresado.
- [ ] No existen bugs críticos abiertos relacionados al login.
- [ ] La funcionalidad fue validada por QA y aprobada por el PO.

---

