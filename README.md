# Auditoría de Seguridad Web – OWASP Top 10

Proyecto de análisis de vulnerabilidades realizado sobre un sitio web de gestión inmobiliaria como ejercicio práctico de ciberseguridad.

El objetivo fue identificar posibles debilidades de seguridad en la aplicación web utilizando herramientas de análisis automatizado y revisión manual basada en estándares de la industria.

---

## Información del Proyecto

- **Tipo de análisis:** Auditoría de seguridad web
- **Metodología:** OWASP Top 10
- **Enfoque:** Black-box testing
- **Herramienta principal:** OWASP ZAP (Zed Attack Proxy)
- **Fecha:** Marzo 2026
- **Entorno analizado:** Localhost (entorno de desarrollo)

---

## Tecnologías del Sitio Analizado

- HTML5
- CSS3
- JavaScript (ES6+)

---

## Herramientas Utilizadas

- OWASP ZAP
- Firefox DevTools

---

## Metodología de Auditoría

El análisis se realizó siguiendo un enfoque de evaluación de vulnerabilidades basado en OWASP Top 10.

Fases ejecutadas:

1. **Reconocimiento**
   - Identificación de la estructura del sitio y tecnologías utilizadas.

2. **Escaneo automatizado**
   - Uso de OWASP ZAP para detectar vulnerabilidades comunes.

3. **Análisis de alertas**
   - Revisión manual y clasificación de hallazgos.

4. **Documentación**
   - Elaboración de reporte técnico con evidencia, impacto y recomendaciones.

---

## Resultados de la Auditoría

Se identificaron **4 vulnerabilidades de riesgo medio**, relacionadas principalmente con configuraciones de seguridad HTTP.

| ID | Vulnerabilidad | Riesgo | CWE |
|---|---|---|---|
| VUL-001 | CSP: Falla al definir directiva sin fallback | Medio | CWE-693 |
| VUL-002 | Cabecera Content-Security-Policy no configurada | Medio | CWE-693 |
| VUL-003 | Falta de Subresource Integrity (SRI) en recursos externos | Medio | CWE-345 |
| VUL-004 | Falta de cabecera anti-clickjacking (X-Frame-Options) | Medio | CWE-1021 |

---

## Posibles Impactos

Las vulnerabilidades identificadas podrían permitir ataques como:

- Clickjacking
- Ejecución de scripts maliciosos
- Manipulación de recursos externos
- Redirección de formularios a destinos maliciosos

---

## Recomendaciones de Seguridad

Para mitigar los riesgos identificados se recomienda:

- Implementar **Content-Security-Policy (CSP)** con directivas restrictivas.
- Configurar **X-Frame-Options** o `frame-ancestors` para prevenir Clickjacking.
- Utilizar **Subresource Integrity (SRI)** para validar recursos externos.
- Agregar cabeceras de seguridad adicionales:
  - `X-Content-Type-Options`
  - `Referrer-Policy`
  - `Permissions-Policy`
- Desplegar la aplicación en **HTTPS** con certificado SSL/TLS válido.

---

## Evidencia del Análisis

El informe completo de la auditoría puede consultarse en el siguiente documento:

📄 **Reporte de Auditoría de Seguridad Web**  
`Reporte_Auditoria_Web.pdf`

---

## Nota

Este análisis fue realizado con fines **educativos y de portafolio profesional**.  
La auditoría se ejecutó únicamente sobre un entorno de desarrollo controlado.

---

## Autor

**Jesús Martínez**  
Ingeniero de Sistemas  
Especialización en Seguridad Informática
