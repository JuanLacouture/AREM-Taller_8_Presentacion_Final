# 📄 **Resumen Ejecutivo del Proyecto Arquitectónico — Taller 8 y Entrega Final**

**Integrantes:**  
- **Valentina Rodríguez**  
- **Juan Lacoutture**

---

## 🏢 **Nombre del Cliente**
**Compulens – Laboratorio Óptico**

---

## 🎯 **Objetivo General del Proyecto**

El objetivo del proyecto fue **analizar, modelar y rediseñar la arquitectura empresarial** del proceso de toma, registro y fabricación de pedidos ópticos para Compulens. Se buscó **identificar fallas operativas, riesgos de seguridad, brechas de integración y oportunidades de automatización**, proponiendo una **arquitectura TO-BE escalable, segura y estandarizada** que mejore la trazabilidad, reduzca errores manuales y modernice la operación mediante automatización, chatbot OCR, integración con ERP Ocular y servicios digitales.

---

## 🧱 **Vistas Arquitectónicas Cubiertas**

| Vista | Alcance de la Solución |
|------|--------------------------|
| **Procesos de Negocio** | Modelos AS-IS del flujo actual (WhatsApp, llamadas, recepción física) y BPMN TO-BE con chatbot OCR, validación automática y facturación DIAN. |
| **Información / Datos** | Modelo ER TO-BE incluyendo entidades de cliente, pedido, detalle, producción y materia prima con trazabilidad INVIMA. |
| **Aplicaciones / Sistemas** | Arquitectura Capa Cliente – Aplicación de Pedidos – Integración – ERP – Bodega – Producción. Nuevo backend unificado y orquestación vía API Gateway. |
| **Infraestructura** | Diagrama de borde, CDN, WAF, API Gateway, backend de pedidos, bases de datos SQL, monitoreo (SIEM) y sistemas externos. |
| **Seguridad** | Análisis STRIDE por actor y componente (cliente, administración, ERP, bodega, mensajería). Controles propuestos: MFA, WAF, hardening del ERP, segregación de roles, logs y backups seguros. |
| **Cumplimiento Normativo** | Checklist de Ley 1581 (datos personales), INVIMA, facturación electrónica DIAN, ISO 27001 Anexo A (accesos, trazabilidad, continuidad, registro de eventos). |

---

## 🧩 **Hallazgos Clave**

- ❗ **Dependencia excesiva de canales informales (WhatsApp, llamadas, papel)** con alto riesgo de pérdida, manipulación o errores manuales.  
- 🔄 **Duplicidad de registro** (call center, recepción, ERP) que genera inconsistencias entre pedido y producción.  
- 🔐 **Brechas de seguridad** en el proceso AS-IS: suplantación, alteración de órdenes, fuga de datos, manipulación de inventario y privilegios excesivos.  
- 📦 **Inventario y trazabilidad INVIMA poco integrados**, afectando control de lotes y disponibilidad.  
- 📌 **Ausencia de notificaciones automáticas** para clientes y jefes de producción, generando retrasos y reprocesos.  
- 📤 **Ausencia de un canal digital oficial** para recepción estructurada de pedidos.

---

## 🚀 **Recomendaciones Principales**

- Implementar **chatbot con OCR** para digitalizar órdenes desde WhatsApp y eliminar reprocesos manuales.  
- Centralizar todos los pedidos en una **Aplicación de Pedidos** con orquestador y API segura al ERP Ocular.  
- Aplicar controles STRIDE:  
  - ✔ MFA para usuarios internos  
  - ✔ WAF + CDN para canal público  
  - ✔ Segregación de roles en ERP y Producción  
  - ✔ Auditoría continua y SIEM para monitoreo  
- Integrar **validación automática de fórmula, cliente y historia del lente** antes de registrar en ERP.  
- Implementar **notificaciones automáticas** de estados (recibido, validado, en producción, factura emitida).  
- Modernizar el flujo de materia prima con **verificación digital de stock, lote e INVIMA**.  
- Desplegar arquitectura en entornos separados (DEV/QA/PROD) con políticas de seguridad y backups.

---

## 💡 **Reflexión Final**

El trabajo permitió aplicar de manera integral los principios de arquitectura empresarial, pasando desde el levantamiento AS-IS real hasta un diseño TO-BE robusto, seguro y escalable. Se ejercieron habilidades en **modelado BPMN, arquitectura lógica, diseño de datos, análisis STRIDE, documentación ejecutiva y diseño de soluciones digitales**, entregando una propuesta aplicable al negocio real de Compulens y alineada con buenas prácticas profesionales.

---

_Listo para entregar en el informe final del Taller 8 y la Entrega Final de Arquitectura Empresarial._
