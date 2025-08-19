# Modelo de Asistencia OyS

Una aplicación de chat full-stack inteligente que utiliza el stack MERN (MongoDB, Express, React, Node.js) y se integra con la API de Google Gemini para proporcionar análisis conversacional y de documentos.

## Características

-   **Interfaz Moderna:** Construida con React y Material-UI, con modo claro/oscuro.
-   **Autenticación Segura:** Sistema de registro e inicio de sesión con tokens JWT. Cada usuario tiene sus propias conversaciones privadas.
-   **Persistencia en la Nube:** Todas las conversaciones se almacenan en una base de datos MongoDB Atlas.
-   **Análisis de Documentos (RAG):** Soporte para subir archivos `.pdf`, `.docx`, y `.txt` para realizar preguntas contextuales sobre su contenido.
-   **IA Conversacional:** Integración con Google Gemini para respuestas inteligentes.

---

## Stack Tecnológico

| Área     | Tecnología                      | Propósito                               |
| :------- | :------------------------------ | :-------------------------------------- |
| **Backend**  | Node.js, Express.js             | Servidor y API REST                     |
|          | MongoDB, Mongoose               | Base de datos NoSQL y modelado de datos |
|          | JWT, Bcrypt.js                  | Autenticación y seguridad de contraseñas |
|          | Multer, Mammoth, pdf-parse      | Gestión y lectura de archivos           |
| **Frontend** | React                           | Biblioteca de interfaz de usuario       |
|          | React Router                    | Enrutamiento                            |
|          | Axios                           | Peticiones HTTP                         |
|          | Material-UI (MUI)               | Biblioteca de componentes de UI         |
|          | React-Markdown, React-Dropzone  | Renderizado y subida de archivos        |

---

## Guía de Instalación y Ejecución

### Requisitos Previos
-   Node.js (v16+)
-   npm (v8+)
-   Una cuenta gratuita de [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
-   Una API Key de [Google AI Studio (Gemini)](https://aistudio.google.com/).

### 1. Configuración del Backend

1.  Navega a la carpeta del backend:
    ```
    cd backend
    ```
2.  Instala las dependencias:
    ```
    npm install
    ```
3.  Crea un archivo `.env` en la raíz de `/backend` y configúralo basándote en el siguiente ejemplo:
    ```env
    PORT=5000
    GOOGLE_AI_STUDIO_API_KEY=AIzaSyBPZWCiiz9RERUEk-IEgOR-GP7LfjLYGUA
    GOOGLE_AI_STUDIO_URL=https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent   
    GOOGLE_SHEET_ID=14LBP8tXv1eL2aIiDUblQhpnkfL1ZhAS2AjAcRi3i1Jw
    SERVICE_ACCOUNT_FILE_PATH=credentials.json # Mantén esta si no ha cambiado
    MONGO_URI=mongodb+srv://kevinsohe:Krsh2001.@asistenciaoys-project.lnmz2hy.mongodb.net/AsistenciaOySDB?retryWrites=true&w=majority&appName=AsistenciaOyS-Project
    JWT_SECRET=Krsh2001.
    ```
4.  Inicia el servidor en modo de desarrollo (se reinicia con los cambios):
    ```
    npm run dev
    ```
    El servidor estará escuchando en `http://localhost:5000`.

### 2. Configuración del Frontend

1.  Abre una **nueva terminal** y navega a la carpeta del frontend:
    ```
    cd frontend
    ```
2.  Instala las dependencias:
    ```
    npm install
    ```
3.  Inicia la aplicación de React:
    ```
    npm start
    ```
    La aplicación se abrirá automáticamente en tu navegador en `http://localhost:3000`.

    *Proyecto desarrollado por Kevin Rodrigo Soto Herrera.*
    