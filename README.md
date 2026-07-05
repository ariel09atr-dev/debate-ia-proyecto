# Debate IA

Este proyecto implementa un sistema de debate entre modelos de inteligencia artificial. Tres modelos de IA debaten en privado sobre una pregunta, y un cuarto modelo sintetiza la respuesta final para el usuario. El debate interno no se muestra en la interfaz de usuario, solo la respuesta final consolidada.

## Características

*   **Debate Interno de IAs**: Utiliza múltiples modelos de lenguaje para generar respuestas más robustas y matizadas.
*   **Ofuscación de Código**: El código fuente principal (`app.py`) ha sido ofuscado para proteger la propiedad intelectual, manteniendo la funcionalidad completa.
*   **Protección de API Key**: La clave de API se gestiona a través de variables de entorno (`.env`) para asegurar que no se exponga en el código fuente ni en el repositorio público.

## Configuración y Ejecución

Sigue estos pasos para configurar y ejecutar el proyecto localmente:

### 1. Clonar el Repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
cd debate-ia
```

### 2. Instalar Dependencias

Este proyecto requiere Python 3 y las librerías listadas en `requirements.txt`. Instálalas usando pip:

```bash
pip install -r requirements.txt
```

### 3. Configurar la API Key de OpenRouter

El proyecto utiliza la API de OpenRouter. Necesitarás una clave de API válida. Sigue estos pasos para configurarla:

1.  Copia el archivo `.env.example` a `.env`:

    ```bash
    cp .env.example .env
    ```

2.  Abre el archivo `.env` recién creado y reemplaza `tu_clave_aqui` con tu clave de API real de OpenRouter:

    ```
    OPENROUTER_API_KEY=sk-or-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
    ```

    **¡Importante!** No compartas tu archivo `.env` ni subas tu clave de API a ningún repositorio público. El archivo `.gitignore` ya está configurado para ignorar `.env`.

### 4. Ejecutar la Aplicación

Una vez configurado, puedes iniciar la aplicación Flask:

```bash
python3 app.py
```

La aplicación se ejecutará en `http://localhost:5000`. Abre esta URL en tu navegador para interactuar con el sistema de debate IA.

## Estructura del Proyecto

*   `app.py`: El script principal de la aplicación Flask (ofuscado).
*   `templates/`: Contiene las plantillas HTML para la interfaz de usuario.
*   `requirements.txt`: Lista de dependencias de Python.
*   `.env.example`: Archivo de ejemplo para la configuración de variables de entorno.
*   `.gitignore`: Define los archivos y directorios que Git debe ignorar.
*   `pyarmor_runtime_000000/`: Directorio que contiene los archivos de tiempo de ejecución necesarios para ejecutar el código ofuscado de PyArmor. **Este directorio es esencial para que la aplicación funcione.**

## Notas sobre el Código Ofuscado

El archivo `app.py` en este repositorio ha sido procesado con PyArmor para ofuscar su código fuente. Esto significa que el código no es legible directamente, pero la aplicación funcionará normalmente. El directorio `pyarmor_runtime_000000` debe estar presente junto a `app.py` para que la aplicación ofuscada se ejecute correctamente.

---

**Autor**: Manus AI
**Fecha**: 05 de Julio de 2026
