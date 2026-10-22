# Hispano ID

Distribución institucional para mostrar el nombre de la cuenta principal de Chrome en las páginas web compatibles y en Nueva pestaña de Hispano ID.

## Instalación administrada

- ID: `kbcdbfkpcfghihghjhmmmicadfkgnlnd`
- Actualizaciones: `https://respchla.github.io/hispano-id/updates.xml`
- Versión: `2.0.6`

Destinada a Chrome administrado en Windows. La instalación forzada y la autorización de Google se configuran por el administrador del colegio. Los permisos de Google se mantienen en `openid` y `https://www.googleapis.com/auth/userinfo.profile`. Cada perfil muestra el nombre de su propia cuenta principal; no se pide al estudiante escribir su nombre ni se inicia una autorización interactiva al abrir Nueva pestaña.

## Actualización 2.0.6

Incluye una Nueva pestaña de Hispano ID con búsqueda en Google, accesos a Classroom, Drive y Gmail, y el nombre verificado en la esquina inferior derecha. Utiliza el [mecanismo de reemplazo de Nueva pestaña de Chrome](https://developer.chrome.com/docs/extensions/develop/ui/override-chrome-pages). La búsqueda envía a Google únicamente el texto escrito, sin añadir el nombre de la cuenta.

La etiqueta comparte las comprobaciones de identidad, caducidad, renovación automática y ajuste de tamaño de las páginas web. Los avisos de cambio de cuenta y zoom llegan también a la página de la extensión; los avisos de zoom se limitan a su pestaña. La instalación conserva el ID, el cliente OAuth y los permisos existentes.

Validación: 19 pruebas unitarias y Chrome aislado con cuentas ficticias. Se comprobó el reemplazo real de Nueva pestaña y de una ventana nueva, búsqueda con caracteres especiales, etiqueta tras navegar a resultados, recarga, cierre y cambio de cuenta simulados, y ausencia de solicitudes de autorización interactivas. El ajuste de zoom se probó en el mismo documento abierto mediante su URL de extensión, porque Chrome rechaza `tabs.setZoom` sobre `chrome://newtab`. También pasaron las pruebas anteriores de páginas web, navegación, zoom y recuperación. Estas pruebas no confirman la recepción en cada equipo del colegio.

## Datos y alcance

No se guardan nombres, historial, contraseñas ni contenido de páginas en este alojamiento. El nombre se consulta directamente a Google y se muestra en la página, donde forma parte de sus píxeles. No se garantiza en otras páginas internas de Chrome, Chrome Web Store, visores protegidos o vídeos a pantalla completa. La extensión no reemplaza la Nueva pestaña de incógnito.

Este repositorio contiene únicamente archivos de distribución y conserva los paquetes anteriores. No contiene nombres de estudiantes, tokens de acceso ni la clave privada de firma. Las descargas se sirven mediante GitHub Pages.
