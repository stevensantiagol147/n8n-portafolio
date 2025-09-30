# 📧 Proyecto 1: Automatización de correo diario con n8n

Este proyecto utiliza n8n para enviar automáticamente un correo electrónico todos los días a las 9:00 AM. Es ideal para recordatorios, notificaciones o cualquier mensaje recurrente.

---

## ⚙️ Descripción del workflow

El flujo de trabajo contiene dos nodos:

1. **Trigger de tiempo (Cron)**  
   - Configurado para activarse todos los días a las 9:00 AM usando la expresión `0 9 * * *`.

2. **Nodo de envío de correo (Email Send)**  
   - Envía un correo desde `stevensantiagol147@gmail.com` a un destinatario definido.
   - El asunto del correo es "Recordatorio diario".
   - El cuerpo del mensaje es:  
     `"Hola, este es tu recordatorio diario enviado automáticamente por n8n."`

---

## 📥 Cómo importar el workflow en n8n

1. Abrir tu instancia de n8n.
2. Ve al menú de Workflows → "Import from file".
3. Selecciona el archivo `workflow.json` incluido en este repositorio.
4. Configura las credenciales SMTP o Gmail para el nodo de correo:
   - Si usas Gmail, necesitarás una contraseña de aplicación (App Password).
   - También puedes usar otro proveedor SMTP si lo prefieres.

---


## 📁 Archivos incluidos

- `workflow.json`: El archivo del flujo de trabajo para importar en n8n.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por steven santiago lopez como parte de un portafolio de automatización con n8n.
