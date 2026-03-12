AI WhatsApp Agent: Atención Automatizada para Feriantes 🎡🤖
Este proyecto implementa un agente de inteligencia artificial autónomo que gestiona consultas de WhatsApp para la comunidad de emprendedores de "La Soberana". Utiliza un stack self-hosted para garantizar la privacidad y el control total de los datos.

🚀 Funcionalidades Clave
Procesamiento de Lenguaje Natural: Respuestas inteligentes generadas por Ollama (IA Local).

Filtro Anti-Bucle y Grupos: Lógica avanzada para ignorar mensajes propios y evitar responder en grupos de WhatsApp.

Infraestructura Robusta: Orquestación total mediante n8n corriendo en contenedores Docker.

🛠️ Stack Tecnológico
n8n: El motor de automatización que conecta todos los nodos.

Ollama: Modelo de lenguaje (LLM) ejecutado localmente para procesar las consultas.

WAHA (WhatsApp HTTP API): Bridge para la comunicación programática con WhatsApp.

Docker: Entorno donde conviven todos los servicios.

⚙️ Arquitectura del Workflow
Webhook: Recibe en tiempo real los eventos de WAHA.

Nodo IF (Seguridad): Valida que el mensaje sea entrante, de un chat individual y no un estado del sistema.

Edit Fields: Limpia y estructura el chatId y el mensaje_usuario para el agente.

AI Agent + Memory: El corazón del flujo; procesa la consulta manteniendo el contexto de la conversación previa.

HTTP Request: Envía la respuesta final de vuelta al usuario vía WAHA.

📝 Ejemplo de Configuración del Agente
El sistema utiliza un System Prompt personalizado para mantener un tono amable y profesional, asegurando que los feriantes reciban información precisa sobre inscripciones y logística.
