# PLATINEXOS 1.0.0 — Windows 11 x64 Portable

[English](../README.md) | [Português (Brasil)](../README-pt-BR.md) | [Español (Latinoamérica)](../README-Espanol.md)


**PLATINEXOS** is a free, independent application for tracking your Steam game library and achievement progress. It is not affiliated with, sponsored by, or endorsed by Valve Corporation. Steam is a trademark of Valve. The application does not unlock achievements on Steam, modify games, or alter save files.

## Features

- Steam library with search, filters, indicators, and statistics.
- Achievement, progress, and official data lookup using information provided by Steam.
- Favorites and personal goals associated with the corresponding account.
- Manual synchronization through the Steam Web API; synchronization on launch is available only with account-specific authorization and an available saved key.
- Interface in Brazilian Portuguese, US English, and Latin American Spanish.
- Terms of Use, Privacy Policy, and third-party license viewer within the application.
- Manual update checks for the Portable edition through public `Sandr0F/PLATINEXOS` Releases, without automatic download or installation.

## Known requirements and limitations

- **Windows 11 x64**.
- Extract the entire ZIP to a folder accessible to the user.
- Internet access to synchronize and retrieve remote content; previously loaded data can be viewed offline as described in the manual.
- A SteamID64 or profile URL and a valid Steam Web API key for authenticated queries. Key availability is subject to Valve's conditions; returned data depends on profile privacy settings and service availability.

The package includes .NET and the Windows App SDK through self-contained deployment. The Steam client does not need to remain open to query the Web API. Running the application without the Steam client installed was previously verified in a Windows 10 environment; version 1.0.0 was validated on Windows 11 x64. Optional installed-game detection depends on local Steam files. These results do not guarantee operation on every Windows installation or eliminate potential native-component requirements. Minimum CPU, memory, and free-space specifications have not been established without measurement.

The version 1.0.0 executable is not digitally signed. Verify the download source and keep Windows security protections enabled. SHA-256 verifies file integrity, not the publisher's identity.

## How to use the Portable edition

Use the attachments included with this Release:

1. Download the ZIP and its `.sha256` file exclusively from the [official Releases](https://github.com/Sandr0F/PLATINEXOS/releases).
2. In PowerShell, from the download folder, run:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\PLATINEXOS-1.0.0-win-x64-Portable.zip'
   ```

3. Compare the result with the SHA-256 below and the verification file.
4. Extract the **entire** ZIP to a folder under your user profile. Do not run it from inside the ZIP or copy only the EXE.
5. Open `Platinexos.exe`, read the documents, and decide whether to accept the terms presented.
6. Follow `LEIA-ME.txt` and configure your account under **Settings**.

The Portable edition stores data per Windows user profile. Extracting another copy to a different folder does not create a separate data profile. Do not delete existing data to update without first checking the instructions and preserving anything you wish to keep.

## Configure Steam integration

Obtain your key legitimately from [Valve's official page](https://steamcommunity.com/dev/apikey) using your own Steam account. Query your own accounts or profiles whose owners have requested or authorized the lookup; the application does not grant access to private information.

Under Settings, enter the SteamID64 or profile URL and the key in the appropriate field. Do not provide your Steam password or Steam Guard codes.

- Saving the key in Windows Credential Manager is **optional**.
- The **Synchronize this Steam account when PLATINEXOS starts** authorization is separate from saving the key, is off by default, and can be revoked for each account.
- Without explicit startup authorization, manual synchronization remains available.
- Do not publish your key in Issues, screenshots, messages, or reports.
- If you suspect compromise, revoke the key through Valve's official service, register a new one, and replace the old key in the application. Removing it from the application does not revoke it at Valve.

## Terms, privacy, and licenses

The package contains the Terms and Privacy Policies in all three languages under `Legal/`, along with `Legal/AVISOS-DE-DIREITOS-AUTORAIS.md`, `Legal/LICENCAS-DE-TERCEIROS.md`, and the original license texts under `Legal/Licencas/`. Read the complete documents and applicable conditions before accepting. Third-party notices and rights are preserved.

The application stores its files in the Windows user profile, with optional credentials stored separately in the Windows vault. The Privacy Policy explains external communications and deletion instructions; deleting a local folder neither revokes the key at Valve nor deletes data held by external services.

© 2026 Sandr0F — PLATINEXOS. This attribution does not grant the developer rights to third-party components. Free distribution does not imply publication of the private source code or an automatic grant of rights to it.

## Support

Use [GitHub Issues](https://github.com/Sandr0F/PLATINEXOS/issues) for problems and suggestions. This is a public channel: do not share keys, passwords, personal databases, caches, or sensitive information. For private and privacy-related matters: [platinexos@gmail.com](mailto:platinexos@gmail.com).

Contributions to independent development are voluntary and do not affect access to features.

## Security and trust

PLATINEXOS 1.0.0 is a free, independent application developed to track Steam games, achievements, and progress.

Before release, the application underwent functional testing, integrity checks, and security analyses performed by specialized platforms.

**Security analysis results:**

- **VirusTotal:** none of the 60 antivirus engines detected threats in the analyzed package (0/60).
- **Kaspersky OpenTIP:** file classified as **Clean**.
- **OPSWAT MetaDefender:** no detections among the 21 antivirus engines reported (0/21), with an overall result of **No Threats Detected**.

The package also underwent technical inspections of its components and dependencies, with no malicious behavior identified that would warrant changes to the application.

PLATINEXOS does not request Steam passwords or Steam Guard codes. Steam integration uses a personal Steam Web API key, with the option to store it securely in Windows Credential Manager.

The platform reports are available for consultation. The official SHA-256 allows users to verify the integrity of the distributed file by comparing it with the approved original package.

| Platform | Selected result | How to check |
|---|---|---|
| VirusTotal | **0/60 antivirus detections** — reanalysis on November 25, 2026 | [View VirusTotal analysis](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection) |
| Kaspersky OpenTIP | **Clean** — final ZIP package | [File report](https://opentip.kaspersky.com/EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF/results?tab=upload) |
| OPSWAT MetaDefender Cloud | **0/21 antivirus detections**, overall result **No Threats Detected** | [File report](https://metadefender.com/results/hash/EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF/overview) |

The figures above refer to antivirus results. VirusTotal also recorded a Sigma behavioral indicator that was investigated, and some additional MetaDefender modules did not complete their checks. See the evidence and scope of these checks in the [public security document](../RELATORIO-DE-SEGURANCA-en-US.md), which presents the three selected platforms without claiming to be a complete history of all audits.

## How to view the reports

[View VirusTotal analysis](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection). Direct report link confirmed by the developer in an incognito window. No new upload is needed. Earlier candidate names refer to the same SHA-256.

## Approved file integrity

- Portable file: `PLATINEXOS-1.0.0-win-x64-Portable.zip`.
- Size: **105,398,429 bytes**.
- Contents: **575 files**.
- SHA-256:

```text
EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF
```

Verification file: `PLATINEXOS-1.0.0-win-x64-Portable.zip.sha256`.

Public documentation: [Terms of Use](../TERMOS-DE-USO-English.md), [Privacy Policy](../POLITICA-DE-PRIVACIDADE-English.md), [third-party licenses index](../LICENCAS-DE-TERCEIROS.md), and [Copyright Notices](../AVISOS-DE-DIREITOS-AUTORAIS.md).


[Real application screenshots](../IMAGENS-en-US.md) · [Steam Web API Key](../Guia-Steam-Web-API-Key/GUIA-en-US.md) · [Reading the legal documents and original licenses](../DOCUMENTOS-E-LICENCAS-en-US.md)
