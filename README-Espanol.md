# PLATINEXOS

[English](README.md) | [Português (Brasil)](README-pt-BR.md) | [Español (Latinoamérica)](README-Espanol.md)

[Notas de la Release](Release/RELEASE-es-419.md) · [Seguridad](RELATORIO-DE-SEGURANCA-es-419.md) · [Steam Web API Key](Guia-Steam-Web-API-Key/GUIA-es-419.md) · [Capturas reales de la aplicación](IMAGENS-es-419.md)


**PLATINEXOS** es una aplicación gratuita e independiente para **Windows 11 x64**. Consulta tu biblioteca de Steam y el progreso de los logros, revisa indicadores y estadísticas y organiza favoritos y objetivos personales. La interfaz está disponible en portugués brasileño, inglés estadounidense y español latinoamericano.

La aplicación no desbloquea logros en Steam, no modifica juegos ni cambia archivos de partidas guardadas. No tiene afiliación, patrocinio ni aprobación de Valve Corporation. Steam es una marca de Valve Corporation.

PLATINEXOS se ofrece bajo una licencia gratuita para uso personal y no comercial, con código fuente propio cerrado, conforme a los [Términos de Uso](TERMOS-DE-USO-Espanol.md). Los componentes de terceros mantienen sus propias licencias.

## Descarga oficial y requisitos

Descarga el Portable en ZIP desde las [Releases oficiales de PLATINEXOS](https://github.com/Sandr0F/PLATINEXOS/releases).

- Windows 11 x64.
- Internet para sincronizar y obtener contenido remoto; los datos ya cargados pueden consultarse localmente conforme a las limitaciones de la aplicación.
- SteamID64 o URL de perfil y una clave válida de la Steam Web API para configurar la sincronización.

El paquete incluye .NET y Windows App SDK mediante una distribución autónoma (*self-contained*). No es necesario mantener abierto el cliente de Steam para consultar la Web API. El funcionamiento sin el cliente de Steam instalado se verificó anteriormente en un entorno Windows 10; la versión 1.0.0 se validó en Windows 11 x64. La detección opcional de juegos instalados depende de los archivos locales de Steam. Estos resultados no garantizan el funcionamiento en todas las instalaciones de Windows ni eliminan posibles requisitos de componentes nativos. No se han establecido requisitos mínimos de CPU, memoria o espacio libre sin mediciones.

## Extraer, verificar y ejecutar

1. Consulta los [Términos de Uso](TERMOS-DE-USO-Espanol.md), la [Política de Privacidad](POLITICA-DE-PRIVACIDADE-Espanol.md) y las [licencias de terceros](LICENCAS-DE-TERCEIROS.md).
2. Descarga el ZIP y el archivo `.sha256` de la misma Release oficial.
3. En PowerShell, desde la carpeta de descargas, ejecuta el siguiente comando, sustituyendo el nombre por el ZIP descargado, y compara el resultado con el archivo `.sha256`:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\nombre-del-archivo.zip'
   ```

4. Extrae **todo el contenido** a una carpeta de tu usuario. No ejecutes la aplicación desde el ZIP ni copies solamente el EXE.
5. Abre `Platinexos.exe` sin privilegios de administrador, consulta los documentos y decide si aceptas los términos presentados.

El ejecutable 1.0.0 no tiene firma digital. Windows puede mostrar advertencias: verifica el origen del archivo y no desactives las protecciones del sistema. SHA-256 verifica la integridad, pero no demuestra la identidad del editor.

## Configurar la Steam Web API

En **Configuración**, ingresa el SteamID64 o la URL del perfil y tu clave personal válida de la Steam Web API. Obtén la clave legítimamente desde tu propia cuenta en la [página oficial de Valve](https://steamcommunity.com/dev/apikey). Consulta tus propias cuentas o perfiles de terceros cuyos titulares hayan solicitado o autorizado la consulta. La aplicación no concede acceso a información privada.

- Ingresa la clave solamente en el campo correspondiente de PLATINEXOS. La aplicación no solicita la contraseña de Steam ni códigos de Steam Guard.
- Guardarla en el **Administrador de credenciales de Windows** es opcional. La clave no se almacena en SQLite, la caché ni las preferencias.
- **Guardar la clave no autoriza la sincronización automática.** Para sincronizar al iniciar, activa la autorización específica para la cuenta de Steam deseada. La opción empieza desmarcada, incluso para cuentas que ya tienen una clave guardada, y requiere una clave guardada disponible.
- Puedes revocar esa autorización en Configuración sin eliminar la clave. La sincronización manual sigue disponible.
- No compartas claves en Issues, informes ni capturas. Si se compromete una clave, revócala en el servicio oficial de Valve, registra otra y sustituye la anterior en la aplicación. Eliminarla de la aplicación no la revoca en Valve.

El propio usuario debe obtener la clave directamente de Valve y aceptar los términos del servicio. El usuario es responsable del registro, del dominio asociado cuando se solicite, del uso y de la confidencialidad de la clave. PLATINEXOS no tiene aprobación oficial conocida de Valve; el uso de `localhost` no demuestra tal aprobación. Valve podrá modificar, restringir, suspender o finalizar el acceso a la Steam Web API conforme a sus términos.

Los datos se almacenan por perfil de Windows. Extraer el Portable en otra carpeta no crea un perfil de datos aislado. Consulta la Política para entender el almacenamiento, los servicios externos y la eliminación separada de datos y credenciales.

## Actualizaciones de la edición Portable

Las actualizaciones se descargan manualmente mediante los canales oficiales. Esta edición no instala actualizaciones automáticamente.

## Documentos por idioma

| Idioma | Términos de Uso | Política de Privacidad |
|---|---|---|
| Portugués brasileño | [Termos de Uso](TERMOS-DE-USO.md) | [Política de Privacidade](POLITICA-DE-PRIVACIDADE.md) |
| English (United States) | [Terms of Use](TERMOS-DE-USO-English.md) | [Privacy Policy](POLITICA-DE-PRIVACIDADE-English.md) |
| Español latinoamericano | [Términos de Uso](TERMOS-DE-USO-Espanol.md) | [Política de Privacidad](POLITICA-DE-PRIVACIDADE-Espanol.md) |

- [Avisos de Derechos de Autor](AVISOS-DE-DIREITOS-AUTORAIS.md).
- [Índice de licencias de terceros](LICENCAS-DE-TERCEIROS.md).
- [Lista de archivos originales de licencia](LICENSE-FILES.txt).

Los Términos, las Políticas, el índice y los textos originales de licencias de este repositorio son copias íntegras de los documentos que acompañan al Portable aprobado. Los archivos HTML y RTF de licencias conservan sus formatos originales y pueden descargarse para su lectura. Las rutas `Legal/...` mencionadas en los textos se refieren a la estructura del ZIP; en esta página, los documentos y la carpeta `Licencas/` se encuentran en la raíz del repositorio documental.

## Soporte y contacto

Utiliza [GitHub Issues de PLATINEXOS](https://github.com/Sandr0F/PLATINEXOS/issues) para informar problemas y sugerir mejoras. El canal es público: no publiques contraseñas, claves de Steam, bases de datos personales, cachés ni otra información sensible.

Para comunicaciones privadas o asuntos de privacidad: [platinexos@gmail.com](mailto:platinexos@gmail.com).

Las contribuciones económicas son totalmente voluntarias y se destinan al desarrollo independiente. Ninguna función depende de un pago.

## Seguridad y confiabilidad

El paquete PLATINEXOS 1.0.0 registró **0/60 detecciones antivirus en VirusTotal** en el nuevo análisis del 25/11/2026, clasificación **Clean (Limpio) en Kaspersky OpenTIP** y **0/21 detecciones antivirus en OPSWAT MetaDefender**, con un resultado general de **No Threats Detected**.

[Consultar análisis en VirusTotal](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection). Enlace directo confirmado por el desarrollador en una ventana privada. No es necesario volver a subir el archivo. Los nombres de candidatos anteriores corresponden al mismo SHA-256.

```text
EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF
```

Estas son verificaciones seleccionadas. El [Informe detallado de seguridad](RELATORIO-DE-SEGURANCA-es-419.md) distingue los resultados antivirus de los indicadores de comportamiento, registra la alerta Sigma investigada y los módulos adicionales de MetaDefender que no completaron sus verificaciones. El SHA-256 y los archivos oficiales están en las [Releases de PLATINEXOS](https://github.com/Sandr0F/PLATINEXOS/releases).


## Capturas reales de la aplicación

![Resumen de la biblioteca de Steam y estadísticas de progreso](Imagens-Release-v3/01-App-Showcase/01-overview-en.png)

[Capturas reales de la aplicación](IMAGENS-es-419.md).

[Lectura de los documentos jurídicos y licencias originales](DOCUMENTOS-E-LICENCAS-es-419.md).
