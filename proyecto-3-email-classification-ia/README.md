# 📬 Proyecto 5: Clasificación de correos con IA y almacenamiento en Google Sheets

Este workflow automatiza la recepción de correos electrónicos, analiza su contenido utilizando inteligencia artificial (OpenAI) y guarda los resultados en una hoja de cálculo de Google Sheets. Es ideal para equipos que reciben correos de soporte, ventas o consultas generales y desean clasificarlos automáticamente.

---

## ⚙️ Descripción del workflow

El flujo de trabajo incluye tres nodos principales:

1. **IMAP Email Trigger (Recibir correo)**  
   - Se conecta a una cuenta de correo vía IMAP.  
   - Detecta nuevos correos en la bandeja de entrada.  
   - Extrae el asunto y el cuerpo del mensaje.

2. **OpenAI (Clasificar con IA)**  
   - Utiliza el modelo `gpt-3.5-turbo` para analizar el contenido del correo.  
   - Clasifica el mensaje como "soporte", "ventas" o "spam" según el texto.

3. **Google Sheets (Guardar resultado)**  
   - Registra el asunto del correo y su clasificación en una hoja de cálculo.  
   - Usa el modo `defineBelow` para mapear los campos manualmente.

---

## 🧪 Requisitos

- Credenciales IMAP configuradas en n8n.
- Cuenta de OpenAI con acceso a la API.
- Hoja de cálculo de Google Sheets con permisos de escritura y credenciales OAuth2 activas.
- Pestaña llamada `Sheet1` con columnas para "Asunto" y "Clasificación".

---

## 📥 Cómo importar el workflow

1. Abre tu instancia de n8n.
2. Ve a **Workflows → Import from file**.
3. Selecciona el archivo `workflow-email-classification-ai.json`.
4. Configura tus credenciales en los tres nodos:
   - IMAP para el correo.
   - OpenAI para la clasificación.
   - Google Sheets para el almacenamiento.

---

## 🧠 Personalización

- Puedes modificar el prompt del nodo OpenAI para usar otras categorías o idiomas.
- Agrega un nodo `Cron` si deseas ejecutar el flujo cada cierto tiempo.
- Integra con otros servicios como Notion, Airtable o bases de datos SQL si prefieres otro destino.

---

## 📁 Archivos incluidos

- `workflow-email-classification-ai.json`: El archivo del flujo de trabajo.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por Steven Santiago Lopez como parte del portafolio de automatización con n8n.
