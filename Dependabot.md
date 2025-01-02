Acerca de la seguridad de la cadena de suministro
GitHub te ayuda a proteger la cadena de suministro, desde comprender las dependencias de tu entorno a conocer las vulnerabilidades de dichas dependencias y aplicarles revisiones.

En este artículo
Acerca de la seguridad de la cadena de suministro en GitHub
Introducción a las características
Disponibilidad de características
Acerca de la seguridad de la cadena de suministro en GitHub
Al desarrollar un proyecto de software, es probable que uses otro software para compilar y ejecutar la aplicación, como bibliotecas de código abierto, marcos u otras herramientas. Estos recursos se conocen colectivamente como "dependencias", ya que el proyecto depende de ellos para funcionar correctamente. El proyecto podría basarse en cientos de estas dependencias, formando lo que se conoce como "cadena de suministro".

La cadena de suministro puede suponer un problema de seguridad. Si una de las dependencias tiene una vulnerabilidad de seguridad conocida o un error, los actores malintencionados podrían aprovechar esta vulnerabilidad para, por ejemplo, insertar código malintencionado ("software malicioso"), robar datos confidenciales o provocar algún otro tipo de interrupción en el proyecto. Este tipo de amenaza se denomina "ataque de cadena de suministro". Tener dependencias vulnerables en la cadena de suministro pone en peligro la seguridad de tu propio proyecto y también pone en riesgo a los usuarios.

Una de las cosas más importantes que puede hacer para proteger su cadena de suministro consiste en revisar sus dependencias vulnerables y reemplazar cualquier software malicioso.

Las dependencias se agregan directamente a la cadena de suministro cuando se especifican en un archivo de manifiesto o en un archivo de bloqueo. Las dependencias también se pueden incluir de forma transitiva, es decir, incluso si no especifica una dependencia concreta, pero se usa en una dependencia propia, también dependerá de esa dependencia.

GitHub ofrece una variedad de características que te ayudarán a comprender las dependencias del entorno, conocer las vulnerabilidades de esas dependencias y aplicarles revisiones.

Las características de la cadena de suministro en GitHub son las siguientes:

Gráfica de dependencias
Revisión de dependencias
Dependabot alerts
Dependabot updates
Dependabot security updates
Dependabot version updates
El gráfico de dependencias es fundamental para la seguridad de la cadena de suministro. En el gráfico de dependencias se identifican todas las dependencias ascendentes y las dependencias descendentes públicas de un repositorio o paquete. En el gráfico de dependencias del repositorio puede ver las dependencias del repositorio y algunas de sus propiedades, como la información de vulnerabilidad.

Otras características de la cadena de suministro de GitHub dependen de la información proporcionada por el gráfico de dependencias.

La revisión de dependencias usa el gráfico de dependencias para identificar los cambios de dependencias y ayudarle a comprender el impacto en la seguridad de estos cambios al revisar solicitudes de incorporación de cambios.
Dependabot realiza referencias cruzadas entre los datos de dependencia proporcionados por el gráfico de dependencias y la lista de advertencias publicadas en GitHub Advisory Database, examina las dependencias y genera Dependabot alerts cuando se detecta una posible vulnerabilidad.
Las Dependabot security updates usan el gráfico de dependencias y Dependabot alerts para ayudarte a actualizar las dependencias con vulnerabilidades conocidas en el repositorio.
Dependabot version updates no usan el gráfico de dependencias y en su lugar se basan en el control de versiones semántico de las dependencias. Dependabot version updates ayudan a mantener actualizadas las dependencias, incluso cuando no tienen ninguna vulnerabilidad.

Para obtener guías de procedimientos recomendados sobre la seguridad de la cadena de suministro de un extremo a otro, incluida la protección de cuentas personales, código y procesos de compilación, consulta Protección de la cadena de suministro de un extremo a otro.

Introducción a las características
Qué es el gráfico de dependencias
Para generar el gráfico de dependencias, GitHub examina las dependencias explícitas de un repositorio declaradas en el manifiesto y los archivos de bloqueo. Cuando se habilita, el gráfico de dependencias analiza automáticamente todos los archivos de manifiesto de paquete conocidos del repositorio y los usa para construir un gráfico con versiones y nombres de dependencia conocidos.

El gráfico de dependencias incluye información sobre las dependencias directas y las transitivas.
El gráfico de dependencias se actualiza automáticamente al insertar una confirmación en GitHub que cambia o agrega un archivo de manifiesto o de bloqueo admitido a la rama predeterminada y cuando alguien inserta un cambio en el repositorio de una de las dependencias.
Para ver el gráfico de dependencias, abra la página principal del repositorio en GitHub y vaya a la pestaña Conclusiones.
Si tienes al menos acceso de lectura al repositorio, puedes exportar el gráfico de dependencias del repositorio como una la lista de materiales de software (SBOM) compatible con SPDX, a través de la interfaz de usuario de GitHub o la API REST de GitHub. Para obtener más información, vea «Exportación de una lista de materiales de software para el repositorio».
De manera adicional, puede usar API de envío de dependencias para enviar dependencias desde el administrador de paquetes o el ecosistema que prefiera, incluso si el ecosistema no es compatible con el gráfico de dependencias para el análisis del archivo de manifiesto o de bloqueo. Las dependencias enviadas a un proyecto con API de envío de dependencias mostrarán qué detector se usó para su envío y cuándo se enviaron. Para obtener más información sobre API de envío de dependencias, vea "Uso de la Dependency submission API".

Para más información sobre el gráfico de dependencias, consulta Acerca del gráfico de dependencias.

Qué es la revisión de dependencias
La revisión de dependencias ayuda a los revisores y colaboradores a comprender los cambios de dependencia y su impacto en la seguridad en cada solicitud de incorporación de cambios.

La revisión de dependencias indica qué dependencias se han agregado, quitado o actualizado en una solicitud de incorporación de cambios. Puede usar las fechas de lanzamiento, la popularidad de las dependencias y la información de vulnerabilidad para ayudarle a decidir si quiere aceptar el cambio.
Puede ver la revisión de dependencias de una solicitud de incorporación de cambios si muestra la diferencia enriquecida en la pestaña Archivos cambiados.
Para más información sobre la revisión de dependencias, consulta Acerca de la revisión de dependencias.

Qué es Dependabot
Dependabot mantiene actualizadas las dependencias para lo cual te informa de cualquier vulnerabilidad de seguridad en ellas, y abre solicitudes de incorporación de cambios de forma automática para actualizar las dependencias a la siguiente versión segura disponible cuando se desencadena una alerta de Dependabot, o bien a la versión más reciente cuando se publica una versión.

El término "Dependabot" abarca las características siguientes:

Dependabot alerts: notificación que se muestra en la pestaña Security del repositorio y en el gráfico de dependencias de este. La alerta incluye un enlace al archivo afectado en el proyecto e información acerca de la versión arreglada.
Dependabot updates:
Dependabot security updates: actualizaciones desencadenadas para actualizar las dependencias a una versión segura cuando se desencadena una alerta.
Dependabot version updates: actualizaciones programadas para mantener actualizadas las dependencias con la versión más reciente.
Las solicitudes de incorporación de cambios que abre Dependabot pueden desencadenar flujos de trabajo que ejecutan acciones. Para más información, consulta Automatizar al Dependabot con las GitHub Actions.

De forma predeterminada:

Si habilita GitHub Actions en el repositorio, GitHub ejecuta Dependabot updates en GitHub Actions.

Si GitHub Actions no está habilitado para el repositorio, GitHub genera Dependabot alerts mediante la aplicación integrada Dependabot en GitHub.

Para más información, consulta Acerca de Dependabot en ejecutores de Acciones de GitHub.

Dependabot security updates puede corregir dependencias vulnerables en GitHub Actions. Cuando se habilitan las actualizaciones de seguridad, Dependabot generará automáticamente una solicitud de cambios para actualizar los datos vulnerables GitHub Actions usados en los flujos de trabajo a la versión con revisión mínima. Para más información, consulta Sobre las actualizaciones de seguridad de Dependabot.

Qué son las alertas de Dependabot
Dependabot alerts resalta los repositorios afectados por una vulnerabilidad recién detectada en función del gráfico de dependencias y GitHub Advisory Database, que contiene las versiones en listas de vulnerabilidades conocidas.

Dependabot realiza un examen para detectar las dependencias no seguras y envía Dependabot alerts cuando:
Se agrega un aviso nuevo a GitHub Advisory Database.
Cambia el gráfico de dependencias del repositorio.
Las Dependabot alerts se muestran en la pestaña Seguridad y en el gráfico de dependencias del repositorio. La alerta incluye un enlace al archivo afectado en el proyecto e información acerca de la versión arreglada.
Para más información, consulta Acerca de las alertas Dependabot.

Qué son las actualizaciones de Dependabot
Hay dos tipos de Dependabot updates: actualizaciones de seguridad y de versión de Dependabot. En los dos casos Dependabot genera solicitudes de incorporación de cambios automáticas para actualizar las dependencias, pero hay varias diferencias.

Dependabot security updates:

Desencadenada por una alerta de Dependabot
Actualizan las dependencias a la versión mínima que resuelve una vulnerabilidad conocida
Compatible con ecosistemas admitidos en el gráfico de dependencias
No requiere un archivo de configuración, pero puedes usar uno para invalidar el comportamiento predeterminado.
Dependabot version updates:

Requiere un archivo de configuración
Se ejecutan según una programación que configure
Actualizan las dependencias a la versión más reciente que coincida con la configuración
Compatible con un grupo diferente de ecosistemas
Para más información sobre Dependabot updates, consulta Sobre las actualizaciones de seguridad de Dependabot y Acerca de las actualizaciones a la versión del Dependabot.

Disponibilidad de características
Repositorios públicos:

Gráfico de dependencias: habilitado de forma predeterminada y no se puede deshabilitar.
Revisión de dependencias: habilitada de forma predeterminada y no se puede deshabilitar.
Dependabot alerts: no está habilitado de forma predeterminada. GitHub detecta las dependencias no seguras y muestra información en el gráfico de dependencias, pero no genera Dependabot alerts de forma predeterminada. Los propietarios de repositorios o los usuarios con acceso administrativo pueden habilitar las Dependabot alerts. También puede habilitar o deshabilitar las alertas de Dependabot para todos los repositorios que pertenecen a la cuenta de usuario u organización. Para más información, consulta Administración de la configuración de seguridad y análisis para la cuenta personal o Administrar la configuración de seguridad y análisis de su organización.
Repositorios privados:

Gráfico de dependencias: no está habilitado de forma predeterminada. Los administradores del repositorio pueden habilitar la característica. Para más información, consulta Explorar las dependencias de un repositorio.

Revisión de dependencias: disponible en los repositorios privados propiedad de las organizaciones que usan GitHub Enterprise Cloud y que tienen una licencia para GitHub Advanced Security. Para más información, vea la documentación de GitHub Enterprise Cloud.

Dependabot alerts: no está habilitado de forma predeterminada. Los propietarios de los repositorios privados o las personas con acceso administrativo puede habilitar las Dependabot alerts si habilitan la gráfica de dependencias y las Dependabot alerts para sus repositorios. También puede habilitar o deshabilitar las alertas de Dependabot para todos los repositorios que pertenecen a la cuenta de usuario u organización. Para más información, consulta Administración de la configuración de seguridad y análisis para la cuenta personal o Administrar la configuración de seguridad y análisis de su organización.

Cualquier tipo de repositorio:

Dependabot security updates: no está habilitado de forma predeterminada. Puedes habilitar las Dependabot security updates para cualquier repositorio que utilice Dependabot alerts y la gráfica de dependencias. Para obtener información sobre cómo habilitar las actualizaciones de seguridad, consulta Configuración de actualizaciones de seguridad de Dependabot.
Dependabot version updates: no está habilitado de forma predeterminada. Las personas con permisos de escritura en un repositorio pueden habilitar las Dependabot version updates. Para obtener información sobre cómo habilitar las actualizaciones de versión, consulta Configuración de las actualizaciones de versiones de Dependabot.
