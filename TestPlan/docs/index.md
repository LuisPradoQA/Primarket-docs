
# Test Plan - Proyecto Primarket

**Versión:** 1.0

**Fecha:** 21/08/2023

**Responsable QA:** Luis Prado - Mateo Sorichetti Vilá

**Proyecto:** Primarket (E-commerce B2B - fabricantes y proveedores)

---

## 1. Introducción

### 1.1 Objetivo del Plan de Pruebas

Este plan de pruebas tiene como objetivo garantizar la calidad funcional, técnica y de experiencia del usuario en **Primarket**, una plataforma de comercio electrónico orientada a conectar fabricantes con proveedores de materia prima. Se realizará mediante una estrategia de testing integral que combine pruebas manuales, automatizadas y de rendimiento, alineadas con la metodología Scrum.

### 1.2 Documentos Relacionados

| NOMBRE                   | DESCRIPCIÓN                                                                                                                       |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| Repositorio del proyecto | [GitHub](https://github.com/users/Visual2024/projects/4)                                                                          |
| Issue tracker            | [Clickup](https://app.clickup.com/90131509380/v/l/2ky43c44-373?pr=90136315153)                                                    |
| Casos de prueba          | [PRIMARKET - Test Cases](https://docs.google.com/spreadsheets/d/1R068pTAraD3TfT1cuLUsIXSZiYd_C6fGkctYw7fjdXE/edit?usp=share_link) |

---

## 2. Alcance del Testing

### 2.1 Requerimientos de Pruebas Incluidos

| ID  | Módulo/Funcionalidad           | Descripción breve                                 |
| --- | ------------------------------ | ------------------------------------------------- |
| F01 | Registro de proveedor          | Alta con validación de email y datos fiscales     |
| F02 | Publicación de materias primas | Carga de insumos con disponibilidad y precio      |
| F03 | Catálogo del fabricante        | Visualización filtrada y búsqueda de proveedores  |
| F04 | Carrito de pedidos             | Selección, modificación y confirmación de pedidos |
| F05 | Historial de transacciones     | Listado y estado de pedidos anteriores            |

### 2.2 Requerimientos Excluidos

| Requerimiento                           | Motivo          |
| --------------------------------------- | --------------- |
| Integraciones con ERPs externos         | Fuera del scope |
| Validación legal o fiscal de documentos | Fuera del scope |

### 2.3 Casos de Prueba Incluidos

| ID   | TÍTULO                                     | ESTADO |
| ---- | ------------------------------------------ | ------ |
| TC-1 | Verificar login con credenciales válidas   | PASS   |
| TC-2 | Verificar login con credenciales inválidas | FAIL   |

### 2.4 Casos de Prueba Excluidos

| ID    | TÍTULO                         | ESTADO    |
| ----- | ------------------------------ | --------- |
| TC-10 | Registro de cuentas            | N/A       |
| TC-11 | Registro de cuentas duplicadas | N/A       |
| TC-12 | Recuperar contraseñas          | Deprecado |

### 2.5 Entorno de Pruebas

| Ambiente | URL                                                        |
| -------- | ---------------------------------------------------------- |
| QA       | [https://ambienteQA.com](https://ambienteQA.com)           |
| Preprod  | [https://ambientepreprod.com](https://ambientepreprod.com) |

---

## 3. Estrategia de las Pruebas

### 3.1 Configuración

1. **Datos necesarios:** ambiente disponible, credenciales, documentación API.
2. **Modalidad:** Casos en Testlink, ClickUp o Jira. Ejecución manual y automatizada.
3. **Tipos de pruebas:** Funcionales, APIs, rendimiento, exploratorias, responsive.
4. **Integraciones:** No previstas en esta etapa.
5. **Regresión:** Al final del ciclo y tras paso a producción.
6. **Herramientas de documentación:** Google Docs y Sheets.
7. **Herramientas de gestión:** Jira, ClickUp o Testlink.

### 3.2 Orden de Ejecución

Fases de mayo a agosto:

* Análisis
* Diseño de casos
* Ejecución
* Paso a producción
* Regresión post-release

### 3.3 Criterios de Inicio

* QA listo
* Plan aprobado
* APIs documentadas
* Casos de prueba diseñados
* Datos y accesos disponibles

### 3.4 Criterios de Término

* 100% de cobertura de ejecución
* Cero defectos críticos
* Documentación del cierre y responsables

### 3.5 Equipos y Responsabilidades

| Nombre    | Rol     | Responsabilidad                  |
| --------- | ------- | -------------------------------- |
| QA Lead   | QA Lead | Supervisar y representar QA      |
| QA Tester | QA      | Crear y ejecutar casos de prueba |

### 3.6 Gestión de Incidencias

Flujo resumido:

1. QA crea ticket en Clickup con evidencia.
2. Dev revisa y corrige (o rechaza).
3. QA revalida.
4. Ciclo se repite hasta cierre.

### 3.7 Plantilla de Reporte de Bugs

* ID, Título, Descripción
* Precondiciones, Datos de prueba
* Pasos, Resultado esperado vs actual
* Captura de pantalla / video
* Severidad, asignación, sprint destino, test case asociado

Campos opcionales: versión, navegador, ambiente.

---

## 4. Entregables

| Entregable                           | Link/Descripción                                                                                                        |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| Plan de pruebas                      | Este documento                                                                                                          |
| Casos de prueba                      | [Google Sheet](https://docs.google.com/spreadsheets/d/1R068pTAraD3TfT1cuLUsIXSZiYd_C6fGkctYw7fjdXE/edit?usp=share_link) |
| Evidencias de ejecución              | [Drive Folder](https://drive.google.com/drive/folders/1P3WAlA6S3MgXU1hHZnfBEFpgC8eE6xPs?usp=share_link)                 |
| Reportes de bugs en Clikup           | Interno                                                                                                                 |
| Informe final por sprint (QA review) | Interno                                                                                                                 |

---

🔚 *Fin del Test Plan – PRIMARKET v1.0*
