# Guía para Contribuyentes de Saika Suite

¡Gracias por tu interés en contribuir a Saika Suite\! Tu apoyo es fundamental para hacer de este proyecto una herramienta poderosa y accesible para la comunidad cubana y más allá.

Esta guía te ayudará a entender cómo puedes contribuir, qué esperamos de tus contribuciones y cómo mantener la calidad y coherencia del código base.

## 1\. Código de Conducta

Antes de empezar, por favor, revisa nuestro [Código de Conducta](https://www.google.com/search?q=CODE_OF_CONDUCT.md). Nos comprometemos a fomentar un entorno abierto y acogedor. Como colaboradores, nos comprometemos a hacer de la participación en nuestro proyecto y nuestra comunidad una experiencia libre de acoso para todos, independientemente de la edad, tamaño corporal, discapacidad visible o invisible, etnia, características sexuales, identidad y expresión de género, nivel de experiencia, educación, estado socioeconómico, nacionalidad, apariencia personal, raza, religión u orientación e identidad sexual.

## 2\. ¿Cómo Contribuir?

Hay muchas formas de contribuir a Saika Suite, no solo escribiendo código:

  * **Reportar Errores (Bugs)**: Si encuentras un error, repórtalo. Una buena descripción del error es invaluable.
  * **Sugerir Características (Features)**: Comparte tus ideas para nuevas funcionalidades o mejoras.
  * **Mejorar la Documentación**: La documentación clara y precisa es vital. Ayúdanos a mejorarla.
  * **Escribir Código**: Implementa nuevas características, corrige errores o mejora el código existente.
  * **Traducir**: Ayuda a traducir la aplicación y la documentación a otros idiomas.
  * **Pruebas**: Ayuda a probar las nuevas características o a verificar los informes de errores.
  * **Retroalimentación (Feedback)**: Usa la aplicación y danos tu opinión. ¡Tu experiencia es importante\!

## 3\. ¿Dónde Empezar?

  * **Issues Abiertos**: Consulta la sección de [Issues](https://www.google.com/search?q=https://github.com/SaikaNET-Studio/saika-suite/issues) en GitHub. Busca etiquetas como `good first issue`, `bug`, `enhancement` o `help wanted`.
  * **Discusiones**: Únete a las discusiones en el repositorio o en los canales de comunicación de SaikaNET Studio (si los hay).

## 4\. Reportar Errores

Si encuentras un error:

1.  **Busca primero:** Antes de crear un nuevo issue, busca si ya existe un informe similar.
2.  **Usa la plantilla:** Abre un nuevo issue y selecciona la plantilla `bug_report.md`.
3.  **Describe el problema:**
      * **Pasos para reproducir:** Explica cómo replicar el error, paso a paso.
      * **Comportamiento esperado vs. observado:** Describe lo que esperabas que sucediera y lo que realmente ocurrió.
      * **Versión de Saika Suite y tu sistema operativo:** Indica qué versión del software estás usando y en qué sistema operativo (Windows, Android, Linux).
      * **Capturas de pantalla o videos:** Si es posible, adjunta imágenes o videos que ilustren el problema.
      * **Para errores offline:** Si el error ocurre sin conexión, usa la plantilla `feedback_offline.md` para describir las condiciones.

## 5\. Sugerir Características

Si tienes una idea para una nueva característica:

1.  **Busca primero:** Asegúrate de que la característica no haya sido sugerida ya.
2.  **Usa la plantilla:** Abre un nuevo issue y selecciona la plantilla `feature_request.md`.
3.  **Describe la característica:** Explica claramente la idea, por qué crees que es útil y cómo beneficiaría a los usuarios.

## 6\. Contribuciones de Código

Para enviar cambios de código, sigue estos pasos:

1.  **Fork el Repositorio:** Crea tu propia copia (fork) del repositorio de Saika Suite en GitHub.
2.  **Clona tu Fork:**
    ```bash
    git clone https://github.com/TU_USUARIO/saika-suite.git
    cd saika-suite
    ```
3.  **Crea una Rama (Branch):** Crea una nueva rama para tus cambios. Usa un nombre descriptivo (ej. `feature/nueva-funcion-x` o `bugfix/corregir-error-y`).
    ```bash
    git checkout -b feature/nombre-de-tu-feature
    ```
4.  **Configura tu Entorno de Desarrollo:** Asegúrate de tener Python 3.x y todas las dependencias instaladas. Consulta el `README_es.md` para más detalles.
    ```bash
    pip install -r requirements.txt
    # Opcional, si aplicas cambios a plataformas específicas:
    # pip install -r requirements_android.txt
    # pip install -r requirements_linux.txt
    ```
5.  **Realiza tus Cambios:** Implementa tus mejoras o correcciones. Sigue las convenciones de codificación existentes en el proyecto.
      * **Modularidad:** Mantén el código bien modularizado, siguiendo la estructura definida en `src/`.
      * **Comentarios:** Comenta tu código cuando sea necesario para explicar lógica compleja.
      * **Pruebas:** Si añades nuevas características, considera escribir pruebas unitarias para ellas en el directorio `tests/unit/`.
6.  **Realiza un Commit:** Haz commits claros y atómicos. Cada commit debe representar un cambio lógico.
    ```bash
    git add .
    git commit -m "feat: Añadir nueva función X para el módulo SaikaPlay"
    # o
    git commit -m "fix: Corregir error de descarga en SaikaGrab al reanudar"
    ```
7.  **Empuja (Push) tu Rama:**
    ```bash
    git push origin feature/nombre-de-tu-feature
    ```
8.  **Crea un Pull Request (PR):**
      * Ve a tu repositorio fork en GitHub y verás una opción para crear un Pull Request desde tu rama a la rama `main` del repositorio original de Saika Suite.
      * **Título del PR:** Debe ser claro y conciso, resumiendo el cambio.
      * **Descripción del PR:** Explica detalladamente los cambios realizados, por qué son necesarios, y si resuelve algún issue existente (enlaza el issue usando `#` seguido del número, ej. `#123`).
      * **Capturas de pantalla/videos:** Si los cambios son visuales, incluye demostraciones.

### Directrices de Código

  * **PEP 8:** Intentamos seguir las directrices de estilo de código [PEP 8](https://peps.python.org/pep-0008/).
  * **Nombres de Variables y Funciones:** Utiliza nombres descriptivos y snake\_case.
  * **Separación de Responsabilidades:** Cada módulo y función debe tener una responsabilidad clara y única.
  * **Internacionalización (i18n):** Si tu cambio implica texto visible para el usuario, asegúrate de que sea "i18n-ready" (listo para ser traducido), usando los mecanismos que definamos para ello en `src/core/utilities/i18n.py`.

## 7\. Proceso de Revisión de Pull Requests

Una vez que envíes tu Pull Request:

  * El equipo de SaikaNET Studio lo revisará.
  * Podemos solicitar cambios, mejoras o aclaraciones.
  * Sé paciente y receptivo a los comentarios; la revisión es un proceso colaborativo para mejorar el software.
  * Una vez aprobado, tus cambios serán fusionados en la rama `main`.

## 8\. Licencia

Al contribuir a Saika Suite, aceptas que tus contribuciones se licenciarán bajo las mismas condiciones que el proyecto principal. Revisa nuestro archivo [LICENSE](https://www.google.com/search?q=LICENSE) para más detalles.

¡Esperamos tus contribuciones y agradecemos tu apoyo para construir un Saika Suite aún mejor\!

-----
