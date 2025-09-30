# 🧲 Proyecto 5: Captura de Leads desde Google Maps + Envío a Google Sheets

Este workflow automatiza la captura de leads comerciales desde Google Maps utilizando Apify y guarda los datos en una hoja de cálculo de Google Sheets. Es ideal para equipos de ventas, marketing o prospección que desean construir listas de negocios locales.

---

## ⚙️ Descripción del workflow

1. **HTTP Request (Apify)**  
   - Consulta un dataset generado por Apify con resultados de búsqueda en Google Maps.  
   - Extrae nombre, teléfono, correo y dirección de cada negocio.

2. **Google Sheets (Guardar leads)**  
   - Inserta cada lead en una hoja de cálculo con columnas personalizadas.  
   - Usa el modo `defineBelow` para mapear los campos manualmente.

---

## 🧪 Requisitos

- Cuenta en [Apify](https://apify.com/) con un actor que scrapee Google Maps.
- Dataset ID y token de Apify configurados en el nodo HTTP.
- Hoja de cálculo de Google Sheets con permisos de escritura y credenciales OAuth2 activas.
- Pestaña llamada `Sheet1` con columnas: Nombre, Teléfono, Email, Dirección.

---

## 📥 Cómo importar el workflow

1. Abre tu instancia de n8n.
2. Ve a **Workflows → Import from file**.
3. Selecciona el archivo `workflow-leads-googlemaps-sheets.json`.
4. Configura tus credenciales y reemplaza:
   - `TU_DATASET_ID` y `TU_TOKEN` en el nodo HTTP.
   - `TU_ID_DE_HOJA` en el nodo Google Sheets.

---

## 🧠 Personalización

- Puedes agregar un nodo `IF` para filtrar leads incompletos.
- Agrega un nodo `Telegram` o `Email` para recibir alertas de nuevos leads.
- Integra con CRM como HubSpot, Zoho o Airtable si deseas enviar los leads directamente.

---

## 📁 Archivos incluidos

- `workflow-leads-googlemaps-sheets.json`: El archivo del flujo de trabajo.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por Steven Santiago Lopez como parte del portafolio de automatización con n8n.
