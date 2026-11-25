<p align="center"><img src="extension/icons/icono-128.png" width="96" alt="Audio Stickers icon"></p>

<h1 align="center">Audio Stickers</h1>

<p align="center">Turn a video, image, or GIF into an <b>audio sticker</b> and send it from <b>WhatsApp Web</b>.<br>Everything is processed in your browser; media is not uploaded to any third-party server by this extension.</p>

<p align="center"><a href="https://github.com/megavip2012/WA-audio-stickers/releases/latest"><img src="docs/img/boton-descargar.png" width="352" alt="Download"></a></p>

<p align="center"><a href="#installation"><img src="docs/img/boton-guia.png" width="282" alt="Installation guide"></a></p>

> **Disclaimer:** This is an unofficial personal project and is not affiliated with WhatsApp or Meta. It relies on internal WhatsApp Web features that may change, and audio stickers are a feature WhatsApp is rolling out/testing. Use at your own risk.

## Installation

This extension is loaded locally in desktop Chromium browsers (Chrome, Edge, or Brave). It does not require running an installer.

1. Download the latest ZIP from the [Releases page](https://github.com/megavip2012/WA-audio-stickers/releases).
2. Extract it to a permanent folder (for example, Documents). Keep the folder in place after installing.
3. Open your browser's extension page: `chrome://extensions`, `edge://extensions`, or `brave://extensions`.
4. Enable **Developer mode**.
5. Click **Load unpacked** (or **Load unpacked extension**) and select the extracted folder containing `manifest.json`.
6. Pin **Audio Stickers** from the extensions menu if you want quick access.

**Language:** Choose a language from the panel selector. The panel updates immediately without reloading WhatsApp Web, and your preference is saved for future sessions.

**Update:** Download and extract the new release, replace the old extension folder contents, then click Reload (↻) on the browser's extensions page. Your settings are preserved.

**Uninstall:** Remove the extension from the extensions page and delete its folder.

## Usage

1. Open [WhatsApp Web](https://web.whatsapp.com/) and enter the chat where you want to send the sticker.
2. Click the extension's icon. The panel has three tabs:
   - **Video:** create a sticker using a video and its audio.
   - **Image + audio:** create a still-image sticker with selected audio (MP3, M4A, OGG, WAV, or audio extracted from a video). Select a segment using the waveform handles; the sticker duration follows that segment.
   - **Video/GIF + audio:** combine an animation (video without its original audio, or GIF) with another audio file. By default, each track keeps its own duration. You can loop the animation or hold its last frame until the audio ends.
3. In the **Video** tab, follow the workflow:
   1. Select a video with sound.
   2. Select the segment using the green handles. The preview shows the selected frame; the −/+ buttons move one frame.
   3. Click **Calculate options**. A resolution × FPS table displays estimated file sizes: green means fits, yellow means fits with reduced quality, ✕ means too large, and ★ marks the recommended option.
   4. Optionally set the pack and author names, create the sticker, review the preview, and send it.
4. On mobile WhatsApp, recipients can add the sticker to Favorites for reuse.

## Limits

| | Limit | Notes |
|---|---:|---|
| Sticker file size | **1 MB** | WhatsApp rejects larger files (HTTP 413). |
| Audio size | 1 MB (about 10 minutes) | WhatsApp Web audio-sticker limit. |
| Resolution | 64–512 px | WhatsApp uses 512 px; larger output does not improve display quality. |
| Frame rate | Up to 30 FPS | Each frame must be at least 8 ms long. |

Longer clips require lower resolution or FPS to stay within 1 MB. The options table estimates what fits before creating the sticker.

Recipients need a WhatsApp version that supports audio stickers. Otherwise WhatsApp may show an unsupported-message notice and they will need to update their app.

## Privacy

- Video conversion is performed locally in your browser.
- Diagnostic logs are stored locally. Phone numbers are masked and keys are excluded. You can view, export, or clear the log in **Test tools** in the panel or through the extension's Options page.
- Logs may include selected file names and the chat name. Review and redact anything you do not wish to share before attaching a diagnostic log to an issue.

## Requirements

- Updated desktop Chrome, Edge, or Brave (uses WebCodecs for audio encoding).
- An active WhatsApp Web session.
- Firefox, Safari, and mobile browsers are not supported. Other Chromium-based browsers may work but are not tested.

## Troubleshooting

1. **The browser says `manifest.json` is missing:** select the extracted folder that directly contains the manifest. Some ZIP tools create an extra nested folder.
2. **The extension errors or disappears:** the folder may have been moved or deleted. Restore it or remove and load the extension again.
3. **Clicking the icon does nothing:** reload the WhatsApp Web tab. Tabs opened before installation/update may not have the extension injected.
4. **Your browser is outdated:** update it and retry.
5. **The recipient sees an unsupported-message notice:** the sticker was sent, but their WhatsApp does not yet support audio stickers; they need to update WhatsApp.
6. **You are using an older build:** download the latest release and update the local extension folder.

WhatsApp Web is not identical for all users and internal interfaces may change. If the issue persists, report it with diagnostics.

## Report a bug or suggest an improvement

Use [GitHub Issues](https://github.com/megavip2012/WA-audio-stickers/issues). Check existing issues first.

For bug reports, include:
- Browser name/version and operating system.
- Extension version (shown at the top of the panel).
- Steps to reproduce, expected behavior, and what happened. Screenshots are helpful; hide chats and phone numbers.
- A diagnostic log for usage-related issues: open **Test tools**, click **Diagnostics**, reproduce the issue, then use **Save log…** and attach the JSON file. Inspect the log and redact sensitive details before sharing.

For installation errors, a screenshot of the browser's extension page is usually enough.

## Developer notes

- [How it works](docs/como-funciona.md): sticker construction, audio format, limits, and extension internals.
- [Development tools](dev/): test pages for conversion without WhatsApp and a synchronization calibration video.

## License

Free for non-commercial use: you may use, study, modify, and redistribute the project, but may not sell it or use it for commercial purposes. See [LICENSE.md](LICENSE.md) for the full [PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0) license. Provided as-is, without warranties.

## Original project

This repository is a fork of [Shirtep/WA-audio-stickers](https://github.com/Shirtep/WA-audio-stickers). Thanks to the original author and contributors.
