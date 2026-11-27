# PLATINEXOS 1.0.0 Privacy Policy

Last updated: November 24, 2026. Version 1.0.0.

## Application and purpose

PLATINEXOS, developed by Sandr0F, is a free, independent application with no affiliation with Valve Corporation. It uses Steam data to display your library, achievements, and progress. Favorites, goals, manual confirmations, and preferences are used to organize your experience in the application.

## Data used

You can provide your SteamID64 or profile URL and a personal Steam Web API key. Depending on what Steam returns, the application may retrieve the profile identifier and name, library, AppIDs, game metadata, achievement names and descriptions, icons, progress, and unlock dates. The application may also store synchronization dates and results, cached images, preferences, and personal records you create.

Optional detection of installed games reads the Steam client's local files and manifests. PLATINEXOS does not modify games or save files.

## Credentials and synchronization at startup

The Steam Web API key stays in memory during the session unless you choose to save it in Windows Credential Manager. In that case, it is associated with the Windows user. The application sends the key to the official Steam Web API endpoint for operations that require it. The application does not ask for your Steam password or Steam Guard codes and does not store the key in the SQLite database, cache, or preferences.

Synchronization at startup takes place once and only if the active Steam account is authorized through **Sync this Steam account when PLATINEXOS opens** and a saved key is available. Saving the key is a separate decision. Clear this option in Settings to revoke authorization for the account without removing the key. Without authorization, you can sync manually with a valid key, either saved or used only in memory.

If you suspect that the key has been compromised, revoke it and register another on [Valve's official Steam Web API key page](https://steamcommunity.com/dev/apikey). Then remove the old key saved in PLATINEXOS and enter the new one. Removing the key from the application does not revoke it with Valve.

## Where data is stored

The application keeps SQLite, preferences, and caches in the `%LOCALAPPDATA%\SteamAchievementTracker` folder of the Windows profile in use. The saved credential, if you choose to save it, is kept in Windows Credential Manager. Acceptance of the Terms of Use is recorded separately in `%LOCALAPPDATA%\PLATINEXOS\terms-acceptance.json`, with the terms version, document identifier, and acceptance date and time in UTC. Startup synchronization authorization is stored per Steam account in the `StartupSynchronization` subfolder in the same Windows profile. The files that the application stores locally remain in the country where the device is physically located. The developer does not receive these files or maintain a server to store them. Processing by Valve and copies made by the user or backup services follow those services' rules.

Different Windows accounts use separate local profiles. People sharing the same Windows account may have access to data stored in that profile. The application does not encrypt SQLite or cache files.

Manual update checks may keep a coordination file at `%LOCALAPPDATA%\PLATINEXOS\updates\check.lock`. The application does not use this file to store the key or Steam data.

## External connections and diagnostics

Requests to the Steam Web API transmit the API key and the identifiers and parameters needed for the operation to Valve, depending on the request type. Valve's processing is independent of PLATINEXOS's local storage. The Steam store and content delivery networks may receive requests for metadata, covers, and icons. At startup, the by Sandr0F signature may query the [public Steam profile of Sandr0F](https://steamcommunity.com/id/Sandr0F/) over HTTPS in XML format (`?xml=1`) and download its avatar from Steam image servers. This query does not use your Steam Web API key. These services may receive connection information, such as the IP address. Links opened in the browser, including guides and voluntary contribution options, follow the policies of the respective sites. [Valve Privacy Policy](https://store.steampowered.com/privacy_agreement/)

PLATINEXOS does not implement its own telemetry, advertising, or automatic reporting to the developer. Detailed Steam Web API diagnostics are optional and presented in the application before execution. Review any report before sharing it.

In the Portable edition, the Check for updates button queries the public GitHub API for Releases of Sandr0F/PLATINEXOS, without sending the Steam Web API key. This query is manual and may transmit connection information to GitHub; it does not automatically download or install updates.

## Retention and control

Local storage lets you consult previously loaded data without synchronizing again. The application does not automatically delete these records after a set period. To back up the local database, close the application before making the backup.

**How to stop future automatic synchronizations:** select the Steam account in Settings and clear **Sync this Steam account when PLATINEXOS opens**. The saved key and previously synchronized data remain. You can remove the key separately.

**How to remove local data:** close PLATINEXOS completely. If desired, make a backup first. Then, in File Explorer, open `%LOCALAPPDATA%\SteamAchievementTracker` and delete the files in that folder that you no longer want to keep. To delete all application files stored in that folder, delete the entire folder. Depending on the files present, this may permanently remove the SQLite database, preferences, goals, manual confirmations, startup synchronization authorizations, and caches. Do not do this if there is information you want to preserve. To also remove the local record of acceptance of the Terms of Use, separately delete `%LOCALAPPDATA%\PLATINEXOS\terms-acceptance.json`, if it exists; deleting it may require you to accept the terms again when opening the application. Separately remove any key stored in Windows Credential Manager, preferably through the application itself. Deleting local files does not remove data held by Valve or backups made by third parties.

These instructions refer to the known storage used by version 1.0.0 and do not automatically delete data in external services.

## Contact and support

For technical questions, problem reports and suggestions, use PLATINEXOS GitHub Issues: [https://github.com/Sandr0F/PLATINEXOS/issues](https://github.com/Sandr0F/PLATINEXOS/issues). This channel is public. Do not share access keys, passwords, local databases, personal information, unreviewed reports or screenshots containing sensitive data. For private or privacy-related matters, contact [platinexos@gmail.com](mailto:platinexos@gmail.com).

**Private privacy contact:** [platinexos@gmail.com](mailto:platinexos@gmail.com). Use this address for requests involving personal data. Do not send that data to public GitHub Issues.
