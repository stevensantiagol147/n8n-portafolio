# 🧲 Proyecto 8: Enriquecimiento de Leads + Validación + Segmentación + Alerta + Almacenamiento

Este workflow avanzado automatiza la recepción de leads desde un formulario web, los enriquece con datos externos, valida su integridad, los segmenta por industria y prioridad, y los guarda en múltiples plataformas mientras envía alertas personalizadas. Es ideal para equipos de ventas que desean trabajar con información más completa y segmentada desde el primer contacto.

---

## ⚙️ Descripción del workflow

Este flujo incluye 10 nodos:

1. **Webhook (Recibir Lead)**  
   - Recibe datos desde un formulario web: nombre, correo, empresa, industria, prioridad.

2. **Set Node (Normalizar campos)**  
   - Limpia y estandariza los campos clave como correo y empresa.

3. **HTTP Request (Enriquecer con API externa)**  
   - Consulta una API como Clearbit para obtener información adicional del lead.

4. **Merge Node (Combinar datos)**  
   - Une los datos originales con los enriquecidos.

5. **IF Node (Validar datos)**  
   - Verifica que el correo y la empresa estén presentes.

6. **IF Node (Segmentar por industria)**  
   - Clasifica el lead según su industria: tecnología, salud o educación.

7. **IF Node (Segmentar por prioridad)**  
   - Evalúa si el lead es de prioridad alta, media o baja.

8. **Google Sheets (Guardar lead)**  
   - Inserta el lead en una hoja de cálculo para seguimiento.

9. **Notion (Guardar lead en base de datos)**  
   - Crea una entrada en una base de datos de Notion con los datos del lead.

10. **Telegram (Enviar alerta personalizada)**  
   - Envía una notificación al equipo con los datos clave del lead.

---

## 🧪 Requisitos

- Formulario web que envíe datos a n8n vía Webhook.
- API externa como Clearbit o Similar para enriquecimiento.
- Hoja de cálculo de Google Sheets con credenciales OAuth2 activas.
- Base de datos en Notion con propiedades configuradas.
- Cuenta de Telegram con credenciales configuradas en n8n.

---

## 📥 Cómo importar el workflow

1. Abre tu instancia de n8n.
2. Ve a **Workflows → Import from file**.
3. Selecciona el archivo `workflow-leads-enriquecimiento-validacion.json`.
4. Configura:
   - El Webhook en tu formulario.
   - Las credenciales de Clearbit, Google Sheets, Notion y Telegram.
   - Los IDs de hoja, base de datos y chat según tu entorno.

---

## 🧠 Personalización

- Puedes agregar más industrias o niveles de prioridad.
- Cambia el destino de almacenamiento a Airtable, HubSpot o bases SQL.
- Integra con calendarios o CRM para asignar automáticamente el lead a un vendedor.

---

## 📁 Archivos incluidos

- `workflow-leads-enriquecimiento-validacion.json`: El archivo del flujo de trabajo.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por Steven Santiago Lopez como parte del portafolio de automatización con n8n.
