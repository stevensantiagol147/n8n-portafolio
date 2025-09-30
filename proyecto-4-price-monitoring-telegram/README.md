# 📦 Proyecto 4: Monitoreo de precios con alerta por Telegram

Este workflow de n8n permite monitorear el precio de un producto desde una API y enviar una alerta automática por Telegram si el precio baja de un umbral definido. Es ideal para seguimiento de ofertas, productos favoritos o alertas de compra.

---

## ⚙️ Descripción del workflow

El flujo de trabajo incluye cuatro nodos:

1. **Cron Diario**  
   - Ejecuta el flujo automáticamente todos los días a las 8:00 a.m.

2. **HTTP Request (Consultar precio)**  
   - Realiza una solicitud GET a una API que devuelve el precio actual de un producto.

3. **IF Node (Verificar precio)**  
   - Compara el precio obtenido con un valor umbral (ej. $100).  
   - Si el precio es menor, continúa el flujo.

4. **Telegram (Enviar alerta)**  
   - Envía un mensaje al canal o usuario de Telegram con el precio actual y el enlace al producto.

---

## 🧪 Requisitos

- API pública o privada que devuelva el precio del producto en formato JSON.
- Cuenta de Telegram con credenciales configuradas en n8n.
- Chat ID del canal o usuario donde se enviará la alerta.
- Ajuste del umbral de precio según tus necesidades.

---

## 📥 Cómo importar el workflow

1. Abre tu instancia de n8n.
2. Ve a **Workflows → Import from file**.
3. Selecciona el archivo `workflow-price-monitoring-telegram.json`.
4. Configura los siguientes valores:
   - URL de la API en el nodo "Consultar precio".
   - Valor umbral en el nodo "Verificar precio".
   - Chat ID y credenciales en el nodo "Enviar alerta Telegram".

---

## 🧠 Personalización

- Puedes cambiar la frecuencia del nodo Cron para ejecutarlo cada hora, semana o mes.
- Agrega múltiples productos usando nodos adicionales o bucles.
- Integra con otras plataformas como Slack, Discord o correo electrónico si prefieres otro canal de alerta.

---

## 📁 Archivos incluidos

- `workflow-price-monitoring-telegram.json`: El archivo del flujo de trabajo.
- `README.md`: Este documento explicativo.

---

## 🧠 Créditos

Creado por Steven Santiago Lopez como parte del portafolio de automatización con n8n.
