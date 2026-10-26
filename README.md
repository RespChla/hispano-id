# Hispano ID · Cuidado de los equipos

Versión **2.1.1** para los navegadores Windows administrados del Colegio Hispanoamericano.

Antes de navegar, muestra las reglas de cuidado del equipo, pide indicar a quién informar un daño y aceptar el compromiso de cuidado. Se identifica la cuenta principal de Chrome y se mantiene el nombre completo en la esquina inferior derecha de las páginas compatibles. Al aceptar, abre Google. La ventana de las reglas se maximiza una sola vez; después respeta los cambios manuales de tamaño.

## Distribución administrada

- ID: `kbcdbfkpcfghihghjhmmmicadfkgnlnd`
- Actualizaciones: `https://respchla.github.io/hispano-id/updates.xml`
- Aplicación prevista: LAB1 LENOVO, LAB2 ASUS, LAB3 ASUS, LAB4 HP, LAB5 HP, LAB6 HP y LAB7 HP.

Conserva el ID y el cliente OAuth institucional. La instalación forzada y la autorización administrativa se configuran en Google Admin. El estudiante usa su cuenta del colegio en el perfil de Chrome; no escribe su nombre ni autoriza individualmente la aplicación. El paquete por sí solo no demuestra recepción en todos los equipos.

## Datos y alcance

La extensión obtiene el nombre mediante `openid` y `userinfo.profile`. La aceptación se guarda localmente en el perfil con nombre, identificador de cuenta, fecha y versión del texto; conserva hasta 100 registros y descarta los de más de 90 días al guardar otro. No envía estos registros a GitHub ni a un servidor de recopilación. No incorpora captura de pantalla, teclado, ratón o historial. El aviso de supervisión se refiere a los sistemas del colegio.

La pantalla de reglas controla la navegación web de Chrome. No bloquea Windows ni demuestra por sí sola que una persona haya leído las reglas o causado un daño. El nombre no se garantiza en páginas internas o superficies protegidas de Chrome. Google Accounts permanece disponible para completar el acceso.

Este repositorio contiene archivos de distribución, sin claves privadas, tokens ni información de estudiantes.

## Aceptación según la UO (2.1.1)

`RequireCareAcceptance` es una política administrada de la extensión. Para una UO con inicio de sesión opcional, configurar en Google Admin → Hispano ID → Política de extensiones:

```json
{
  "RequireCareAcceptance": { "Value": false }
}
```

Con `false`, no se exige cuenta ni aceptación, Nueva pestaña abre Google y se retiran las redirecciones anteriores. Si hay una cuenta verificada, el nombre sigue visible. No se crea una aceptación ficticia. Los cambios se atienden sin reiniciar Chrome cuando llega la política.

En una UO donde se obliga a iniciar sesión, usar `true` (o dejar la política ausente para conservar el comportamiento existente). El valor lo controla el administrador; cerrar sesión no desactiva la obligación.

La política nativa `BrowserSignin` no se expone directamente a esta extensión. Cambiar solo su selector no sincroniza este ajuste: el administrador debe mantener ambos valores coordinados por UO. No se modifica la instalación forzada ni la obligación de iniciar sesión de Chrome.

Validación de 2.1.1: 39 pruebas aprobadas; mismo ID, firma, OAuth y permisos. La recepción de la versión y la política en cada equipo debe comprobarse por separado.
