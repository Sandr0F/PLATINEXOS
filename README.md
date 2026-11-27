# PLATINEXOS

[English](README.md) | [Português (Brasil)](README-pt-BR.md) | [Español (Latinoamérica)](README-Espanol.md)

[Release notes](Release/RELEASE-en-US.md) · [Security](RELATORIO-DE-SEGURANCA-en-US.md) · [Steam Web API Key](Guia-Steam-Web-API-Key/GUIA-en-US.md) · [Real application screenshots](IMAGENS-en-US.md)


**PLATINEXOS** is a free, independent application for **Windows 11 x64**. Track your Steam library and achievement progress, view indicators and statistics, and organize favorites and personal goals. The interface is available in Brazilian Portuguese, American English and Latin American Spanish.

The application does not unlock achievements on Steam, modify games or change save files. It is not affiliated with, sponsored by or endorsed by Valve Corporation. Steam is a trademark of Valve Corporation.

PLATINEXOS is provided under a free-of-charge license for personal and non-commercial use, with closed proprietary source code, as set out in the [Terms of Use](TERMOS-DE-USO-English.md). Third-party components retain their own licenses.

## Official download and requirements

Download the Portable ZIP from the [official PLATINEXOS Releases](https://github.com/Sandr0F/PLATINEXOS/releases).

- Windows 11 x64.
- Internet access for synchronization and remote content; previously loaded data can be viewed locally subject to the application's limitations.
- A SteamID64 or profile URL and a valid Steam Web API key to configure synchronization.

The package includes .NET and the Windows App SDK through self-contained deployment. The Steam client does not need to remain open to query the Web API. Running the application without the Steam client installed was previously verified in a Windows 10 environment; version 1.0.0 was validated on Windows 11 x64. Optional installed-game detection depends on local Steam files. These results do not guarantee operation on every Windows installation or eliminate potential native-component requirements. Minimum CPU, memory, and free-space specifications have not been established without measurement.

## Extract, verify and run

1. Read the [Terms of Use](TERMOS-DE-USO-English.md), [Privacy Policy](POLITICA-DE-PRIVACIDADE-English.md) and [third-party licenses](LICENCAS-DE-TERCEIROS.md).
2. Download the ZIP and `.sha256` file from the same official Release.
3. In PowerShell, from your download folder, run the command below, replacing the filename with the downloaded ZIP, and compare the result with the `.sha256` file:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\filename.zip'
   ```

4. Extract **all contents** to a folder in your user account. Do not run from inside the ZIP or copy only the EXE.
5. Open `Platinexos.exe` without administrator privileges, read the documents and decide whether to accept the terms presented.

The 1.0.0 executable is not digitally signed. Windows may display warnings: check the file's origin and do not disable system protections. SHA-256 verifies integrity but does not establish the publisher's identity.

## Configure the Steam Web API

In **Settings**, enter the SteamID64 or profile URL and your valid personal Steam Web API key. Obtain the key legitimately through your own account on [Valve's official page](https://steamcommunity.com/dev/apikey). Query your own accounts or third-party profiles whose holders have requested or authorized the query. The application does not grant access to private information.

- Enter the key only in PLATINEXOS's dedicated field. The application does not ask for a Steam password or Steam Guard codes.
- Saving it in **Windows Credential Manager** is optional. The key is not stored in SQLite, the cache or preferences.
- **Saving the key does not authorize automatic synchronization.** To sync at startup, enable the separate authorization for the desired Steam account. The option starts unchecked, including for accounts that already have a saved key, and requires a saved key to be available.
- You can revoke this authorization in Settings without deleting the key. Manual synchronization remains available.
- Do not share keys in Issues, reports or screenshots. If compromised, revoke the key through Valve's official service, register another and replace the old key in the application. Removing it from the application does not revoke it at Valve.

The user must obtain the key directly from Valve and accept the service's terms. The user is responsible for registration, the associated domain when requested, use of the key and its confidentiality. PLATINEXOS has no known official approval from Valve; using `localhost` does not establish such approval. Valve may modify, restrict, suspend or terminate access to the Steam Web API under its terms.

Data is stored per Windows user profile. Extracting the Portable to another folder does not create an isolated data profile. Read the Policy to understand storage, external services and the separate removal of data and credentials.

## Portable edition updates

Updates are downloaded manually through official channels. This edition does not install updates automatically.

## Documents by language

| Language | Terms of Use | Privacy Policy |
|---|---|---|
| Brazilian Portuguese | [Termos de Uso](TERMOS-DE-USO.md) | [Política de Privacidade](POLITICA-DE-PRIVACIDADE.md) |
| English (United States) | [Terms of Use](TERMOS-DE-USO-English.md) | [Privacy Policy](POLITICA-DE-PRIVACIDADE-English.md) |
| Latin American Spanish | [Términos de Uso](TERMOS-DE-USO-Espanol.md) | [Política de Privacidad](POLITICA-DE-PRIVACIDADE-Espanol.md) |

- [Copyright Notices](AVISOS-DE-DIREITOS-AUTORAIS.md).
- [Third-party license index](LICENCAS-DE-TERCEIROS.md).
- [List of original license files](LICENSE-FILES.txt).

The Terms, Policies, index and original license texts in this repository are complete copies of the documents accompanying the approved Portable. HTML and RTF license files retain their original formats and can be downloaded for reading. Paths beginning with `Legal/...` in those texts refer to the ZIP layout; on this page, the documents and `Licencas/` folder are at the documentation repository's root.

## Support and contact

Use [PLATINEXOS GitHub Issues](https://github.com/Sandr0F/PLATINEXOS/issues) to report problems and suggest improvements. This channel is public: do not post passwords, Steam keys, personal databases, caches or other sensitive information.

For private communications or privacy matters: [platinexos@gmail.com](mailto:platinexos@gmail.com).

Financial contributions are entirely voluntary and support independent development. No feature requires payment.

## Security and reliability

The PLATINEXOS 1.0.0 package recorded **0/60 antivirus detections on VirusTotal** in the November 25, 2026 reanalysis, a **Clean classification on Kaspersky OpenTIP**, and **0/21 antivirus detections on OPSWAT MetaDefender**, with an overall result of **No Threats Detected**.

[View VirusTotal analysis](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection). Direct report link confirmed by the developer in an incognito window. No new upload is needed. Earlier candidate names refer to the same SHA-256.

```text
EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF
```

These are selected checks. The [Detailed security report](RELATORIO-DE-SEGURANCA-en-US.md) distinguishes antivirus results from behavioral indicators, records the investigated Sigma alert and identifies additional MetaDefender modules that did not complete their checks. The SHA-256 and official files are available through [PLATINEXOS Releases](https://github.com/Sandr0F/PLATINEXOS/releases).


## Real application screenshots

![Steam library overview and progress statistics](Imagens-Release-v3/01-App-Showcase/01-overview-en.png)

[Real application screenshots](IMAGENS-en-US.md).

[Reading the legal documents and original licenses](DOCUMENTOS-E-LICENCAS-en-US.md).
