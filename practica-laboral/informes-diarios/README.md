# 📅 Informes Diarios de Seguridad — Wazuh

Informes generados durante el análisis diario de alertas como analista SOC nivel 1.  
Cada informe cubre el período de las últimas 24 horas de monitoreo.

---

## 📄 Archivos

| Archivo | Fecha | Contenido destacado |
|---|---|---|
| `Documentacion_08-01-2026-jueves.docx` | 07–08 ene 2026 | Brute force SSH desde IPs externas, actividad FIM en rutas EFI y Docker |
| `documentacion_de_wazuh__24-12-2025_.docx` | 24 dic 2025 | Migración de servidor Wazuh, análisis de 80.422 eventos, threat hunting |
| `documentacion_de_wazuh_lunes_29-12-2025.docx` | 29 dic 2025 | Validación de FIM/Syscheck, eventos modified y added |
| `documentacion_de_wazuh_2__05-01-2026.docx` | 05 ene 2026 | Análisis FIM agente dhana.argonos.cl (1.991 alertas), cambios root |
| `documentacion_1.docx` | Dic 2025 | Confirmación operatividad FIM, comunicación al Director |
| `informe_28-01-2026.docx` | 28 ene 2026 | Ataques fuerza bruta SSH en 5 agentes, sin compromiso confirmado |

---

## 📊 Estructura de cada informe

Cada informe diario sigue esta estructura:
1. **Resumen ejecutivo** — estado general del período
2. **Eventos relevantes detectados** — alertas de nivel ≥ 10
3. **Agentes involucrados** — nodos con mayor actividad
4. **Análisis** — interpretación de patrones
5. **Conclusión y estado general**

---

## 🔑 Hallazgos recurrentes documentados

- Ataques de fuerza bruta SSH desde IPs externas geolocalizadas en EE.UU., Corea del Sur, Alemania y Países Bajos
- Volumen elevado de alertas de bajo nivel (ruido operativo) — hasta 78.610 alertas en 24 horas
- Modificaciones en archivos críticos del sistema (rutas EFI, Docker) por usuario root
- 13 agentes monitoreados activos de forma continua
