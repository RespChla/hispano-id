# Hispano ID

Distribución de la extensión institucional para mostrar el nombre de la cuenta principal de Chrome en las páginas web compatibles.

## Instalación administrada

Esta distribución está destinada a los navegadores Windows administrados del Colegio Hispanoamericano. La instalación se configura desde Google Admin para las unidades organizativas seleccionadas.

- ID de la extensión: `kbcdbfkpcfghihghjhmmmicadfkgnlnd`
- Manifiesto de actualizaciones: `https://respchla.github.io/hispano-id/updates.xml`
- Versión: `2.0.4`

El estudiante debe usar su cuenta escolar en el perfil de Chrome. El administrador debe configurar la **instalación forzada**, que impide quitar o desactivar la extensión desde Chrome, y la autorización OAuth administrativa antes de desplegarla. El objetivo es que el nombre aparezca automáticamente, sin pedir consentimiento a cada estudiante. Cada perfil muestra su propio nombre y la etiqueta conserva su tamaño cuando cambia el zoom de la página. Google permite [autorizar clientes OAuth mediante delegación de todo el dominio](https://knowledge.workspace.google.com/admin/apps/control-api-access-with-domain-wide-delegation) para omitir el consentimiento individual. Los únicos permisos requeridos son `openid` y `https://www.googleapis.com/auth/userinfo.profile`. Esta autorización tiene alcance de dominio; la instalación puede limitarse a las UO seleccionadas. La publicación del paquete no aplica por sí sola estas políticas. Debe validarse primero con cuentas de prueba sin autorizaciones previas; si aparece un aviso, el despliegue aún no cumple el requisito.

## Actualización 2.0.4

La etiqueta se recupera cuando una página la elimina al reorganizar su diseño. La posición y el tamaño se ajustan al área visible tanto con el zoom de página como con la ampliación visual. Un fallo aislado de la consulta de zoom no descarta una identidad válida.

Se mantienen los mismos permisos y la caducidad del nombre. Se comprobaron en Chrome aislado el zoom de página de 25–500 %, la ampliación visual de 1,639–3×, las cuatro esquinas configurables, formularios largos, la reinyección, el cambio de cuenta y el cierre de sesión. Estas pruebas no sustituyen la comprobación en cada equipo administrado.

## Datos y alcance

Hispano ID consulta directamente a Google el nombre del perfil mediante los permisos `openid` y `userinfo.profile`. No registra historial, contraseñas ni contenido de páginas. El nombre se muestra dentro de la página visitada y forma parte de su contenido visible. No se garantiza su presencia en páginas internas de Chrome, documentos protegidos ni vídeos a pantalla completa. Este repositorio aloja únicamente archivos de distribución. No contiene nombres de estudiantes, tokens de acceso ni la clave privada usada para firmar las actualizaciones. Las descargas se sirven mediante GitHub Pages, sujeto a las políticas de privacidad de GitHub.
