Configuración de ajustes de seguridad globales para su organización
Personalice las funciones de seguridad avanzada de GitHub para fortalecer la seguridad de su organización.

¿Quién puede utilizar esta función?
Propietarios de organizaciones, administradores de seguridad y miembros de la organización con el rol de administrador

En este artículo
Acerca de la configuración global
Cómo acceder a la página de configuración global de su organización
Configuración de los ajustes globales del Dependabot
Configuración de los ajustes globales de escaneo de código
Configuración de los ajustes de escaneo secreto global
Creación de administradores de seguridad para su organización
Acerca de la configuración global
Además de las configuraciones de seguridad, que determinan la configuración de seguridad a nivel de repositorio, también debes configurar las configuraciones globales para tu organización. Las configuraciones globales se aplican a toda tu organización y pueden personalizar las funciones de seguridad avanzada de GitHub según tus necesidades.

Cómo acceder a la página de configuración global de su organización
En la esquina superior derecha de GitHub, selecciona tu foto de perfil y luego haz clic en Tus organizaciones .

Debajo del nombre de su organización, haga clic en Configuración . Si no puede ver la pestaña "Configuración", seleccione el menú desplegable y luego haga clic en Configuración .

Captura de pantalla de las pestañas del perfil de una organización. La pestaña "Configuración" está resaltada en naranja oscuro.
En la sección "Seguridad" de la barra lateral, seleccione el menú desplegable Seguridad del código y luego haga clic en Configuración global .

Configuración de los ajustes globales del Dependabot
Dependabot consta de tres funciones diferentes que le ayudan a administrar sus dependencias:

Alertas de Dependabot: le informan sobre vulnerabilidades en las dependencias que utiliza en su repositorio.
Actualizaciones de seguridad de Dependabot: genera automáticamente solicitudes de extracción para actualizar las dependencias que utilizas y que tienen vulnerabilidades de seguridad conocidas.
Actualizaciones de versiones de Dependabot: genera solicitudes de extracción automáticamente para mantener tus dependencias actualizadas.
Puede personalizar varias configuraciones globales para Dependabot:

Creación y gestión de reglas de clasificación automática de Dependabot
Agrupación de actualizaciones de seguridad de Dependabot
Habilitar actualizaciones de dependencias en ejecutores de GitHub Actions
Conceder a Dependabot acceso a repositorios privados e internos
Creación y gestión de reglas de clasificación automática de Dependabot
Puede crear y administrar reglas de clasificación automática de Dependabot para indicarle que descarte o posponga automáticamente las alertas de Dependabot e incluso que abra solicitudes de extracción para intentar resolverlas. Para configurar las reglas de clasificación automática de Dependabot, haga clic en rules" %} y luego cree o edite una regla:

Puede crear una nueva regla haciendo clic en Nueva regla , luego ingresando los detalles de su regla y haciendo clic en Crear regla .
Puede editar una regla existente haciendo clic en , luego realizando los cambios deseados y haciendo clic en Guardar regla .
Para obtener más información sobre las reglas de clasificación automática de Dependabot, consulte Acerca de las reglas de clasificación automática de Dependabot y Personalización de las reglas de clasificación automática para priorizar las alertas de Dependabot .

Agrupación de actualizaciones de seguridad de Dependabot
Dependabot puede agrupar todas las actualizaciones de seguridad sugeridas automáticamente en una única solicitud de incorporación de cambios. Para habilitar las actualizaciones de seguridad agrupadas, seleccione Actualizaciones de seguridad agrupadas . Para obtener más información sobre las actualizaciones agrupadas y las opciones de personalización, consulte Configuración de las actualizaciones de seguridad de Dependabot .

Habilitar actualizaciones de dependencias en ejecutores de GitHub Actions
Si tanto Dependabot como GitHub Actions están habilitados para los repositorios existentes en su organización, GitHub utilizará automáticamente ejecutores alojados en GitHub para ejecutar actualizaciones de dependencias para esos repositorios.

De lo contrario, para permitir que Dependabot use ejecutores de GitHub Actions para realizar actualizaciones de dependencia para todos los repositorios existentes en la organización, seleccione "Dependabot en ejecutores de Actions".

Para obtener más información, consulte Acerca de Dependabot en los ejecutores de GitHub Actions .

Para tener un mayor control sobre el acceso de Dependabot a sus registros privados y recursos de red internos, puede configurar Dependabot para que se ejecute en ejecutores autoalojados de GitHub Actions. Para obtener más información, consulte " Acerca de Dependabot en ejecutores de GitHub Actions " y " Administración de Dependabot en ejecutores autoalojados ".

Conceder a Dependabot acceso a repositorios privados e internos
Para actualizar las dependencias privadas de los repositorios de su organización, Dependabot necesita acceder a esos repositorios. Para otorgarle a Dependabot acceso al repositorio privado o interno deseado, desplácese hacia abajo hasta la sección "Otorgar acceso a Dependabot a repositorios privados" y, luego, use la barra de búsqueda para encontrar y seleccionar el repositorio deseado. Tenga en cuenta que otorgarle a Dependabot acceso a un repositorio significa que todos los usuarios de su organización tendrán acceso al contenido de ese repositorio a través de las actualizaciones de Dependabot. Para obtener más información sobre los ecosistemas compatibles con repositorios privados, consulte Ecosistemas y repositorios compatibles con Dependabot .

Configuración de los ajustes globales de escaneo de código
El escaneo de código es una función que se utiliza para analizar el código en un repositorio de GitHub y encontrar vulnerabilidades de seguridad y errores de codificación. Los problemas identificados mediante el análisis se muestran en el repositorio.

Puede personalizar varias configuraciones globales para el escaneo de código:

Recomendar el conjunto de consultas extendidas para la configuración predeterminada
Habilitar la corrección automática de Copilot para CodeQL
Habilitación de Copilot Autofix para herramientas de escaneo de códigos de terceros
Establecer un umbral de error para las comprobaciones de escaneo de código en las solicitudes de extracción
Recomendar el conjunto de consultas extendidas para la configuración predeterminada
El escaneo de código ofrece grupos específicos de consultas CodeQL, llamadas suites de consultas CodeQL, para ejecutar en su código. De forma predeterminada, se ejecuta la suite de consultas "Predeterminada". GitHub también ofrece la suite de consultas "Extendida", que contiene todas las consultas de la suite de consultas "Predeterminada", además de consultas adicionales con menor precisión y gravedad. Para sugerir la suite de consultas "Extendida" en toda su organización, seleccione Recomendar la suite de consultas extendida para repositorios que habiliten la configuración predeterminada . Para obtener más información sobre las suites de consultas integradas para la configuración predeterminada de CodeQL, consulte Suites de consultas CodeQL .

Habilitar la corrección automática de Copilot para CodeQL
Puede seleccionar Copilot Autofix para habilitar Copilot Autofix para todos los repositorios de su organización que utilicen la configuración predeterminada de CodeQL o la configuración avanzada de CodeQL. Copilot Autofix es una expansión del escaneo de código que sugiere correcciones para las alertas de escaneo de código. Para obtener más información, consulte Uso responsable de Copilot Autofix para escaneo de código .

Habilitación de Copilot Autofix para herramientas de escaneo de códigos de terceros
Nota

La compatibilidad con herramientas de escaneo de códigos de terceros se encuentra en versión preliminar pública y está sujeta a cambios. Actualmente, se admite la herramienta de terceros ESLint. Para obtener más información, consulte Uso responsable de Copilot Autofix para escaneo de códigos .

Puede seleccionar Copilot Autofix para herramientas de terceros para habilitar Copilot Autofix para todos los repositorios de su organización que utilicen herramientas de terceros. Copilot Autofix es una expansión del escaneo de código que sugiere correcciones para las alertas de escaneo de código.

Establecer un umbral de error para las comprobaciones de escaneo de código en las solicitudes de extracción
Puede elegir los niveles de gravedad en los que fallará la comprobación del escaneo de código en las solicitudes de extracción. Para elegir un nivel de gravedad de seguridad, seleccione el menú desplegable Seguridad: NIVEL DE GRAVEDAD DE SEGURIDAD y, a continuación, haga clic en un nivel de gravedad de seguridad. Para elegir un nivel de gravedad de alerta, seleccione el menú desplegable OTRO: NIVEL DE GRAVEDAD DE ALERTA y, a continuación, haga clic en un nivel de gravedad de alerta. Para obtener más información, consulte Acerca de las alertas de escaneo de código .

Configuración de los ajustes de escaneo secreto global
El escaneo secreto es una herramienta de seguridad que escanea todo el historial de Git de los repositorios, así como los problemas, solicitudes de extracción, discusiones y wikis en esos repositorios, en busca de secretos filtrados que se hayan confirmado accidentalmente, como tokens o claves privadas.

Puede personalizar varias configuraciones globales para el escaneo secreto:

Detección de secretos genéricos con escaneo de secretos Copilot
Agregar un enlace de recurso para confirmaciones bloqueadas
Definición de patrones personalizados
Detección de secretos genéricos con escaneo de secretos Copilot
La detección de secretos genéricos del escaneo de secretos de Copilot es una expansión del escaneo de secretos impulsada por IA que escanea y crea alertas para secretos no estructurados, como contraseñas. Para habilitar estos escaneos, seleccione Escanear en busca de secretos genéricos . Tenga en cuenta que los secretos genéricos suelen tener una tasa más alta de falsos positivos que otros tipos de alertas. Para obtener más información sobre los secretos genéricos, consulte Detección responsable de secretos genéricos con el escaneo de secretos de Copilot .

Nota

No necesita una suscripción a GitHub Copilot para utilizar la detección de secretos genéricos de Copilot Secret Scanning. Las funciones de Copilot Secret Scanning están disponibles para los repositorios privados en las empresas de GitHub Enterprise Cloud que tienen habilitada la seguridad avanzada de GitHub.

Agregar un enlace de recurso para confirmaciones bloqueadas
Para brindar contexto a los desarrolladores cuando el escaneo de secretos bloquea una confirmación, puede mostrar un vínculo con más información sobre el motivo por el cual se bloqueó la confirmación. Para incluir un vínculo, seleccione Agregar un vínculo de recurso en la CLI y la interfaz web cuando se bloquea una confirmación . En el cuadro de texto, escriba el vínculo al recurso deseado y luego haga clic en Guardar .

Definición de patrones personalizados
Puede definir patrones personalizados para el escaneo de secretos con expresiones regulares. Los patrones personalizados pueden identificar secretos que no son detectados por los patrones predeterminados admitidos por el escaneo de secretos. Para crear un patrón personalizado, haga clic en Nuevo patrón , luego ingrese los detalles de su patrón y haga clic en Guardar y ejecutar en seco . Para obtener más información sobre patrones personalizados, consulte Definición de patrones personalizados para el escaneo de secretos .

Creación de administradores de seguridad para su organización
El rol de administrador de seguridad otorga a los miembros de su organización la capacidad de administrar alertas y configuraciones de seguridad en toda la organización. Los administradores de seguridad pueden ver datos de todos los repositorios de su organización a través de la descripción general de seguridad.

Para obtener más información sobre el rol de administrador de seguridad, consulte Administrar administradores de seguridad en su organización .
