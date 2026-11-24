# Política de Privacidad de PLATINEXOS 1.0.0

Última actualización: 23 de noviembre de 2026. Versión 1.0.0.

## Aplicación y finalidad

PLATINEXOS, desarrollado por Sandr0F, es una aplicación gratuita e independiente, sin afiliación con Valve Corporation. Utiliza datos de Steam para mostrar la biblioteca, los logros y el progreso. Los favoritos, los objetivos, las confirmaciones manuales y las preferencias se utilizan para organizar tu experiencia en la aplicación.

## Datos utilizados

Puedes proporcionar tu SteamID64 o la URL del perfil y una clave personal de la Steam Web API. Según lo que devuelva Steam, la aplicación puede consultar el identificador y el nombre del perfil, la biblioteca, los AppIDs, los metadatos de juegos, los nombres y las descripciones de logros, los íconos, el progreso y las fechas de desbloqueo. La aplicación también puede guardar fechas y resultados de sincronización, imágenes en caché, preferencias y los registros personales que crees.

La identificación opcional de juegos instalados lee los archivos y manifiestos locales del cliente de Steam. PLATINEXOS no modifica los juegos ni los archivos de partidas guardadas.

## Credenciales y sincronización al iniciar

La clave de la Steam Web API permanece en memoria durante la sesión, a menos que elijas guardarla en el Administrador de credenciales de Windows. En ese caso, queda asociada al usuario de Windows. La aplicación envía la clave al endpoint oficial de la Steam Web API para las operaciones que la requieren. La aplicación no solicita la contraseña de Steam ni códigos de Steam Guard y no guarda la clave en la base de datos SQLite, la caché ni las preferencias.

La sincronización al iniciar ocurre una vez y solo si la cuenta de Steam activa tiene autorización mediante **Sincronizar esta cuenta de Steam al abrir PLATINEXOS** y hay una clave guardada disponible. Guardar la clave es una decisión independiente. Desmarca esta opción en Configuración para revocar la autorización de la cuenta sin eliminar la clave. Sin autorización, puedes sincronizar manualmente con una clave válida, guardada o utilizada solo en memoria.

Si sospechas que la clave se ha visto comprometida, revócala y registra otra en la [página oficial de claves de la Steam Web API de Valve](https://steamcommunity.com/dev/apikey). Después, elimina la clave anterior guardada en PLATINEXOS e introduce la nueva. Eliminar la clave de la aplicación no la revoca en Valve.

## Dónde se guardan los datos

La aplicación mantiene SQLite, las preferencias y las cachés en la carpeta `%LOCALAPPDATA%\SteamAchievementTracker` del perfil de Windows en uso. La credencial guardada, si eliges guardarla, permanece en el Administrador de credenciales. La aceptación de los Términos de Uso se registra por separado en `%LOCALAPPDATA%\PLATINEXOS\terms-acceptance.json`, con la versión de los términos, el identificador del documento y la fecha y hora de aceptación en UTC. La autorización de sincronización al iniciar se guarda por cuenta de Steam en la subcarpeta `StartupSynchronization`, en el mismo perfil de Windows. Los archivos que la aplicación almacena localmente permanecen en el país donde se encuentra físicamente el dispositivo. El desarrollador no recibe estos archivos ni mantiene un servidor para almacenarlos. El tratamiento realizado por Valve y las copias hechas por el usuario o por servicios de respaldo siguen las reglas de esos servicios.

Las distintas cuentas de Windows utilizan perfiles locales separados. Las personas que comparten la misma cuenta de Windows pueden tener acceso a los datos guardados en ese perfil. La aplicación no cifra SQLite ni los archivos de caché.

La verificación manual de actualizaciones puede mantener un archivo de coordinación en `%LOCALAPPDATA%\PLATINEXOS\updates\check.lock`. La aplicación no utiliza este archivo para almacenar la clave ni datos de Steam.

## Conexiones externas y diagnóstico

Las consultas a la Steam Web API transmiten a Valve la clave de la API y los identificadores y parámetros necesarios para la operación, según el tipo de consulta. El tratamiento realizado por Valve es independiente del almacenamiento local de PLATINEXOS. La tienda y las redes de distribución de contenido de Steam pueden recibir solicitudes para buscar metadatos, portadas e íconos. Al iniciar, la firma by Sandr0F puede consultar por HTTPS el [perfil público de Steam de Sandr0F](https://steamcommunity.com/id/Sandr0F/) en formato XML (`?xml=1`) y descargar su avatar de los servidores de imágenes de Steam. Esta consulta no utiliza la clave de la Steam Web API del usuario. Estos servicios pueden recibir información de la conexión, como la dirección IP. Los enlaces abiertos en el navegador, incluidas las guías y las opciones de contribución voluntaria, siguen las políticas de los sitios correspondientes. [Política de Privacidad de Valve](https://store.steampowered.com/privacy_agreement/)

PLATINEXOS no implementa telemetría propia, publicidad ni envío automático de informes al desarrollador. El diagnóstico detallado de la Steam Web API es opcional y se presenta en la aplicación antes de su ejecución. Revisa cualquier informe antes de compartirlo.

En la modalidad Portable, el botón Buscar actualizaciones consulta la API pública de GitHub para comprobar las Releases de Sandr0F/PLATINEXOS, sin enviar la clave de la Steam Web API. Esta consulta es manual y puede transmitir información de conexión a GitHub; no descarga ni instala actualizaciones automáticamente.

## Retención y control

El almacenamiento local permite consultar datos ya cargados sin volver a sincronizar. La aplicación no elimina estos registros automáticamente después de un plazo. Para guardar una copia de la base de datos local, cierra la aplicación antes de hacer el respaldo.

**Cómo detener futuras sincronizaciones automáticas:** selecciona la cuenta de Steam en Configuración y desmarca **Sincronizar esta cuenta de Steam al abrir PLATINEXOS**. La clave guardada y los datos ya sincronizados se conservan. Puedes eliminar la clave por separado.

**Cómo eliminar los datos locales:** cierra PLATINEXOS por completo. Si lo deseas, haz antes una copia de respaldo. Después, en el Explorador de archivos, abre `%LOCALAPPDATA%\SteamAchievementTracker` y elimina los archivos de esa carpeta que no quieras conservar. Para borrar todos los archivos de la aplicación almacenados en esa carpeta, elimina la carpeta completa. Esta operación puede eliminar permanentemente la base de datos SQLite, las preferencias, los objetivos, las confirmaciones manuales, las autorizaciones de sincronización al iniciar y las cachés, según los archivos presentes. No la realices si hay información que quieras conservar. Para eliminar también el registro local de aceptación de los Términos de Uso, elimina por separado `%LOCALAPPDATA%\PLATINEXOS\terms-acceptance.json`, si existe; esta eliminación podría requerir una nueva aceptación al abrir la aplicación. Elimina por separado cualquier clave almacenada en el Administrador de credenciales de Windows, preferentemente desde la propia aplicación. Eliminar archivos locales no elimina los datos que conserva Valve ni las copias de respaldo hechas por terceros.

Estas instrucciones se refieren al almacenamiento conocido de la versión 1.0.0 y no eliminan automáticamente los datos de servicios externos.

## Contacto y soporte

Para dudas técnicas generales, utiliza [GitHub Issues del repositorio público de PLATINEXOS](https://github.com/Sandr0F/PLATINEXOS/issues) cuando ese repositorio esté disponible. **Este canal es público. No publiques claves, bases de datos locales, identificadores personales, informes sin revisar ni capturas sensibles.**

**Contacto privado para privacidad:** [platinexos@gmail.com](mailto:platinexos@gmail.com). Utiliza esta dirección para solicitudes que involucren datos personales. No envíes esos datos al GitHub Issues público.
