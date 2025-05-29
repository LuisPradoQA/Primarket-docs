# JMeter – Pruebas de Carga y Rendimiento

## Setup básico

1. Descargar Apache JMeter: [https://jmeter.apache.org/download\_jmeter.cgi](https://jmeter.apache.org/download_jmeter.cgi)
2. Crear archivo `.jmx` para prueba de carga inicial
3. Configurar propiedades según entorno QA (`Thread Group`, `HTTP Request`, `Listeners`)

## Escenarios sugeridos

| Escenario                         | Objetivo                           | Endpoint probado |
| --------------------------------- | ---------------------------------- | ---------------- |
| Carga masiva de login             | Validar estabilidad de login       | POST /auth/login |
| Consulta de productos concurrente | Simular múltiples usuarios         | GET /productos   |
| Publicación en lote               | Validar respuesta ante inserciones | POST /productos  |

## Métricas clave a capturar

* Tiempo medio de respuesta (ms)
* Transacciones por segundo (TPS)
* Porcentaje de errores

## Entregables sugeridos

* Archivo `.jmx` con configuración
* CSV de resultados
* Gráfico de resumen (tiempo vs usuarios)
* Recomendación técnica basada en análisis

> Requiere coordinación con el equipo DevOps para no afectar entornos activos.
