# Proyecto Parcial - API con FastAPI y Google Gemini

## Descripción

Este proyecto es una aplicación web simple construida con FastAPI que integra la API de Google Gemini para generar contenido basado en prompts proporcionados por el usuario. El endpoint principal permite enviar un prompt y recibir una respuesta generada por el modelo de IA Gemini.

## Características

- API RESTful utilizando FastAPI
- Integración con Google Gemini para generación de contenido
- Soporte para variables de entorno mediante dotenv
- Servidor ASGI con Uvicorn

## Instalación

1. Clona este repositorio:
   ```
   git clone <url-del-repositorio>
   cd proyectoParcial
   ```

2. Crea un entorno virtual (opcional pero recomendado):
   ```
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. Instala las dependencias:
   ```
   pip install -r requirements.txt
   ```

4. Configura las variables de entorno:
   - Crea un archivo `.env` en la raíz del proyecto
   - Agrega tu clave API de Google Gemini:
     ```
     GEMINI_API_KEY=tu_clave_api_aqui
     ```

## Uso

1. Ejecuta la aplicación:
   ```
   uvicorn main:app --reload
   ```

2. La API estará disponible en `http://127.0.0.1:8000`

3. Accede a la documentación automática de FastAPI en `http://127.0.0.1:8000/docs`

## API Endpoints

### GET /llm/{prompt}

Genera contenido basado en el prompt proporcionado.

- **Parámetros:**
  - `prompt` (string): El texto del prompt para el modelo Gemini

- **Respuesta:**
  ```json
  {
    "Respuesta": "Texto generado por Gemini"
  }
  ```

**Ejemplo de uso:**
```
curl "http://127.0.0.1:8000/llm/Cuéntame una historia corta"
```

## Dependencias

Las dependencias principales se listan en `requirements.txt`:

- FastAPI: Framework web para APIs
- google-genai: Cliente para Google Gemini
- python-dotenv: Gestión de variables de entorno
- Uvicorn: Servidor ASGI

## Contribución

Si deseas contribuir a este proyecto, por favor crea un fork y envía un pull request.

## Licencia

Este proyecto está bajo la Licencia MIT.