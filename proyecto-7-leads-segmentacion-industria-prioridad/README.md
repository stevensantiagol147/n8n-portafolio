# 🧲 Proyecto 7: Segmentación de Leads por industria y prioridad + almacenamiento + alerta

Este workflow automatiza la recepción de leads desde un formulario web, valida que tengan datos completos, los segmenta por industria y prioridad, los guarda en Google Sheets y envía alertas por Telegram. Es ideal para equipos de ventas que desean clasificar y priorizar contactos automáticamente.

---

## ⚙️ Descripción del workflow

1. **Webhook (Recibir Lead)**  
   - Recibe datos desde un formulario web: nombre, correo, industria, prioridad, mensaje.

2. **IF Node (Validar datos)**  
   - Verifica que el correo y la industria estén presentes.

3. **IF Node (Segmentar por industria)**  
   - Divide el flujo en tres ramas: tecnología, salud, educación.

4. **IF Node (Segmentar por prioridad)**  
   - Dentro de cada industria, evalúa si el lead es de prioridad alta, media o baja.

5. **Google Sheets (Guardar lead)**  
   - Guarda el lead en una hoja específica según industria y prioridad.

6. **Telegram (Enviar alerta)**  
   - Envía una alerta personalizada con los datos del lead.

---

## 🧪 Requisitos

- Formulario web que envíe datos a n8n vía Webhook.
- Hoja de cálculo de Google Sheets con permisos de escritura y credenciales OAuth2 activas.
- Cuenta de Telegram con credenciales configuradas en n8n.
- Chat ID del canal o usuario donde se enviará la alerta.

---

## 📥 Cómo importar el workflow

1. Abre tu instancia de n8n.
2. Ve a **Workflows → Import from file**.
3. Selecciona el archivo `workflow-leads-segmentacion-industria.json`.
4. Configura:
   - El Webhook en tu formulario.
   - El ID de tu hoja de cálculo.
   - Las credenciales de Telegram y el Chat ID.

---

## 🧠 Personalización

- Puedes agregar más industrias o niveles de prioridad.
- Cambia el destino de almacenamiento a Notion, Airtable o CRM.
- Agrega lógica adicional para validar dominios de correo o números de teléfono.

---

## 📁 Archivos incluidos

- `workflow-leads-segmentacion-industria.json`: El archivo del flujo de trabajo.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por Steven Santiago Lopez como parte del portafolio de automatización con n8n.
