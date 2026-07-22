# agente-soporte-n8n
# 🤖 Agente de IA para Gestión Automática de Tickets de Soporte

## 📌 Descripción del Proyecto
Este flujo de trabajo en **n8n** utiliza un **Agente de IA (Tools Agent)** integrado con **OpenAI (GPT-4o)** para procesar solicitudes de soporte de usuarios recibidas por chat, registrar automáticamente los datos en **Google Sheets** y enviar un correo electrónico de confirmación vía **Gmail**.

---

## 🛠️ Arquitectura del Flujo de Trabajo
El flujo consta de los siguientes nodos principales:
1. **When Chat Message is Received:** Desencadenador nativo de chat que captura la entrada del usuario.
2. **AI Agent (Tools Agent):** Nodo de razonamiento que procesa el texto, extrae entidades (*nombre*, *correo*, *falla*) y decide qué herramientas ejecutar.
3. **OpenAI Chat Model:** Modelo de lenguaje encargado del procesamiento conversacional.
4. **Google Sheets (Append Row):** Herramienta conectada al agente con mapeo automático de campos para almacenar los tickets de soporte.
5. **Gmail (Send Message):** Envía la notificación y confirmación del ticket al usuario final.

---

## 🚀 Instrucciones de Ejecución
1. Clonar este repositorio o descargar el archivo `punto_de_control1_miguel_tovar.json`.
2. En n8n, crear un nuevo workflow y seleccionar **Import from File**.
3. Configurar las credenciales para **OpenAI**, **Google Sheets** y **Gmail**.
4. Abrir la ventana de chat e ingresar una solicitud de soporte.

---

## 📸 Evidencias de Funcionamiento
* **Flujo Ejecutado en n8n:**
  ![Flujo n8n](n8n_flow.png)
* **Registro en Google Sheets:**
  ![Google Sheets](sheets_record.png)
* **Confirmación por Gmail:**
  ![Correo Gmail](gmail_confirmation.png)
