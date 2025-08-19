# Dependencias del Proyecto
Este documento detalla todas las librerías y dependencias utilizadas en el proyecto "Modelo de Asistencia OyS", tanto en el backend como en el frontend.
---

## 1. Dependencias del Backend (`backend/package.json`)
Estas dependencias son necesarias para que el servidor de Node.js (Express) funcione correctamente. Para instalarlas, navega a la carpeta `backend` y ejecuta:
cd backend
npm install
Use code with caution.
Markdown
## 1.1. Dependencias de Producción (dependencies)
Librería	Versión	Propósito
axios	^1.10.0	Cliente HTTP basado en promesas. Se utiliza para realizar solicitudes a la API de Google AI Studio (Gemini) desde el servidor.
cors	^2.8.5	Middleware de Express para habilitar el Intercambio de Recursos de Origen Cruzado (CORS), permitiendo que el frontend (en localhost:3000) se comunique con el backend (en localhost:5000).
dotenv	^16.4.5	Carga variables de entorno desde un archivo .env a process.env. Es crucial para mantener seguras las API Keys y otras configuraciones sensibles fuera del código fuente.
express	^5.1.0	Framework web minimalista y flexible para Node.js. Se utiliza para crear el servidor, definir rutas (como /api/chat) y manejar las solicitudes HTTP.

## 2. Dependencias del Frontend (frontend/package.json)
Estas dependencias son necesarias para que la aplicación de React funcione. Para instalarlas, navega a la carpeta frontend y ejecuta:
Generated bash
cd frontend
npm install

## 2.1. Dependencias Principales de la Aplicación (dependencies)
Librería	Versión	Propósito
@emotion/react	^11.11.4	Librería de CSS-in-JS requerida por Material-UI para aplicar estilos a los componentes.
@emotion/styled	^11.11.5	Complemento de @emotion/react que permite crear componentes estilizados con la sintaxis de styled-components. Requerido por Material-UI.
@mui/icons-material	^5.16.5	Paquete que proporciona los iconos de Material Design como componentes de React.
@mui/material	^5.16.5	La biblioteca principal de componentes de UI de Material-UI. Proporciona componentes pre-diseñados como Button, TextField, Paper, AppBar, etc.
axios	^1.10.0	Cliente HTTP basado en promesas. Se utiliza para que el frontend se comunique con el backend.
react	^19.1.0	La biblioteca principal para construir interfaces de usuario.
react-dom	^19.1.0	Proporciona los métodos específicos del DOM para React (como ReactDOM.createRoot).
react-markdown	^9.0.1	Componente de React para renderizar texto en formato Markdown a HTML/JSX. Esencial para mostrar las respuestas de la IA con formato (negritas, listas, etc.).
react-router-dom	^6.25.1	Librería para manejar el enrutamiento en la aplicación React. Permite crear una aplicación de página única (SPA) con múltiples "vistas" o "páginas".
react-scripts	5.0.1	Paquete de Create React App que incluye los scripts y configuraciones para iniciar (npm start), compilar (npm build) y probar (npm test) la aplicación.
remark-gfm	^4.0.0	Plugin para react-markdown que añade soporte para GitHub Flavored Markdown (tablas, texto tachado, etc.).
web-vitals	^2.1.4	Una pequeña librería de Google para medir las métricas de rendimiento del sitio web en el mundo real.

## 2.2. Dependencias de Pruebas (@testing-library/*)
Estas dependencias se utilizan para escribir y ejecutar pruebas para los componentes de React. Vienen por defecto con Create React App.
Librería	Versión	Propósito
@testing-library/dom	^10.4.0	Herramientas para consultar y interactuar con el DOM en el entorno de pruebas.
@testing-library/jest-dom	^6.6.3	Proporciona "matchers" personalizados para Jest (ej. toBeInTheDocument()) para hacer las aserciones de prueba más legibles.
@testing-library/react	^16.3.0	La biblioteca principal para probar componentes de React de una manera que se asemeja a cómo los usan los usuarios.
@testing-library/user-event	^13.5.0	Simula eventos de usuario (clics, escritura) de forma más realista que los eventos de simulación nativos.