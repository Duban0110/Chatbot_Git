🤖 Chatbot API experto en Git y Control de Versiones

Este proyecto es una API REST construida con FastAPI que actúa como un chatbot especializado en Git y control de versiones. Utiliza el modelo Mistral a través de OpenRouter (compatible con la API de OpenAI) para generar respuestas claras y detalladas sobre temas relacionados con Git, ramas, merge, rebase, conflictos, flujos de trabajo y más.
🚀 Requisitos

    Python 3.8 o superior

    Clave API de OpenRouter

    Conexión a internet

🛠 Instalación

    Clona este repositorio o descarga los archivos

    Crea un entorno virtual:

python -m venv venv  

    Activa el entorno virtual:

        Windows: venv\Scripts\activate

        macOS/Linux: source venv/bin/activate

    Instala las dependencias:

pip install -r requirements.txt  

    Crea un archivo .env en la raíz del proyecto con el siguiente contenido:

API_KEY=tu_api_key_de_openrouter  
BASE_URL=https://openrouter.ai/api/v1  

▶ Ejecución

Inicia el servidor local con:

uvicorn main:app --reload  

    API disponible en: http://127.0.0.1:8000

    Documentación interactiva: http://127.0.0.1:8000/docs

📬 Ejemplo de uso

Petición tipo POST a /chat:

{"pregunta": "¿Cuál es la diferencia entre merge y rebase en Git?"}  

Respuesta esperada:

{"respuesta": "El merge une dos ramas conservando su historial, mientras que el rebase reescribe el historial para crear una secuencia lineal..."}  

🐳 Despliegue con Docker

Construcción de imagen:

docker build -t git-chatbot .  

Ejecución del contenedor:

docker run -d -p 8000:8000 --name chatbot --env-file .env git-chatbot  

☁️ Despliegue en Render

    Crea un nuevo Web Service en Render

    Conecta tu repositorio desde GitHub

    Añade las variables de entorno desde .env

    Usa este comando de inicio:

uvicorn main:app --host 0.0.0.0 --port 8000  

📁 Estructura del proyecto

git-chatbot-api/  
├── main.py           # API principal con FastAPI  
├── config.py         # Contiene el PROMPT_SISTEMA específico para Git  
├── .env              # Variables de entorno (no subir a GitHub)  
├── requirements.txt  # Paquetes necesarios  
├── Dockerfile        # Configuración para despliegue con Docker  
└── README.md         # Instrucciones y documentación  

👨‍💻 Autor

Dev. Duban Maruqez

