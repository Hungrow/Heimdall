# Registro de Cambios (Changelog)

Todos los cambios notables realizados en el proyecto **Heimdall Sentinel System** se documentan en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/),
y este proyecto se adhiere a [Semantic Versioning](https://semver.org/lang/es/).

---

## [2.2.7] - 2026-10-26

### Añadido
- **Soporte Multimonitor Total**: Interceptor global de diálogos (`_patch_dialogs()`) que vincula automáticamente cuadros `messagebox` y diálogos de explorador `filedialog` a la ventana activa de Heimdall, sin importar en qué monitor se encuentre la aplicación.
- **Centrado Geométrico en Escritorios Virtuales Extendidos**: Implementado `posicionar_modal_en_padre()` para ventanas `CTkToplevel` que soporta coordenadas globales negativas (pantallas a la izquierda o arriba del monitor principal).
- **Separación de Estados en Resumen Consolidado TXT**: El informe de fin de semana ahora cuenta con dos secciones estrictamente independientes: `[SUBSANACIONES DE FALLOS RESPECTO AL DÍA ANTERIOR]` y `[TRABAJOS QUE ESTABAN EN CURSO Y HAN FINALIZADO]`.
- **Nuevo Formato Visual Estilizado de Backups**: Rediseño del archivo `Alertas_Heimdall_FinDeSemana_*.txt` con tarjetas ASCII estructuradas, resumen horizontal de balance (`✓ Éxitos | ⏳ En curso | ❌ Fallos | Total`) y timestamps normalizados al estándar `DD/MM/AAAA HH:MM` (eliminando microsegundos `.000000`).

### Cambiado
- **Módulo OIDSync**: Eliminado el botón manual redundante "Analizar y Diagnosticar Log"; ahora la carga del archivo desencadena de inmediato el diagnóstico y redacción del correo.
- **Distribución de la Barra Superior**: Reestructuración dinámica del botón de Modo Vigía (`☕`), Modo Ayuda (`?`) y barra Spotlight (`🔍 Buscar...`) con anclaje a la derecha (`pack(side="right")`), previniendo solapamientos en pantallas de alto escalado DPI (125%, 150%).

### Corregido
- **Detección Cronológica Criterio A (Commvault/NetBackup)**: Corregida la extracción de la cabecera `Generated on:` en ficheros de Commvault dentro del hilo de procesamiento en segundo plano, garantizando el emparejamiento exacto de los días 24, 25 y 26 con sus correspondientes informes.
- **Tooltips Flotantes**: Corregido el reposicionamiento de las tarjetas pedagógicas de ayuda para evitar que salten a la pantalla primaria al superar los límites de la pantalla secundaria.

---

## [2.2.6] - 2026-10-21

### Añadido
- **Pantalla de Inicio Animada (Splash Screen)**: Pantalla de carga dinámica con diseño moderno, icono corporativo oficial (`heimdall.ico`), barra de progreso animada y reporte de estado de carga de subsistemas en tiempo real.
- **Detección Inteligente del Día de la Semana**: Los Lunes se despliega automáticamente el panel de procesamiento por lotes de fin de semana en Modo Piloto; los Miércoles se muestra un recordatorio en consola para retirar la VPN al operar con WAFs.
- **Extracción de IPs Críticas en WAF**: Nueva ventana modal interactiva para filtrar, desduplicar y exportar a un fichero `.txt` las direcciones IP marcadas en estado Rojo (reportadas) de los informes analizados en memoria o descubiertos en disco.
- **Clarificación de Fuentes en Lotes de Backups**: Nombres descriptivos para CSVs 1 (NetBackup), CSVs 2 (Commvault) y CSV Día Previo en el panel de fin de semana.
- **Árboles Semánticos de Comandos**: Integración de bases de referencia técnica offline para Checkpoint Gaia (Expert y Clish), Linux y PowerShell.

### Optimizado
- Mayor robustez en el script batch autónomo de reemplazo de binarios (`apply_update.bat`).
- Manejo preventivo de excepciones de concurrencia al empaquetar con PyInstaller.

---

## [2.2.5] - 2026-10-15

### Añadido
- **Modo Vigía (Keep-Awake Sentinel)**: Módulo discreto en segundo plano con micro-movimientos de cursor en trayectorias circulares para prevenir el bloqueo de sesión y suspensión del sistema durante turnos de supervisión.
- **Sentinel Spotlight**: Búsqueda global omnidireccional con atajo rápido para direccionamiento IP, diagramas de red y documentación operativa.
- **Sincronización con Feodotracker**: Descarga y cotejo automático de variantes en listas de botnets C2 de Abuse.ch.

---

## [2.2.0] - 2026-09-25

### Añadido
- **Particionador Checkpoint**: División inteligente de scripts SecureCRT `.vbs` en bloques parametrizables (ej. 500 líneas) para evitar bloqueos por sobrecarga de búfer en consolas de gestión.
- **Módulo NetKit**: Calculadora de subredes con detección de solapamiento y formateador de direcciones MAC.
- **Gestión Avanzada de Configuración**: Panel centralizado de Ajustes con comprobación de cambios pendientes al cambiar de pestaña.

---

## [2.1.0] - 2026-09-18

### Añadido
- **Conciliación Cruzada de Backups**: Algoritmo inicial para cruzar incidencias entre Veritas NetBackup y Commvault.
- **Parser de Sincronización OIDSync**: Detección de patrones de error en trazas de texto y confección del correo de incidencias de usuarios.
- **Generador de Informes Excel**: Plantillas ejecutivas con formato condicional y fórmulas dinámicas de resumen.

---

## [2.0.0] - 2026-09-15

### Añadido
- **Lanzamiento Inicial de la Suite Heimdall**: Unificación modular de herramientas dispersas de sistemas bajo una arquitectura moderna en Python y CustomTkinter.
- **Sistema de Actualización Continua**: Verificación de versiones contra repositorio de red y releases web.
