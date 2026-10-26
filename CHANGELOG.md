# Registro de Versiones (Changelog)

Todos los cambios notables realizados en **Heimdall Sentinel System** se documentan en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/),
y el proyecto sigue las directrices de [Semantic Versioning](https://semver.org/lang/es/).

---

## [2.2.7] - 2026-10-26

### Añadido
- **Soporte Multimonitor Integral**: Interceptor global de diálogos (`messagebox` y `filedialog`) que asegura la apertura de cualquier ventana emergente directamente en el monitor donde se encuentra la aplicación activa.
- **Posicionamiento Geométrico en Pantallas Secundarias**: Nuevo algoritmo de centrado para ventanas modales sobre espacios de escritorio virtual con coordenadas negativas o extendidas.
- **Formato Estructurado de Resumen de Conciliación**: Nuevo diseño en texto estilizado con métricas claras de balance, agrupación limpia por estado y marcas temporales normalizadas.
- **Segregación Estricta de Estados**: Clasificación independiente entre incidencias resueltas respecto al período anterior y procesos que se encontraban en curso.

### Cambiado
- **Flujo Directo en Módulo de Sincronización**: Procesamiento y generación de diagnóstico automáticos al cargar el fichero de registros, retirando pasos manuales redundantes.
- **Barra Superior Dinámica**: Reorganización responsiva de botones de acceso rápido y búsqueda Spotlight con anclaje adaptable para evitar colisiones en resoluciones con escalado DPI (125%, 150%).

### Corregido
- **Ordenación Cronológica en Lotes de Registros**: Extracción precisa de fechas en cabecera durante la ejecución en segundo plano para garantizar el emparejamiento exacto de datasets heterogéneos.
- **Visualización de Tooltips de Asistencia**: Corrección en el cálculo de límites de pantalla para evitar desvíos hacia el monitor primario en configuraciones multimonitor.

---

## [2.2.6] - 2026-10-21

### Añadido
- **Pantalla de Carga Dinámica (Splash Screen)**: Indicador de inicio con barra de progreso, identidad visual del sistema y reporte en tiempo real de carga de componentes.
- **Automatización por Días Operativos**: Lógica contextual en la interfaz para destacar flujos de auditoría de registros según el día de la semana.
- **Filtrado y Exportación de Indicadores Críticos**: Modal interactivo para consolidar y exportar listados de direcciones IP anómalas a partir de telemetría perimetral.
- **Base de Conocimiento de Comandos**: Árboles de referencia técnica offline estructurados para sintaxis operativa y diagnóstico de sistemas.

### Optimizado
- Mayor estabilidad y comprobaciones de integridad en el script autónomo de reemplazo transaccional de versiones.

---

## [2.2.5] - 2026-10-15

### Añadido
- **Modo Vigía (Keep-Awake Sentinel)**: Módulo de micro-actividad en segundo plano para estaciones de supervisión en tiempo real.
- **Sentinel Spotlight**: Búsqueda omnidireccional con atajo de teclado para direccionamiento de red, diagramas de topología y documentación.
- **Integración con Feeds de Amenazas**: Ingesta y comprobación automática de variaciones en listas públicas de indicadores de compromiso (IOCs).

---

## [2.2.0] - 2026-09-25

### Añadido
- **Particionado de Scripts de Configuración**: División parametrizable de scripts de aprovisionamiento en bloques de tamaño configurable para consolas de administración CLI.
- **Módulo NetKit**: Herramientas integradas para cálculo de subredes, detección de colisiones IP y normalización de formatos de red.
- **Persistencia Avanzada**: Panel de Ajustes con detección de modificaciones sin guardar.

---

## [2.1.0] - 2026-09-18

### Añadido
- **Motor de Conciliación de Registros**: Cruce y desduplicación jerárquica de registros entre distintas plataformas de almacenamiento.
- **Generación de Libros de Cálculo**: Informes estructurados con formato condicional y cálculo automático de métricas.

---

## [2.0.0] - 2026-09-15

### Añadido
- **Lanzamiento de la Plataforma Heimdall**: Unificación de utilidades operativas y de seguridad bajo una suite modular moderna en Python y CustomTkinter.
- **Actualizador Idempotente**: Detección y despliegue autónomo de revisiones.
