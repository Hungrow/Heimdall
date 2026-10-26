# 🛡️ HEIMDALL Sentinel System

<div align="center">

![Heimdall Banner](https://img.shields.io/badge/Heimdall-Sentinel%20System-0ea5e9?style=for-the-badge&logo=shield&logoColor=white)
![Release](https://img.shields.io/badge/Release-v2.2.7-10b981?style=for-the-badge&logo=github)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-3b82f6?style=for-the-badge&logo=windows)
![Python](https://img.shields.io/badge/Python-3.12+-ffd343?style=for-the-badge&logo=python&logoColor=black)
![Architecture](https://img.shields.io/badge/Architecture-Modular%20Desktop%20Suite-8b5cf6?style=for-the-badge)

<p align="center">
  <strong>Suite modular de ingeniería de sistemas, automatización de seguridad perimetral y análisis de telemetría de infraestructura.</strong>
</p>

</div>

---

## 📋 Descripción

**Heimdall Sentinel System** es una plataforma de escritorio diseñada para centralizar, automatizar y auditar flujos técnicos en infraestructuras corporativas. Unifica herramientas de análisis de registros, procesamiento de eventos de seguridad perimetral, diagnóstico de redes y generación de reportes ejecutivos bajo una interfaz gráfica moderna, reactiva y optimizada para estaciones de trabajo con múltiples pantallas.

---

## ⚡ Capacidades Principales

### 📊 Auditoría y Conciliación de Telemetría
* **Procesamiento de Registros**: Ingesta, parseo y cotejo de datasets y ficheros de actividad de múltiples plataformas.
* **Desduplicación Inteligente**: Algoritmo de resolución jerárquica para consolidar reintentos y ejecuciones múltiples.
* **Conciliación Cronológica**: Análisis histórico por lotes con detección de incidencias persistentes y eventos resueltos.
* **Informes Estructurados**: Generación automática de libros de cálculo ejecutivos y resúmenes formateados de incidencias.

### 🛡️ Inteligencia de Amenazas y Seguridad Perimetral
* **Extracción de Indicadores (IOCs)**: Aislamiento y consolidación de direcciones IP anómalas o clasificadas como críticas en eventos perimetrales.
* **Reputación y Verificación Externa**: Integración mediante API con servicios de reputación de amenazas y fuentes de inteligencia públicas.
* **Generación de Contramedidas**: Exportación de listados desduplicados y confección asistida de scripts de configuración para dispositivos de red y cortafuegos.
* **Control de Ejecución**: Particionamiento configurable de scripts para prevenir sobrecargas en consolas de gestión CLI.

### 🌐 Utilidades de Red y Diagnóstico (NetKit)
* **Calculadora CIDR**: Cálculo integral de parámetros de subred (máscaras, broadcast, rangos válidos y wildcard).
* **Análisis de Colisiones**: Verificación de solapamiento de direccionamiento IP entre diferentes segmentos.
* **Normalización de Formatos**: Limpieza y adaptación de direcciones físicas (MAC) y formatos de red heterogéneos.

### 🔍 Sentinel Spotlight y Navegación Universal
* **Búsqueda Global Integrada**: Acceso rápido (`Ctrl+F`) para consultar simultáneamente direccionamiento de red, diagramas de topología y referencias técnicas.
* **Base de Conocimiento Offline**: Árboles de referencia semántica para sintaxis de comandos y diagnóstico en sistemas operativos de servidor y appliances de red.

### 🖥️ Ergonomía y Operación Continua
* **Soporte Multimonitor**: Gestión de coordenadas virtuales para posicionar modales y diálogos de archivo en el monitor activo.
* **Modo Vigía**: Micro-actividad preventiva para estaciones de supervisión en tiempo real.
* **Interfaz Adaptativa**: Soporte para temas claro y oscuro con escalado dinámico para resoluciones de alta densidad (High-DPI).

---

## 🚀 Despliegue y Uso

### Ejecutable Standalone
El binario portable compilado está disponible en el apartado de [Releases](https://github.com/Hungrow/Heimdall/releases/latest). No requiere instalación de intérpretes ni dependencias adicionales en la estación de trabajo.

### Ejecución desde Código Fuente
```bash
# Clonar el proyecto
git clone https://github.com/Hungrow/Heimdall.git
cd Heimdall

# Crear entorno virtual e instalar dependencias
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt

# Iniciar la suite
python heimdall.py
```

---

## 🔒 Privacidad y Configuración

* **Aislamiento de Datos**: El procesamiento de telemetría, logs y datos analizados se ejecuta **100% en local** dentro de la estación de trabajo.
* **Gestión de Claves**: Las credenciales locales y claves API se gestionan mediante el archivo local `config.json` (ignorado en el control de versiones). Se incluye `config.example.json` como plantilla de referencia.

---

## 📜 Historial de Versiones

Consulta el archivo [CHANGELOG.md](CHANGELOG.md) para el desglose detallado de versiones y mejoras continuas.

---

<div align="center">
  <sub>Heimdall Sentinel System • Diseñado y mantenido por <strong>Hungrow</strong></sub>
</div>
