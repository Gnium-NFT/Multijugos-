Acerca del examen de código con CodeQL
Puedes utilizar CodeQL para identificar las vulnerabilidades y errores en tu código. Los resultados se muestran como alertas del code scanning en GitHub.

¿Quién puede utilizar esta característica?
Code scanning está disponible para los siguientes tipos de repositorios:

Repositorios públicos en GitHub.com
Repositorios propiedad de la organización en GitHub Enterprise Cloud con GitHub Advanced Security habilitado
En este artículo
Acerca de CodeQL
Modelado de marcos personalizados o de nicho
Consultas de CodeQL
CodeQL es el motor de análisis de código que desarrolló GitHub para automatizar las verificaciones de seguridad. Puedes analizar tu código utilizando CodeQL y mostrando los resultados como alertas del code scanning.

Hay dos tres principales de usar el análisis de CodeQL para code scanning:

Usa la configuración predeterminada para configurar rápidamente el análisis de CodeQL para el code scanning en el repositorio. La configuración predeterminada elige automáticamente los lenguajes que se van a analizar, los conjuntos de consultas que se van a ejecutar y los eventos que desencadenan exámenes. Si lo prefiere, puede seleccionar manualmente el conjunto de consultas para ejecutar y lenguajes que se van a analizar. Después de habilitar CodeQL, GitHub Actions ejecutará ejecuciones de flujo de trabajo para examinar el código. Para más información, consulta Establecimiento de la configuración predeterminada para el examen del código.

Usa la configuración avanzada para agregar el flujo de trabajo de CodeQL al repositorio. Esto genera un archivo de flujo de trabajo personalizable en el que se usa github/codeql-action para ejecutar la instancia de CodeQL CLI. Para más información, consulta Establecimiento de la configuración avanzada para el examen del código.

Ejecuta CodeQL CLI directamente en un sistema de integración continua externo y carga los resultados en GitHub. Para más información, consulta Utilizar el análisis de código de CodeQL con tu sistema de IC existente.

Para más información sobre alertas de code scanning, consulta Acerca de las alertas de análisis de código.

Acerca de CodeQL
CodeQL es un lenguaje de programación y herramientas asociadas que tratan código como datos. Se creó explícitamente para facilitar el análisis de código y encontrar posibles vulnerabilidades en el código con mayor confianza que los analizadores estáticos tradicionales.

Generas una base de datos de CodeQL para representar tu base de código.
Entonces, ejecutarás consultas de CodeQL en esa base de datos para identificar problemas en la base de código.
Estos resultados de consulta se muestran como alertas del code scanning en GitHub cuando utilizas al CodeQL con el code scanning.
CodeQL es compatible tanto con lenguajes compilados como interpretados, y puede buscar vulnerabilidades y errores en el código escrito en los lenguajes compatibles.

C/C++
C#
Go
Java/Kotlin
JavaScript/TypeScript
Python
Ruby
Swift
Note

Use java-kotlin para analizar el código escrito en Java, Kotlin o ambos.
Use javascript-typescript para analizar el código escrito en JavaScript, TypeScript o ambos.
Para más información, vea la documentación en el sitio web de CodeQL: "Lenguajes y marcos admitidos".

Modelado de marcos personalizados o de nicho
Expertos de GitHub, investigadores de seguridad y colaboradores de la comunidad escriben bibliotecas para modelar el flujo de datos en marcos y bibliotecas populares. Si usas dependencias personalizadas que no están modeladas, puedes usar la extensión CodeQL para Visual Studio Code para crear modelos para estas dependencias y usarlos para ampliar el análisis. Para más información, consulta Uso del editor de modelos de CodeQL.

Consultas de CodeQL
Los expertos de GitHub, investigadores de seguridad y contribuyentes comunitarios escriben y mantienen las consultas predeterminadas de CodeQL que se utilizan para el code scanning. Las consultas se actualizan periódicamente para mejorar el análisis y reducir los falsos positivos.

Escribir sus propias consultas
Las consultas son de código abierto, por lo que puede verlas y contribuir a ellas en el repositorio github/codeql. Para obtener más información, consulta Acerca de las consultas de CodeQL en la documentación de CodeQL.

Ejecutar consultas adicionales
Si vas a examinar el código con una configuración avanzada o un sistema de CI externo, puedes ejecutar consultas adicionales como parte del análisis.

Estas consultas deben pertenecer a un paquete de consultas de CodeQL publicado o un paquete de CodeQL en un repositorio.

Cuando un paquete de consultas de CodeQL se publica en el Container registry de GitHub, todas las dependencias transitivas que requieren las consultas y un caché de compilación se incluyen en el paquete. Esto mejora el rendimiento y garantiza que el ejecutar las consultas del paquete proporciona resultados idénticos cada vez que actualizas a una versión nueva del paquete o de CLI.

Los paquetes de consultas de CodeQL pueden descargarse de varios registros de contenedor GitHub. Para más información, consulta Personalización de la configuración avanzada para el examen de código.

Para más información, consulta Personalización del análisis con paquetes de CodeQL.
