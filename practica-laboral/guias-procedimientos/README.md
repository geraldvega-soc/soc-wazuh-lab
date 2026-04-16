# 📘 Guías y Procedimientos Técnicos

Documentación técnica elaborada durante la práctica laboral, orientada a procedimientos operativos del entorno Wazuh.

---

## 📄 Archivos

| Archivo | Descripción |
|---|---|
| `Guia_Dashboard_Wazuh_Alertas_Criticas.docx` | Guía completa para crear dashboards de monitoreo de alertas críticas en Wazuh |
| `Habilitacion_Modulo_Vulnerability_Detection_Wazuh.docx` | Procedimiento paso a paso para habilitar Vulnerability Detection — elaborado como respuesta al incidente del 7 de enero |

---

## 🔧 Detalle de guías

### Guía Dashboard Wazuh — Alertas Críticas
Este documento cubre:
- Módulos críticos de Wazuh para detección de amenazas
- Reglas para ataques de fuerza bruta SSH/RDP (IDs: 5712, 5551, 5763)
- Reglas de File Integrity Monitoring (IDs: 550, 553, 554, 592)
- Reglas de escalada de privilegios (IDs: 5401, 5901)
- Detección de ataques web (SQLi, XSS, Directory Traversal)

### Procedimiento Vulnerability Detection
Documento entregado al Director Giovanni como respuesta al incidente React2Shell:
- Habilitación del módulo en `ossec.conf`
- Configuración del Wazuh Indexer
- Configuración de agentes con Syscollector (hotfixes Windows)
- Verificación de logs y validación en dashboard
