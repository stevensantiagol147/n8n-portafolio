# 📊 Proyecto 2: Extracción de datos desde API y guardado en Google Sheets

Este workflow de n8n realiza una automatización sencilla pero poderosa: obtiene datos desde una API pública y los guarda automáticamente en una hoja de cálculo de Google Sheets. Es útil para recopilar información periódica, hacer reportes o alimentar dashboards.

---

## ⚙️ Descripción del workflow

El flujo de trabajo contiene dos nodos:

1. **HTTP Request (Obtener datos de API)**  
   - Realiza una solicitud GET a `https://jsonplaceholder.typicode.com/posts`, una API pública que devuelve datos simulados tipo blog post.
   - El formato de respuesta es JSON.

2. **Google Sheets (Guardar datos)**  
   - Inserta los datos obtenidos en una hoja de cálculo de Google Sheets.
   - Usa el modo `autoMapInputData` para mapear automáticamente los campos del JSON a columnas.
   - Requiere autenticación OAuth2 y el ID de la hoja de cálculo.

---

## 📥 Cómo importar el workflow en n8n

1. Abrir tu instancia de n8n.
2. Ve a Workflows → "Import from file".
3. Selecciona el archivo `workflow-api-to-google-sheets.json`.
4. Configura el nodo de Google Sheets:
   - Autenticación OAuth2 con tu cuenta de Google.
   - Reemplaza `"TU_ID_DE_HOJA"` por el ID real de tu hoja de cálculo.
   - Asegúrate de que la hoja tenga una pestaña llamada `Sheet1`.

---

## 🧪 Recomendaciones

- Puedes cambiar la URL del nodo HTTP para conectarte a cualquier otra API.
- Si la API devuelve muchos campos, asegúrate de que la hoja de cálculo tenga columnas suficientes.
- Este workflow puede combinarse con un nodo de tiempo (cron) para ejecutarse automáticamente cada día o semana.

---

## 📁 Archivos incluidos

- `workflow-api-to-google-sheets.json`: El archivo del flujo de trabajo.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por Steven Santiago Lopez como parte de un portafolio de automatización con n8n.
