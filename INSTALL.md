# Guía de Instalación y Configuración para "Modelo de Asistencia OyS"

Este documento proporciona una guía detallada paso a paso para configurar el entorno de desarrollo y ejecutar el proyecto en un sistema operativo Windows.

---

## 1. Requisitos Previos de Software

Antes de descargar el proyecto, es **esencial** tener el siguiente software instalado y configurado correctamente.

### 1.1. Node.js y npm
-   **Instalación:**
    1.  Ve a la página oficial: [https://nodejs.org/](https://nodejs.org/)
    2.  Descarga la versión **LTS (Long-Term Support)**.
    3.  Ejecuta el instalador aceptando las opciones por defecto.
-   **Verificación:**
    Abre una nueva terminal (CMD o PowerShell) y ejecuta `node -v` y `npm -v`. Deberías ver los números de versión.

### 1.2. Git
-   **Instalación:**
    1.  Ve a la página oficial: [https://git-scm.com/downloads](https://git-scm.com/downloads)
    2.  Al instalar, en la pantalla "Adjusting your PATH environment", selecciona la opción recomendada: **"Git from the command line and also from 3rd-party software"**.
-   **Verificación:**
    Abre una nueva terminal y ejecuta `git --version`.

### 1.3. Editor de Código
-   Se recomienda **Visual Studio Code**: [https://code.visualstudio.com/](https://code.visualstudio.com/)

### 1.4. Cuentas de Servicios Externos
-   **MongoDB Atlas:** Necesitarás una cuenta gratuita para la base de datos. Crea un clúster, un usuario de base de datos (anota **usuario** y **contraseña**) y obtén tu **cadena de conexión (URI)**.
-   **Google AI Studio:** Necesitarás una **API Key** para el modelo Gemini.

---

## 2. Configuración del Proyecto

### 2.1. Obtener el Código
Clona el repositorio en una carpeta de tu elección:
```bash
git clone https://github.com/Kevinsohe/modelo-asistencia-oys.git
cd modelo-asistencia-oys
```

### 2.2. Configurar Variables de Entorno (Paso Clave)
1.  Navega a la carpeta `backend`.
2.  Crea un nuevo archivo llamado `.env`.
3.  Copia y pega la siguiente plantilla y rellena tus credenciales:
    ```env
    # Puerto del servidor
    PORT=5000

    # Cadena de conexión de MongoDB Atlas
    MONGO_URI=mongodb+srv://<TU_USUARIO>:<TU_PASSWORD>@tu_cluster...

    # Secreto para JWT
    JWT_SECRET=UN_SECRETO_ALEATORIO_Y_LARGO

    # Credenciales de Google AI
    GOOGLE_AI_STUDIO_API_KEY=tu_api_key_de_gemini
    GOOGLE_AI_STUDIO_URL=https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent
    ```
    **Importante:** Reinicia el servidor del backend cada vez que modifiques este archivo.

---

## 3. Instalación de Dependencias y Solución de Errores

### 3.1. Solucionar Error de Scripts de PowerShell (Si ocurre)
Este es un error común en Windows.
1.  Abre **PowerShell como Administrador**.
2.  Ejecuta: `Set-ExecutionPolicy RemoteSigned`
3.  Confirma con `S` y Enter. Cierra la ventana.

### 3.2. Instalar Librerías
1.  **Backend:**
    ```bash
    cd backend
    npm install
    ```
2.  **Frontend:**
    ```bash
    cd ../frontend
    npm install
    ```

---

## 4. Ejecutar la Aplicación

Necesitarás **dos terminales abiertas**.

1.  **Terminal 1 (Backend):**
    ```bash
    cd backend
    npm run dev
    ```
2.  **Terminal 2 (Frontend):**
    ```bash
    cd frontend
    npm start
    ```
La aplicación se abrirá en `http://localhost:3000`.