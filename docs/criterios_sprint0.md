# 📋 Criterios de Aceptación – Sprint 0

Este documento reúne los **criterios de aceptación** y la **Definition of Done (DoD)** para las historias de usuario incluidas en el Sprint 0 del proyecto **Primarket**.

Los criterios de aceptación están redactados de forma clara, objetiva y verificable. Su propósito es alinear las expectativas del equipo de desarrollo, producto y QA para asegurar que cada historia cumpla con las condiciones necesarias para ser considerada “hecha”.

Cada entrada incluye:
- 🧾 La historia de usuario correspondiente
- ✅ Criterios de aceptación (funcionales y técnicos)
- 🧪 Definition of Done (DoD): checklist mínimo de calidad y entregables

Este documento sirve como **base para el diseño de casos de prueba**, revisión de historias, seguimiento de avances y validación previa al cierre de cada tarea.

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
- [ ] Historia aprobada por QA y Product Owner.

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

---

#### 🧪 Definition of Done (DoD)

- [ ] Pruebas funcionales realizadas con y sin 2FA.
- [ ] Validación del envío de correos (2FA y recuperación) en entorno QA.
- [ ] Pruebas de seguridad con reCAPTCHA correctamente implementado.
- [ ] Pruebas de flujo completo de recuperación de contraseña.
- [ ] Validación del bloqueo de acceso si el código 2FA no es ingresado.
- [ ] No existen bugs críticos abiertos relacionados al login.
- [ ] La funcionalidad fue validada por QA y aprobada por el Product Owner.

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
