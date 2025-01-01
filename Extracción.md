Acerca de comparar ramas en solicitudes de extracción
Las solicitudes de extracción muestran las diferencias para comparar los cambios que haz hecho en tu rama de tema respecto a la rama en la cual quieres fusionar tus cambios.

En este artículo
Opciones de diferentes vistas
No se mostrarán las diferencias de motivos
Comparaciones de diferencias de Git de tres puntos y de dos puntos
Acerca de la comparación de tres puntos en GitHub
Información adicional
Note

Al crear la solicitud de cambios, puedes modificar la rama base con la que comparas los cambios. Para más información, consulta Crear una solicitud de incorporación de cambios.

Puede ver los cambios propuestos en una solicitud de cambios en la pestaña Archivos cambiados. Captura de pantalla de las pestañas de una solicitud de cambios. La pestaña "Archivos cambiados" aparece resaltada en naranja oscuro.

En lugar de ver las confirmaciones de cambios, puedes ver los cambios propuestos ya que aparecerán en los archivos una vez que se fusiona la solicitud de extracción. Los archivos aparecen en orden alfabético en la pestaña Archivos cambiados. Las adiciones a los archivos aparecen en color verde y están precedidas por un signo +, mientras que el contenido que se ha eliminado aparece en color rojo y precedido por un signo -.

Opciones de diferentes vistas
Tip

Si te resulta difícil comprender el contexto de un cambio, puedes hacer clic en View en la pestaña de archivos modificados para ver el archivo completo con los cambios propuestos.

Tienes varias opciones para ver una diferencia:

La vista unificada muestra el contenido actualizado y el existente en conjunto en una vista lineal.
La vista en dos paneles muestra el contenido viejo de un lado y el contenido nuevo del otro.
La vista diferencia rica muestra una previsualización de cómo se verán los cambios una vez que se fusione la solicitud de extracción.
La vista de origen muestra los cambios en el origen sin el formato de la vista diferencia rica.
También puedes elegir ignorar los cambios de espacio en blanco para obtener una vista más precisa de los cambios sustanciales en una solicitud de extracción.

Captura de pantalla de la pestaña "Archivos cambiados" de una solicitud de incorporación de cambios. La pestaña "Vista de diferencias" está resaltada en naranja oscuro.

Para simplificar la revisión de cambios en una solicitud de cambios grande, puedes filtrar el diff para que solo muestre los tipos de archivo seleccionados, muestre menos archivos de los cuales seas CODEOWNER, oculte archivos que ya hayas visto, u oculte archivos borrados. Para más información, consulta Filtrar archivos en una solicitud de extracción.

Captura de pantalla del menú desplegable de filtro de archivos. El menú se expande y se resalta en naranja oscuro.

No se mostrarán las diferencias de motivos
Has excedido el límite total de archivos o de ciertos tipos de archivos. Para más información, consulta Límites de los repositorios.
Los archivos coinciden con una regla en el archivo .gitattributes del repositorio para impedir que ese archivo se muestre de manera predeterminada. Para más información, consulta Personalizar cómo aparecen los archivos cambiados en GitHub.
Comparaciones de diferencias de Git de tres puntos y de dos puntos
Hay dos métodos de comparación para el comando git diff; dos puntos (git diff A..B) y tres puntos (git diff A...B). Las solicitudes de incorporación de cambios en GitHub muestran una diferencia de tres puntos.

Comparación de diferencias de Git de tres puntos
La comparación de tres puntos muestra la diferencia entre la confirmación común más reciente de ambas ramas (base de combinación) y la versión más reciente de la rama puntual.

Comparación de diferencias de Git de dos puntos
La comparación de dos puntos muestra la diferencia entre el estado más reciente de la rama base (por ejemplo, main) y la versión más reciente de la rama puntual.

Para ver dos referencias confirmables en una comparación de diferencia de dos puntos en GitHub, puedes editar la URL de la página "Comparar cambios" de tu repositorio. Para más información, vea "committish" en el glosario de Git en el sitio del libro Pro Git.

Por ejemplo, esta dirección URL usa los códigos SHA abreviados para comparar las confirmaciones f75c570 y 3391dcc: https://github.com/github-linguist/linguist/compare/f75c570..3391dcc.

Una diferenciación de dos puntos compara dos referencias confirmables de Git, como SHA u OID (ID de objeto), directamente entre sí. En GitHub, las referencias confirmables de Git en una comparación de diferenciación de dos puntos se deben subir al mismo repositorio o a sus bifurcaciones.

Si quieres simular una diferenciación de dos puntos en una solicitud de extracción y ver una comparación entre las versiones más recientes de cada rama, puedes fusionar la rama base en tu rama de tema, que actualiza el último antepasado común entre tus ramas.

Para más información sobre los comandos de Git para comparar los cambios, consulta Opciones de diferencias de Git en el sitio del libro de Pro Git.

Acerca de la comparación de tres puntos en GitHub
Dado que la comparación de tres puntos realiza la comparación con la base de fusión mediante combinación, se centra en "lo que introduce una solicitud de cambios".

Cuando se usa una comparación de dos puntos, la diferencia cambia cuando se actualiza la rama base, incluso si no ha realizado ningún cambio en la rama puntual. Además, una comparación de dos puntos se centra en la rama base. Esto significa que todo lo que agregues se muestra como que falta en la rama base, como si fuera una eliminación y viceversa. Como resultado, los cambios que presenta la rama puntual se convierten en ambiguos.

Por el contrario, al comparar las ramas con la comparación de tres puntos, los cambios en la rama puntual siempre se encuentran en la diferencia si se actualiza la rama base, ya que la diferencia muestra todos los cambios desde que las ramas difieren.

Combinación con una periodicidad frecuente
Para evitar confundirse, combina la rama base (por ejemplo, main) en la rama puntual con frecuencia. Al combinar la rama base, las diferencias que muestran las comparaciones de dos puntos y tres puntos son las mismas. Se recomienda combinar una solicitud de incorporación de cambios lo antes posible. Esto anima a los colaboradores a que las solicitudes de incorporación de cambios sean más pequeñas, lo que en general es una práctica recomendada.

Información adicional
Acerca de las solicitudes de incorporación de cambios
Acerca de las bifurcaciones
