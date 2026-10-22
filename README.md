# Hispano ID

Distribución institucional para mostrar el nombre de la cuenta principal de Chrome en las páginas web compatibles.

## Instalación administrada

- ID: `kbcdbfkpcfghihghjhmmmicadfkgnlnd`
- Actualizaciones: `https://respchla.github.io/hispano-id/updates.xml`
- Versión: `2.0.7`

Destinada a Chrome administrado en Windows. Mantiene la instalación forzada, el cliente OAuth y los permisos `openid` y `https://www.googleapis.com/auth/userinfo.profile`. Cada perfil muestra el nombre de su cuenta principal, sin solicitar autorización interactiva al abrir una pestaña.

## Actualización 2.0.7

Nueva pestaña abre directamente **https://www.google.com/**. Se elimina la pantalla de bienvenida de Hispano ID introducida en 2.0.6. La página y el buscador son los originales de Google; Hispano ID añade únicamente la etiqueta del nombre verificado. La redirección no envía nombres, identificadores ni parámetros personalizados, y no deja una pantalla intermedia en el historial de Atrás.

La etiqueta conserva sus comprobaciones de cuenta, caducidad, renovación automática y ajuste al zoom. Ya no se consulta ni se muestra la identidad dentro de la página intermedia de la extensión. El cambio se distribuye por el canal existente sin modificar las políticas de instalación.

Pasaron 19 pruebas unitarias y las pruebas de Chrome aislado: destino de pestañas y ventanas nuevas, búsqueda, recarga, zoom y cambio de cuenta con identidades ficticias. Se verificó además la página pública real de Google tras abrir Nueva pestaña, mostrando la etiqueta de una cuenta ficticia. Las pruebas no confirman la recepción de la actualización en cada equipo administrado.

## Datos y alcance

El nombre se consulta directamente a Google y forma parte del contenido visible de las páginas compatibles. No se registra en este alojamiento. No se garantiza la etiqueta en otras páginas internas de Chrome, Chrome Web Store, visores protegidos o vídeos a pantalla completa. Incógnito queda excluido. Abrir google.com requiere conexión de red y no reproduce los accesos directos ni la personalización de la Nueva pestaña interna de Chrome.

Este repositorio contiene únicamente distribución pública, sin nombres de estudiantes, tokens ni claves privadas de firma. Conserva los paquetes anteriores. Las descargas se sirven mediante GitHub Pages.
