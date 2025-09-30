# 🧲 Proyecto 6: Captura de Leads desde formulario web + validación + almacenamiento

Este workflow automatiza la recepción de leads desde un formulario web, valida que tengan correo y teléfono, y guarda los datos en Google Sheets solo si están completos. Es ideal para equipos de ventas que desean filtrar contactos antes de almacenarlos.

---

## ⚙️ Descripción del workflow

1. **Webhook (Recibir Lead)**  
   - Escucha envíos desde un formulario web.  
   - Recibe nombre, correo, teléfono y mensaje.

2. **IF Node (Validar datos)**  
   - Verifica que el correo y teléfono no estén vacíos.  
   - Si están completos, continúa el flujo.  
   - Si faltan datos, se descarta el lead.

3. **Set Node (Formatear datos)**  
   - Organiza los campos para el destino final.

4. **Google Sheets (Guardar lead)**  
   - Inserta el lead en una hoja de cálculo.  
   - Usa `autoMapInputData` para asignar los campos automáticamente.

---

## 🧪 Requisitos

- Formulario web que envíe datos a n8n vía Webhook (ej. Typeform, HTML personalizado).
- Hoja de cálculo de Google Sheets con permisos de escritura y credenciales OAuth2 activas.
- Pestaña llamada `Sheet1` con columnas: Nombre, Correo, Teléfono, Mensaje.

---

## 📥 Cómo importar el workflow

1. Abre tu instancia de n8n.
2. Ve a **Workflows → Import from file**.
3. Selecciona el archivo `workflow-leads-validation-storage.json`.
4. Configura:
   - El Webhook en tu formulario.
   - El ID de tu hoja de cálculo en Google Sheets.

---

## 🧠 Personalización

- Puedes agregar un nodo `Telegram` o `Email` para recibir alertas de nuevos leads válidos.
- Integra con CRM como HubSpot, Zoho o Airtable si deseas enviar los leads directamente.
- Agrega lógica adicional para validar dominios de correo o números de teléfono.

---

## 📁 Archivos incluidos

- `workflow-leads-validation-storage.json`: El archivo del flujo de trabajo.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por Steven Santiago Lopez como parte del portafolio de automatización con n8n.
