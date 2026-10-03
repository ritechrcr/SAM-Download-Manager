# SAM Download Manager (SDM)

## Version 1.0.1a
Release date: October 1, 2026

SAM Download Manager (SDM) is a Windows download manager designed to provide a simple download queue, direct-link handling, configurable download behavior, automatic post-download actions, and built-in archive extraction without requiring an external archive application.

## Main Features

- Download queue with support for multiple downloads.
- Configurable maximum number of simultaneous downloads.
- Pause and resume support for compatible downloads.
- Multi-connection / boosted downloading support where available.
- Automatic retry handling for failed or interrupted downloads.
- Configurable default Download Folder.
- The selected Download Folder is saved and reused by SDM.
- Default download folder: C:\Downloads.
- Import links from text files.
- Clear Links option for completed entries.
- Open downloaded file and open containing folder options.
- System Tray support.
- Closing SDM with the X button gives the choice to completely exit or minimize SDM to the System Tray.
- Custom SDM dark title bar and interface.

## Supported Link Services

SDM includes handling for:

- MediaFire
- MEGA / mega.nz

SDM can resolve supported page links into downloadable files where the service and link allow it.

## Clipboard / Browser Link Detection

SDM includes clipboard monitoring for supported download links copied from a web browser.

Supported copied links include MediaFire and MEGA links in current version ore to be added. 

## Advance Mode

Advance Mode contains additional download and automation controls.

### Multiple Downloads

Allows the user to configure the maximum number of simultaneous downloads.

### Download Folder

Allows the user to select a permanent download folder instead of choosing a folder for every download.

The selected folder is stored in SDM settings and restored the next time the application starts.

Default:

C:\Downloads

### Auto Features

Available automatic actions include:

- Auto Shutdown
- Sleep
- Hibernate
- Auto Extract

Shutdown, Sleep, or Hibernate can be selected so SDM performs the chosen action after all queued downloads have finished.

Auto Extract is a persistent option. When enabled, SDM remembers the setting after the application is closed and opened again.

## Built-in Archive Extractor

SDM includes its own archive extraction system and does not require other extractor to perform the supported extraction operations.

Supported archive formats:

- ZIP
- RAR
- TAR
- GZ
- TGZ
- TAR.GZ

Available extraction actions include:

- Extract Here
- Extract To...
- Auto Extract

Auto Extract creates an extraction folder based on the downloaded archive name.

Example:

C:\Downloads\GameFiles.rar

is extracted to:

C:\Downloads\GameFiles\

For numbered RAR archives such as:

GameFiles.part1.rar

the extraction folder is:

GameFiles\

The extractor includes:

- Extraction progress bar.
- Extraction percentage.
- Extracted bytes / total bytes information.
- Current-file information.
- Cancel extraction.
- Confirmation before cancelling.
- Automatic closing after a confirmed cancellation.
- Multipart archive validation.
- Missing-volume detection.
- Protection against unsafe archive paths.
- Open button after successful extraction to open the destination folder.
- Close button after extraction completes.

For multipart RAR archives, Auto Extract uses the primary volume rather than attempting to start a separate extraction for every numbered part.

## Duplicate Download Protection

Version 1.0.1a includes duplicate-download protection.

SDM checks the download queue and destination before adding another copy of the same download.

A completed download is not downloaded again when the completed file still exists.

If the completed file was manually deleted from disk, SDM can allow the file to be downloaded again instead of permanently blocking the URL because of an old Completed entry.

For downloads where a reliable expected file size is available, SDM can use the file size as an additional completed-file check.

## Fixes and Changes in Version 1.0.1a

- Added persistent Download Folder selection.
- Download Folder is now saved instead of reverting to the default folder after restart.
- Added System Tray integration.
- Added close confirmation with the option to completely exit SDM or leave it running in the System Tray.
- Corrected the SDM window behavior so it does not intentionally remain above other applications.
- Added Auto Shutdown.
- Added Sleep.
- Added Hibernate.
- Added built-in Archive Extractor support.
- Added ZIP, RAR, TAR, GZ, TGZ, and TAR.GZ extraction.
- Added Extract Here and Extract To options.
- Added extraction progress and percentage display.
- Added cancellable extraction with confirmation.
- Added multipart archive checking and missing-part handling.
- Added Auto Extract under Auto Features.
- Auto Extract setting is saved between SDM sessions.
- Auto Extract creates a folder using the archive name.
- Added Open button after successful extraction to open the extracted folder.
- Added duplicate-download detection.
- Corrected duplicate handling so a deleted completed file can be downloaded again.
- Improved MEGA completion/retry handling to avoid treating a completed transfer as a failed download.
- Improved supported-link clipboard handling for MediaFire, MEGA.

## Notes

Some download features depend on the behavior of the remote hosting service. A hosting provider can change its pages, URLs, authentication, rate limits, or download mechanisms, which may require a future SDM update.

Resume and multi-connection behavior can also depend on whether the remote server supports the required HTTP range operations.

## About

SAM Download Manager

SDM Version 1.0.1a

10/1/2026

By: Ritech RFCR
