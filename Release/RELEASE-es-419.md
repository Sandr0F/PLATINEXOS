# PLATINEXOS 1.0.0 — Windows 11 x64 Portable

[English](../README.md) | [Português (Brasil)](../README-pt-BR.md) | [Español (Latinoamérica)](../README-Espanol.md)


**PLATINEXOS** es una aplicación gratuita e independiente para seguir tu biblioteca de juegos y tu progreso en los logros de Steam. No está afiliada, patrocinada ni aprobada por Valve Corporation. Steam es una marca de Valve. La aplicación no desbloquea logros en Steam, no modifica juegos ni altera archivos de partidas guardadas.

## Funcionalidades

- Biblioteca de Steam con búsqueda, filtros, indicadores y estadísticas.
- Consulta de logros, progreso y datos oficiales proporcionados por Steam.
- Favoritos y objetivos personales asociados a la cuenta correspondiente.
- Sincronización manual mediante Steam Web API y sincronización al iniciar solo con autorización específica para la cuenta y una clave guardada disponible.
- Interfaz en portugués de Brasil, inglés de Estados Unidos y español latinoamericano.
- Términos de Uso, Política de Privacidad y consulta de licencias de terceros dentro de la aplicación.
- Comprobación manual de actualizaciones de la edición Portable mediante las Releases públicas de `Sandr0F/PLATINEXOS`, sin descarga ni instalación automáticas.

## Requisitos y limitaciones conocidos

- **Windows 11 x64**.
- Extracción completa del ZIP en una carpeta accesible para el usuario.
- Internet para sincronizar y obtener contenido remoto; los datos cargados previamente pueden consultarse sin conexión, según el manual.
- SteamID64 o URL del perfil y clave válida de Steam Web API para consultas autenticadas. La obtención de la clave depende de las condiciones de Valve; los datos devueltos dependen de la privacidad del perfil y la disponibilidad de los servicios.

El paquete incluye .NET y Windows App SDK mediante una distribución autónoma (*self-contained*). No es necesario mantener abierto el cliente de Steam para consultar la Web API. El funcionamiento sin el cliente de Steam instalado se verificó anteriormente en un entorno Windows 10; la versión 1.0.0 se validó en Windows 11 x64. La detección opcional de juegos instalados depende de los archivos locales de Steam. Estos resultados no garantizan el funcionamiento en todas las instalaciones de Windows ni eliminan posibles requisitos de componentes nativos. No se han establecido requisitos mínimos de CPU, memoria o espacio libre sin mediciones.

El ejecutable 1.0.0 no cuenta con firma digital. Comprueba el origen de la descarga y mantén activadas las protecciones de Windows. El SHA-256 confirma la integridad, no la identidad del editor.

## Cómo utilizar la edición Portable

Utiliza los archivos adjuntos a esta Release:

1. Descarga el ZIP y su archivo `.sha256` exclusivamente desde las [Releases oficiales](https://github.com/Sandr0F/PLATINEXOS/releases).
2. En PowerShell, desde la carpeta de descarga, ejecuta:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\PLATINEXOS-1.0.0-win-x64-Portable.zip'
   ```

3. Compara el resultado con el SHA-256 indicado más abajo y con el archivo de verificación.
4. Extrae **todo** el ZIP a una carpeta de tu perfil de usuario. No lo ejecutes desde el ZIP ni copies únicamente el EXE.
5. Abre `Platinexos.exe`, lee los documentos y decide si aceptas los términos presentados.
6. Sigue `LEIA-ME.txt` y configura tu cuenta en **Configuración**.

La edición Portable conserva los datos por perfil de usuario de Windows. Extraer otra copia en una carpeta distinta no crea un perfil de datos separado. No elimines los datos existentes para actualizar sin consultar antes las instrucciones y conservar lo que desees mantener.

## Configurar la integración con Steam

Obtén tu clave legítimamente en la [página oficial de Valve](https://steamcommunity.com/dev/apikey), utilizando tu propia cuenta de Steam. Consulta tus propias cuentas o perfiles cuyos titulares hayan solicitado o autorizado la consulta; la aplicación no concede acceso a información privada.

En Configuración, introduce el SteamID64 o la URL del perfil y la clave en el campo correspondiente. No proporciones tu contraseña de Steam ni códigos de Steam Guard.

- Guardar la clave en el Administrador de credenciales de Windows es **opcional**.
- La autorización **Sincronizar esta cuenta de Steam al iniciar PLATINEXOS** es independiente de guardar la clave, está desactivada de forma predeterminada y puede revocarse para cada cuenta.
- Sin autorización específica al iniciar, sigue disponible la sincronización manual.
- No publiques tu clave en Issues, capturas de pantalla, mensajes ni informes.
- Si sospechas que la clave se ha comprometido, revócala en el servicio oficial de Valve, registra otra y reemplaza la anterior en la aplicación. Eliminarla de la aplicación no la revoca en Valve.

## Términos, privacidad y licencias

El paquete contiene los Términos y las Políticas de Privacidad en los tres idiomas dentro de `Legal/`, además de `Legal/AVISOS-DE-DIREITOS-AUTORAIS.md`, `Legal/LICENCAS-DE-TERCEIROS.md` y los textos originales en `Legal/Licencas/`. Consulta los documentos completos y las condiciones aplicables antes de aceptarlos. Se mantienen los avisos y derechos de terceros.

La aplicación almacena sus archivos en el perfil de usuario de Windows y las credenciales opcionales por separado en el almacén seguro de Windows. La Política explica las comunicaciones externas y las instrucciones de eliminación; borrar una carpeta local no revoca la clave en Valve ni elimina datos de servicios externos.

© 2026 Sandr0F — PLATINEXOS. Esta identificación no atribuye al desarrollador derechos sobre componentes de terceros. La gratuidad no implica la publicación del código fuente privado ni la concesión automática de derechos sobre él.

## Soporte

Utiliza [GitHub Issues](https://github.com/Sandr0F/PLATINEXOS/issues) para comunicar problemas y sugerencias. Es un canal público: no envíes claves, contraseñas, bases de datos personales, cachés ni información sensible. Para asuntos privados y de privacidad: [platinexos@gmail.com](mailto:platinexos@gmail.com).

Las contribuciones al desarrollo independiente son voluntarias y no condicionan las funcionalidades.

## Seguridad y confiabilidad

PLATINEXOS 1.0.0 es una aplicación gratuita e independiente, desarrollada para seguir juegos, logros y progreso en Steam.

Antes de su lanzamiento, la aplicación pasó por pruebas funcionales, verificaciones de integridad y análisis de seguridad realizados por plataformas especializadas.

**Resultados de los análisis de seguridad:**

- **VirusTotal:** ninguno de los 60 motores antivirus detectó amenazas en el paquete analizado (0/60).
- **Kaspersky OpenTIP:** archivo clasificado como **Clean (Limpio)**.
- **OPSWAT MetaDefender:** ninguna detección entre los 21 motores antivirus mostrados (0/21), con resultado general **No Threats Detected**.

El paquete también pasó por inspecciones técnicas de sus componentes y dependencias, sin que se identificara un comportamiento malicioso que justificara modificaciones en la aplicación.

PLATINEXOS no solicita contraseñas de Steam ni códigos de Steam Guard. La integración con Steam utiliza una clave personal de Steam Web API, con la opción de guardarla de forma segura en el Administrador de credenciales de Windows.

Los informes de las plataformas están disponibles para consulta. El SHA-256 oficial permite verificar la integridad del archivo distribuido al compararlo con el paquete original aprobado.

| Plataforma | Resultado seleccionado | Consulta |
|---|---|---|
| VirusTotal | **0/60 detecciones antivirus** — nuevo análisis del 25/11/2026 | [Consultar análisis en VirusTotal](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection) |
| Kaspersky OpenTIP | **Clean (Limpio)** — ZIP definitivo | [Informe del archivo](https://opentip.kaspersky.com/EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF/results?tab=upload) |
| OPSWAT MetaDefender Cloud | **0/21 detecciones antivirus**, resultado general **No Threats Detected** | [Informe del archivo](https://metadefender.com/results/hash/EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF/overview) |

Las cifras anteriores corresponden a resultados antivirus. VirusTotal también registró un indicador de comportamiento Sigma que se investigó, y algunos módulos adicionales de MetaDefender no completaron sus verificaciones. Consulta las evidencias y el alcance de estas verificaciones en el [documento público de seguridad](../RELATORIO-DE-SEGURANCA-es-419.md), que presenta las tres plataformas seleccionadas sin declararse un historial completo de todas las auditorías.

## Cómo consultar los informes

[Consultar análisis en VirusTotal](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection). Enlace directo confirmado por el desarrollador en una ventana privada. No es necesario volver a subir el archivo. Los nombres de candidatos anteriores corresponden al mismo SHA-256.

## Integridad del archivo aprobado

- Archivo Portable: `PLATINEXOS-1.0.0-win-x64-Portable.zip`.
- Tamaño: **105.398.429 bytes**.
- Contenido: **575 archivos**.
- SHA-256:

```text
EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF
```

Archivo de verificación: `PLATINEXOS-1.0.0-win-x64-Portable.zip.sha256`.

Documentación pública: [Términos de Uso](../TERMOS-DE-USO-Espanol.md), [Política de Privacidad](../POLITICA-DE-PRIVACIDADE-Espanol.md), [índice de licencias de terceros](../LICENCAS-DE-TERCEIROS.md) y [Avisos de Derechos de Autor](../AVISOS-DE-DIREITOS-AUTORAIS.md).


[Capturas reales de la aplicación](../IMAGENS-es-419.md) · [Steam Web API Key](../Guia-Steam-Web-API-Key/GUIA-es-419.md) · [Lectura de los documentos jurídicos y licencias originales](../DOCUMENTOS-E-LICENCAS-es-419.md)
