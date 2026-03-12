AI WhatsApp Agent: Atención Automatizada para Feriantes 🎡🤖
Este proyecto implementa un agente de inteligencia artificial autónomo que gestiona consultas de WhatsApp para la comunidad de emprendedores de "La Soberana". Utiliza un stack self-hosted para garantizar la privacidad y el control total de los datos.

<img width="842" height="304" alt="image" src="https://github.com/user-attachments/assets/67852d35-252e-4b72-b8c3-ccd0795fcc40" />


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
<img width="460" height="595" alt="image" src="https://github.com/user-attachments/assets/32064cf5-7f2d-4905-8491-a6a3f4cd9e76" />

Nodo IF (Seguridad): Valida que el mensaje sea entrante, de un chat individual y no un estado del sistema.
<img width="459" height="616" alt="image" src="https://github.com/user-attachments/assets/0b50c3eb-9960-4163-bca4-02ef486f7d0a" />

Edit Fields: Limpia y estructura el chatId y el mensaje_usuario para el agente.
<img width="620" height="593" alt="image" src="https://github.com/user-attachments/assets/0a3e6401-60ec-4927-a74c-dc7206e4c931" />

AI Agent + Memory: El corazón del flujo; procesa la consulta manteniendo el contexto de la conversación previa.
<img width="595" height="539" alt="image" src="https://github.com/user-attachments/assets/6c6f69da-0388-4462-8e41-52031a8c1fc6" />

HTTP Request: Envía la respuesta final de vuelta al usuario vía WAHA.
<img width="599" height="762" alt="image" src="https://github.com/user-attachments/assets/077280a8-5655-4339-ae4f-4813b08de650" />


📝 Ejemplo de Configuración del Agente
El sistema utiliza un System Prompt personalizado para mantener un tono amable y profesional, asegurando que los feriantes reciban información precisa sobre inscripciones y logística.
