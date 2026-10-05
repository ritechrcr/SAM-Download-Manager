# SAM Download Manager (SDM)

**SAM Download Manager** is a Windows download manager developed by **Ritech RFCR**. It provides a simple download queue, browser and clipboard integration, configurable download behavior, automatic post-download actions, and built-in archive extraction without requiring an external archive application.

**Current Version:** 1.0.3  
**Release Date:** October 4, 2026  
**Developer:** Ritech RFCR

---

## Main Features

- Download queue with support for multiple downloads.
- Configurable maximum number of simultaneous downloads.
- Pause and resume support for compatible downloads.
- Multi-connection / boosted downloading support where available.
- Automatic retry handling for failed or interrupted downloads.
- Configurable and persistent default Download Folder.
- Default download folder: `C:\Downloads`.
- Import links from text files.
- Clear completed links from the download list.
- Open downloaded files or their containing folders.
- Browser integration for supported browsers.
- Clipboard link detection.
- System Tray support.
- Automatic Shutdown, Sleep, and Hibernate actions.
- Built-in archive extraction.
- Duplicate download protection.
- Custom dark SAM Download Manager interface.

---

## Browser & Clipboard Integration

SAM Download Manager includes browser integration designed to make sending downloads to SDM easier.

Current integration includes:

- Microsoft Edge support.
- Mozilla Firefox support.
- Automatic interception of supported browser downloads.
- **Download with SAM Download Manager** browser integration.
- Clipboard detection for supported download links.
- Improved communication between browsers and SAM Download Manager.

Browser and website behavior can change over time and may require future SDM updates.

---

## Supported Link Services

SDM includes handling for supported links from services such as:

- MediaFire
- MEGA / mega.nz

SDM can resolve supported page links into downloadable files where the service and link allow it.

---

## Advance Mode

Advance Mode contains additional download and automation controls.

### Multiple Downloads

Allows the user to configure the maximum number of simultaneous downloads.

### Download Folder

Allows the user to select a permanent download folder instead of choosing a folder for every download.

The selected folder is stored in SDM settings and restored the next time the application starts.

Default:

`C:\Downloads`

### Auto Features

Available automatic actions include:

- Auto Shutdown
- Sleep
- Hibernate
- Auto Extract

Shutdown, Sleep, or Hibernate can be selected so SDM performs the chosen action after all queued downloads have finished.

Auto Extract is a persistent option. When enabled, SDM remembers the setting after the application is closed and opened again.

---

## Built-in Archive Extractor

SDM includes its own archive extraction system and does not require another archive application for supported extraction operations.

### Supported Formats

- ZIP
- RAR
- TAR
- GZ
- TGZ
- TAR.GZ

### Extraction Options

- Extract Here
- Extract To...
- Auto Extract
- Extraction progress and percentage.
- Extracted data / total data information.
- Current-file information.
- Elapsed extraction time.
- Cancel extraction with confirmation.
- Multipart archive validation.
- Missing-volume detection.
- Protection against unsafe archive paths.
- Open destination folder after successful extraction.

Auto Extract creates an extraction folder based on the downloaded archive name.

Example:

`C:\Downloads\GameFiles.rar`

is extracted to:

`C:\Downloads\GameFiles\`

For numbered RAR archives such as:

`GameFiles.part1.rar`

the extraction folder is:

`GameFiles\`

For multipart RAR archives, Auto Extract uses the primary volume rather than attempting to start a separate extraction for every numbered part.

---

## Duplicate Download Protection

SDM checks the download queue and destination before adding another copy of the same download.

A completed download is not downloaded again when the completed file still exists.

If the completed file was manually deleted from disk, SDM can allow the file to be downloaded again instead of permanently blocking the URL because of an old Completed entry.

Where a reliable expected file size is available, SDM can use the file size as an additional completed-file check.

---

# Release History

## Version 1.0.3

**Release Date: October 4, 2026**

### What's New

- Added browser integration support for Microsoft Edge and Mozilla Firefox.
- Added automatic download interception from supported browsers.
- Added **Download with SAM Download Manager** browser integration.
- Added clipboard link detection for supported download links.
- Improved communication between web browsers and SAM Download Manager.
- Improved browser download handling and confirmation behavior.
- Improved single-instance handling for external download requests.
- Added a new startup Splash Screen.
- Added animated startup loading progress and application version display.
- Improved application startup behavior.
- Improved application resource organization.
- Improved build and publishing reliability.
- Improved browser integration deployment.
- Various stability improvements and bug fixes.

---

## Version 1.0.2a

**Release Date: October 3, 2026**

### Fixes & Improvements

- **Responsive Window Layout**
  - Improved interface behavior when maximizing and resizing the main window.
  - Main sections now adapt correctly to the available window size.

- **Unified Popup Design**
  - Updated application popups to better match the visual style of SAM Download Manager.
  - Improved consistency between the main interface and confirmation/message dialogs.

- **Single Instance Protection**
  - SAM Download Manager prevents multiple active instances from running simultaneously.

- **Dark Scrollbar Fix**
  - Improved scrollbar appearance when a large number of downloads are displayed.

- **Duplicate Link Protection**
  - Improved clipboard link detection to prevent duplicate downloads.

- **System Tray Clipboard Restore**
  - Improved application behavior when supported download links are detected while SDM is in the System Tray.

- **Extraction Window Improvements**
  - Added extracted data progress information.
  - Added real-time extraction elapsed time.
  - Improved Cancel behavior.
  - Added an **Open** button after successful extraction.
  - Improved multipart archive validation and missing-part detection.

- **Extraction Performance Optimization**
  - Significantly improved archive extraction performance.
  - Improved extraction I/O and memory handling.
  - Reduced unnecessary interface updates during extraction.

- **Faster Download Finalizing**
  - Improved performance when combining multi-connection download segments.
  - Improved disk access behavior when multiple downloads reach Finalizing.

- **Completed File Detection**
  - SDM detects files that have already been completely downloaded.
  - Existing completed files are not downloaded again.

- **Multipart Duplicate Notification**
  - Improved duplicate notifications for multipart archive downloads.

- **Header Visual Fix**
  - Improved visual consistency of the SAM Download Manager title and menu area.

- **Version Display**
  - Added the current application version beside the SAM Download Manager name.

### Performance & Stability

Version 1.0.2a introduced multiple optimizations based on real-world testing, with a focus on download finalization, archive extraction, duplicate handling, clipboard behavior, and interface consistency.

---

## Version 1.0.1a

**Release Date: October 1, 2026**

### Features, Fixes & Improvements

- Added persistent Download Folder selection.
- Added System Tray integration.
- Added close confirmation with the option to exit SDM or leave it running in the System Tray.
- Improved window behavior.
- Added Auto Shutdown.
- Added Sleep.
- Added Hibernate.
- Added built-in Archive Extractor support.
- Added ZIP, RAR, TAR, GZ, TGZ, and TAR.GZ extraction.
- Added Extract Here and Extract To options.
- Added extraction progress and percentage display.
- Added cancellable extraction with confirmation.
- Added multipart archive checking and missing-part handling.
- Added Auto Extract.
- Added persistent Auto Extract settings.
- Added Open button after successful extraction.
- Added duplicate-download detection.
- Improved duplicate handling when completed files have been manually deleted.
- Improved MEGA completion and retry handling.
- Improved supported-link clipboard handling for MediaFire and MEGA.

---

## Notes

Some download features depend on the behavior of the remote hosting service. A hosting provider can change its pages, URLs, authentication, rate limits, or download mechanisms, which may require a future SDM update.

Resume and multi-connection behavior can also depend on whether the remote server supports the required HTTP range operations.

---

## About

**SAM Download Manager**  
**Version 1.0.3**  
**October 4, 2026**  
**Ritech RFCR**
