# Política de Seguridad

La seguridad de las operaciones, la privacidad de los datos de infraestructura y la protección de credenciales son pilares fundamentales de **Heimdall Sentinel System**.

---

## Versiones con Soporte de Seguridad

| Versión | Estado de Soporte |
| :--- | :--- |
| **2.2.x** | :white_check_mark: Soporte activo (Recomendada) |
| **2.1.x** | :warning: Parches críticos únicamente |
| **< 2.1.0**| :x: Fin de soporte |

---

## Directrices de Gestión de Credenciales y Claves API

1. **Gestión Local**:
   - Heimdall nunca envía telemetría de uso ni recopila información sensible hacia servidores externos.
   - Las claves de API (como las credenciales de **AbuseIPDB**) se almacenan de forma local en el archivo `config.json` de la máquina del operador.
2. **Exclusión de Repositorio**:
   - El archivo `config.json` se encuentra ignorado deliberadamente en el control de versiones (`.gitignore`).
   - Se debe utilizar siempre `config.example.json` para desplegar nuevas instalaciones.
   - Si detecta que una clave real ha sido expuesta accidentalmente en un commit, revóquela de inmediato en el panel del proveedor correspondiente.

---

## Notificación de Vulnerabilidades

Si identifica una vulnerabilidad de seguridad o un defecto que comprometa la integridad de los datos:

1. **No abra una incidencia pública** en el rastreador de problemas de GitHub.
2. Contacte directamente al mantenedor del proyecto (**Hungrow**) por correo electrónico o a través de los canales internos del equipo de operaciones.
3. Proporcione un informe detallado con:
   - Pasos para reproducir el fallo.
   - Entorno operativo y versión exacta de Heimdall afectada.
   - Impacto estimado sobre la infraestructura.

Agradecemos su colaboración responsable para mantener segura la suite operativa.
