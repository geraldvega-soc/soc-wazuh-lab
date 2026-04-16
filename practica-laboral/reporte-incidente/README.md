# 🚨 Reporte de Incidente — React2Shell (CVE-2025-55182)

**Fecha del incidente:** 7 de enero de 2026  
**Servidor afectado:** nodo1-kh (Agente ID 017)  
**Severidad:** Crítica — CVSS 10.0  
**Herramienta de detección:** Wazuh SIEM  
**Analista:** Gerald Vega Soto  

---

## 📌 Resumen ejecutivo

El servidor `nodo1-kh` fue comprometido mediante la vulnerabilidad crítica **React2Shell**, que afecta versiones vulnerables de **Next.js** y permite **ejecución remota de código (RCE) sin autenticación**. El incidente fue detectado a través de Wazuh y analizado durante la jornada del 7 de enero de 2026.

---

## 🔓 Vulnerabilidad explotada

| Campo | Detalle |
|---|---|
| **CVE** | CVE-2025-55182 / CVE-2025-66478 |
| **Nombre** | React2Shell |
| **CVSS** | 10.0 (Crítico) |
| **Componente afectado** | Next.js — React Server Components (RSC Flight) |
| **Vector de ataque** | Deserialización insegura vía peticiones POST |
| **Autenticación requerida** | Ninguna |
| **Referencia** | Unit 42 (Palo Alto Networks) |

---

## 🕐 Línea de tiempo

| Fecha | Evento |
|---|---|
| 7 de septiembre 2025 | Imagen del servidor buildeada con versión vulnerable de Next.js |
| 3 de diciembre 2025 | Publicación pública de la vulnerabilidad React2Shell |
| 7 de enero 2026 | Detección del incidente en Wazuh — servidor `nodo1-kh` comprometido |
| 7 de enero 2026 | Análisis forense y reporte presentado al Director Giovanni |
| 7 de enero 2026 | Habilitación del módulo Vulnerability Detection como medida preventiva |

---

## 🔎 Evidencias detectadas en Wazuh

- Múltiples intentos de autenticación sospechosa en el servidor afectado
- Accesos desde ubicaciones geográficas no habituales
- Patrones de post-explotación:
  - Intentos de acceso a claves SSH
  - Búsqueda de credenciales (AWS, variables `.env`)
- Comportamiento alineado con técnicas documentadas por **Unit 42 (Palo Alto Networks)**

---

## 🛡️ Medidas tomadas

1. Identificación y confirmación del vector de ataque (vulnerabilidad de aplicación, no credenciales)
2. Reporte formal al Director de Seguridad
3. Habilitación del módulo **Vulnerability Detection** en Wazuh para detección proactiva de CVEs
4. Refuerzo del monitoreo de aplicaciones web en los agentes

---

## 📁 Archivos

| Archivo | Descripción |
|---|---|
| `Reporte_de_incidente_07-01-2026.docx` | Reporte enviado al Director |
| `Habilitacion_Modulo_Vulnerability_Detection_Wazuh.docx` | Procedimiento implementado como respuesta al incidente |

---

## 🧠 Lecciones aprendidas

- Las vulnerabilidades de aplicación (sin autenticación) representan vectores críticos que no siempre son cubiertos por controles de acceso tradicionales.
- El monitoreo proactivo con Vulnerability Detection permite identificar software desactualizado antes de ser explotado.
- La correlación de eventos en Wazuh (autenticaciones anómalas + geolocalización + post-explotación) fue clave para confirmar el compromiso.
