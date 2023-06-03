[![Abrir en GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526682400)

# API HTTP de Python con GitHub Codespaces y Copilot

_Ejecuta una API de Python en este repositorio listo para usar en minutos_

Al abrir este repositorio de plantilla en Codespaces, puedes ponerte rápidamente en acción con una aplicación web de Python que sirve una API HTTP. Podrás centrarte en trabajar en el proyecto en lugar de ocuparte de la configuración y la preparación. Y luego realizarás cambios en el código utilizando [GitHub Copilot](https://copilot.github.com/), una nueva herramienta de finalización de código impulsada por IA que te ayuda a escribir código más rápido.

## 🚀 Inicio rápido
1. [Sigue los pasos](#--pruébalo) para configurar tu espacio de trabajo en Codespaces y ejecutar la aplicación.
2. [Realiza cambios en la aplicación](#realiza-cambios-con-copilot) utilizando [GitHub Copilot](https://copilot.github.com/) para modificar el código.
3. Acepta el desafío y implementa tu aplicación en Azure.

🤔 ¿Curioso? Mira el siguiente video donde explicamos todos los detalles:

[![Entorno de desarrollo de Python con Codespaces](https://img.youtube.com/vi/_i9Pywj3rSg/0.jpg)](https://youtu.be/_i9Pywj3rSg "Entorno de desarrollo de Python con Codespaces")


<details>
   <summary><strong>Aprende más sobre las APIs</strong></summary>

   Una API (Interfaz de Programación de Aplicaciones, por sus siglas en inglés) describe una forma en que dos computadoras pueden interactuar entre sí.
   Una API HTTP permite que una computadora conectada a Internet envíe una solicitud HTTP a otra computadora conectada a Internet y reciba una respuesta. Por ejemplo, mi computadora podría enviar una solicitud a
   `http://un-sitio-web-climatico-api.com/api/ciudad=Los+Angeles` y recibir datos como `{"máxima": 72, "mínima": 66}`.

   Las APIs HTTP a menudo proporcionan datos o funcionalidades únicas para un servicio, como el ejemplo de una API para un sitio web climático. Un sitio web climático podría ofrecer puntos finales de API adicionales para otras funcionalidades relacionadas con el clima, como pronósticos futuros o datos históricos. Cualquier sitio web puede decidir ofrecer una API si cree que tiene una funcionalidad útil para compartir con otras computadoras. En este proyecto, ejecutarás una API HTTP que genera un token aleatorio.
</details>

Esta plantilla también está lista para ser utilizada con [Codespaces](https://github.com/features/codespaces), un entorno de desarrollo en la nube con [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza).

<details>
   <summary><b>🎥 Mira el video tutorial para aprender más sobre Codespaces</b></summary>

   [![Tutorial de Codespaces](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://aka.ms/CodespacesVideoTutorial "Tutorial de Codespaces")
</details>

## Para estudiantes y desarrolladores

Usando Codespaces,

 obtienes [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza) en la nube, utilizando un "contenedor de desarrollo". Al igual que con una versión local de [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza), la versión en la nube también te permite instalar extensiones y utilizar una terminal.

También puedes configurar tu contenedor de desarrollo para ejecutar una versión específica y tenerlo configurado con tus extensiones favoritas.

Estos son los archivos y carpetas clave que lo hacen posible:

- [webapp/](./.webapp): El código de la API HTTP, construido con el framework FastAPI.
- [.devcontainer/Dockerfile](./.devcontainer/Dockerfile): Archivo de configuración utilizado por Codespaces para determinar el sistema operativo y otros detalles.
- [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json): Archivo de configuración utilizado por Codespaces para configurar las opciones de [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza), como la activación de extensiones adicionales.

## 🧐 Utilizar Codespaces

Prueba esta plantilla de repositorio utilizando Codespaces siguiendo estos pasos:

1. Crea un repositorio a partir de esta plantilla. Utiliza este [enlace para crear el repositorio](https://github.com/microsoft/codespaces-project-template-py/generate). Puedes hacer que el repositorio sea privado o público, como prefieras.
2. Antes de crear el espacio de trabajo, ¡habilita GitHub Copilot para tu cuenta! Si no está habilitado, consulta [Realiza cambios utilizando Copilot](#realiza-cambios-con-copilot).
3. Accede a la página principal del repositorio recién creado.
4. Debajo del nombre del repositorio, usa el menú desplegable "Code" y en la pestaña de Codespaces, selecciona "Crear Codespace en main".
   ![Crear Codespace](https://docs.github.com/assets/cb-138303/images/help/codespaces/new-codespace-button.png)
5. Espera mientras GitHub inicializa el espacio de trabajo:
   ![Creando Codespace](https://github.com/microsoft/codespaces-teaching-template-py/raw/main/images/Codespace_build.png)

### Inspecciona tu entorno de Codespaces

Lo que tienes en este punto es un entorno preconfigurado donde ya se han instalado todas las versiones y bibliotecas que necesitas. Es una experiencia de configuración cero.

## Ejecución de la aplicación

Esta aplicación de Python utiliza FastAPI, un potente framework web que autodocumenta sus puntos finales de API. La API tiene solo un punto final que genera una cadena pseudoaleatoria única que se puede utilizar como token.


![Ejecución de FastAPI](./images/api-running.png)


<details>
<summary><b>Ejecuta FastAPI dentro de Codespace</b></summary>

La API incluida en este repositorio de plantilla tiene un solo punto final que genera un token. Ponlo en marcha siguiendo estos pasos:

1. Abre una ventana de terminal abriendo la paleta de comandos (Ctrl+Shift+P o Cmd+Shift+P) y selecciona el comando "Abrir nueva terminal".
2. Ejecuta `uvicorn` en la consola para iniciar la aplicación de la API:



    ```console
    uvicorn --host 0.0.0.0 webapp.main:app --reload
    ```

    Deberías ver una salida similar a esta:

    ```output
    INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
    INFO:     Started reloader process [28720]
    INFO:     Started server process [28722]
    INFO:     Waiting for application startup.
    INFO:     Application startup complete.
    ```

    Aparecerá una ventana emergente que indica que tu aplicación está disponible en el puerto 8000. Haz clic en el botón para abrirlo en el navegador.
3. Una vez que se cargue el sitio, haz clic en el botón "Probar" o agrega `/docs` al final de la URL en la barra de direcciones. La documentación de la API generada automáticamente debería cargarse y verse así:

   ![Documentos de OpenAPI](./images/fast-api.png)

4. Por último, intenta interactuar con la API enviando una solicitud utilizando la página autodocumentada. Haz clic en el botón "POST" y luego en el botón "Probar":

   ![Probar una solicitud POST](./images/try-it-out.png)

🔒 ¿Ves el candado junto a la URL del sitio web en el navegador? Eso indica que el sitio web se está sirviendo a través de una conexión segura HTTPS que cifra las respuestas HTTP. Esto es muy importante cuando una API puede recibir datos sensibles o responder con datos sensibles (como una contraseña).

</details>

## Personaliza tu Codespace

Puedes cambiar tu entorno y el editor de texto para que la próxima vez que crees (o reconstruyas) el entorno, todo se configure automáticamente. Veamos dos desafíos diferentes que seguramente querrás hacer:

1. Cambiar la versión de Python
2. Agregar o modificar una extensión de editor preinstalada


<details>

<summary><b>Paso 1: Cambiar el entorno de Python</b></summary>

Digamos que deseas cambiar la versión de Python que está instalada. Esto es algo que puedes controlar.

Abre [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json) y reemplaza la siguiente sección:

```json
"VARIANT": "3.8-bullseye"
```

con la siguiente instrucción:

```json
"VARIANT": "3.9-bullseye"
```

Este cambio indica a Codespaces que use Python 3.9 en lugar de 3.8.

Si realizas algún cambio de configuración en `devcontainer.json`, aparecerá un cuadro después de guardar.

![Recreando Codespace](https://github.com/microsoft/codespaces-teaching-template-py/raw/main/images/Codespace_rebuild.png)

Haz clic en "rebuild". Espera a que tu Codespace reconstruya el entorno de VS Code.

</details>


<details>

<summary><b>Paso 2: Agregar una extensión</b></summary>

Tu entorno viene con extensiones preinstaladas. Puedes cambiar las extensiones con las que tu entorno de Codespaces se inicia. Aquí te explicamos cómo hacerlo:

1. Abre el archivo [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json) y busca el elemento JSON **extensions**:

   ```json
   "extensions": [
    "ms-python.python",
   

 "ms-python.vscode-pylance"
   ],
   ```

2. Agrega una nueva extensión a la lista. Por ejemplo, puedes agregar la extensión de Docker:

   ```json
   "extensions": [
    "ms-python.python",
    "ms-python.vscode-pylance",
    "ms-azuretools.vscode-docker"
   ],
   ```

   Puedes agregar cualquier otra extensión disponible en el [Marketplace de Visual Studio Code](https://marketplace.visualstudio.com/).
3. Una vez que hayas guardado los cambios, tu Codespace se reconstruirá automáticamente y tendrás la nueva extensión disponible cuando vuelvas a abrirlo.

</details>

## Realiza cambios con Copilot

Una de las características más emocionantes de este proyecto es la posibilidad de utilizar [GitHub Copilot](https://copilot.github.com/). Copilot es una herramienta de finalización de código impulsada por IA que puede ayudarte a escribir código más rápido.

Copilot se basa en un modelo de lenguaje de IA avanzado y se entrena con una gran cantidad de código fuente público. Puede sugerir fragmentos de código completos y autocompletar líneas de código mientras escribes.

En este proyecto, puedes aprovechar Copilot para realizar cambios en la aplicación de API HTTP de Python. Copilot analizará el código existente y sugerirá cambios o adiciones basadas en el contexto y la intención.

Aquí tienes algunos consejos para aprovechar al máximo Copilot:

- Escribe comentarios descriptivos y específicos en tu código para darle contexto adicional a Copilot.
- Usa `# TODO` para indicar tareas que te gustaría que Copilot completara.
- Acepta sugerencias de Copilot si consideras que son útiles, pero revísalas siempre antes de incorporarlas en tu código.

¡Diviértete experimentando con Copilot y descubre cómo puede ayudarte a desarrollar más rápidamente!

## ¿Qué sigue?

Ahora que tienes la aplicación de API HTTP en funcionamiento en Codespaces, puedes comenzar a modificarla y expandirla según tus necesidades. Aquí hay algunas ideas para comenzar:

- Agrega nuevos puntos finales a la API que realicen diferentes tareas o proporcionen diferentes tipos de datos.
- Implementa una base de datos para almacenar y recuperar datos en la API.
- Agrega autenticación y autorización a la API para proteger los puntos finales.
- Conecta la API con otros servicios o APIs externas para obtener o enviar datos.

Recuerda que también puedes implementar tu aplicación en un servidor real utilizando servicios en la nube como [Azure](https://azure.microsoft.com/?WT.mc_id=academic-77460-alfredodeza). Esto te permitirá hacer que tu API sea accesible para otros usuarios y aplicaciones.

¡Diviértete explorando y desarrollando tu aplicación de API HTTP con Codespaces y Copilot!

## 📚 Recursos adicionales

- [Documentación de FastAPI](https://fastapi.tiangolo.com/)
- [Documentación de Uvicorn](https://www.uvicorn.org/)
- [Documentación de GitHub Copilot](https://copilot.github.com/)
- [Documentación de Codespaces](https://docs.github.com/en/codespaces)
- [Preguntas frecuentes de Codespaces](https://docs.github.com/en/codespaces/codespaces-reference/about-codespaces#faq)
- [Explorar las plantillas de Codespaces](https://github.com/topics/codespaces)
