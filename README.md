# Oruvex - Your signal. Your control.

Focused, native camera and microphone tools for Windows creators who stream and play on the same computer. Design and product direction by João Rodrigues / Kira, with AI-assisted development.

## Download: 0.2.2-beta.1 - English edition

[Oruvex Cam](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.2-beta.1/Oruvex-Cam-0.2.2-beta.1-Windows.zip) · [Oruvex Voice](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.2-beta.1/Oruvex-Voice-0.2.2-beta.1-Windows.zip) · [Release notes and requirements](https://github.com/artssbykira/oruvex-apps/releases/tag/v0.2.2-beta.1)

Experimental betas, free to evaluate. Extract the entire ZIP before running. The Oruvex executables are not code-signed yet: review the download and do not automatically bypass security alerts. Compatibility, performance and latency depend on your system. Test before an important stream.

### What's new

Both apps now have English controls, tray menus and app messages. Cam retains its wider sidebar, fixed header and tray actions, exposure settings before focus, and settings-refresh feedback. Voice retains its separate output-message row, unobstructed tray button and headphone-monitor controls. Capture, decoding, buffers, drivers and RNNoise processing are unchanged. Layout tests are not a new streaming or gaming benchmark.

### Brand guidelines

[Oruvex](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.2-beta.1/BRAND_GUIDELINES_ORUVEX_V2_EN.pdf) · [Oruvex Cam](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.2-beta.1/BRAND_GUIDELINES_ORUVEX_CAM_V2_EN.pdf) · [Oruvex Voice](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.2-beta.1/BRAND_GUIDELINES_ORUVEX_VOICE_V2_EN.pdf) · [Complete English brand kit](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.2-beta.1/Oruvex-Brand-Kit-V2-English.zip)

Three 12-page English manuals covering identity, construction, typography, color, small-scale use and communication. The kit includes official vector assets, icons and supporting fonts with their licenses. Brand examples are illustrative compositions, not screenshots of a running app.

## Oruvex Cam

Connects to **Canon EOS cameras over USB** using Canon EDSDK, without digiCamControl or OBS Virtual Camera. Displays the detected model and lets you choose between connected Canon cameras. Includes optional preview, lens focus control, supported exposure settings, five saved presets and system-tray operation. Advanced settings are collapsed by default.

**Canon's proprietary SDK DLLs are not included in the public ZIP.** Obtain the **x86 (32-bit)** EDSDK through [Canon's official SDK program](https://www.usa.canon.com/support/sdk), under Canon's terms. In the app, click **Add Canon SDK (x86)**, select the x86 binary folder and restart.

Only **EOS Rebel T7** has been verified in the development environment. Other Canon models are experimental and depend on SDK version, firmware and Live View. Nikon, Sony and ordinary UVC webcams are not supported. Model detection is not a certification of compatibility.

In OBS or TikTok LIVE Studio, select **KCC Camera**. This legacy technical identifier is retained to preserve existing sources; the app is named Oruvex Cam. Virtual camera registration requires administrator rights and must be updated if you move the folder.

The **1920x1080/60** output profile may upscale and repeat frames. It does not guarantee native 1080p60 capture. **1024x576/30** is the lighter profile. The input counter reports frames received from the camera, not a promise of 60 unique frames. Turning preview off stops local drawing, not the resource use of sending video to your streaming app.

## Oruvex Voice

RNNoise-based microphone noise suppression on the **CPU**, with adjustable strength, an optional gate, headphone monitoring with independent volume and system-tray operation. It does not use CUDA or GPU-based AI processing. That does not mean zero CPU, memory or window-composition cost.

1. Extract the full ZIP and open **Oruvex Voice.exe**.
2. If requested, click **Install virtual output**, follow the official VB-CABLE installer and restart Windows. Administrator rights are required.
3. Select your physical microphone. It must run at **48,000 Hz**, using 16-bit PCM or 32-bit float. If needed, adjust its Windows audio properties.
4. In OBS/TikTok, select **CABLE Output (VB-Audio Virtual Cable)**. CABLE Input is the playback destination used internally by the app.
5. Use headphones when you click **Start monitoring** to avoid feedback. Monitoring adds a separate playback path.
6. **Minimize to system tray** keeps cleanup running; **Exit** stops the app.

**VB-CABLE is VB-Audio donationware**, not a driver created by Oruvex. Its official installer is included without modifications. Its own terms still apply. [Source/download](https://www.vb-cable.com/) · [Participation and licensing](https://vb-audio.com/Services/licensing.htm). Consider supporting VB-Audio if you find its software useful.

## Upgrading

Choose **Exit** from each app's tray menu before replacing files. Extract the full new package. Preserve your legally obtained Canon SDK; do not reinstall VB-CABLE if it already works. Existing preferences remain in the same legacy locations. [Previous releases](https://github.com/artssbykira/oruvex-apps/releases) remain available.

## Requirements, privacy and testing

Windows 10/11 **x64** and .NET Framework 4.x. Cam runs as x86 for the SDK; Voice runs as x64. Physical device compatibility is required. Native Windows dialogs and hardware device names may use your system language.

Processing is local. No telemetry or audio/video upload is implemented in these apps. Existing settings are kept in `%LOCALAPPDATA%\K Cam App` and `HKCU\Software\KMNC`. Legacy filenames and identifiers are intentionally preserved. No streaming account or login is required for local processing.

RNNoise uses **10 ms blocks**, but this is not a measurement of end-to-end latency. Resource use, game FPS and audio latency must be evaluated on your own hardware. There is no promise of zero resource use or universal compatibility.

Use the release's **SHA256SUMS.txt** to verify file integrity. [Report an issue](https://github.com/artssbykira/oruvex-apps/issues) with Windows version, camera model and SDK version. Review logs before sharing; do not publish serial numbers, private recordings or tokens.

## Credits and conditions

Oruvex design and product direction: João Rodrigues / Kira, with AI-assisted execution. Oruvex is not affiliated with or certified by Canon, OBS, NVIDIA, TikTok or VB-Audio.

- Softcam: MIT; license included in the Cam ZIP.
- RNNoise / Xiph.Org: BSD-3-Clause; license included in the Voice ZIP.
- NAudio 1.10.0: Microsoft Public License; license included in the Voice ZIP.
- VB-CABLE: VB-Audio donationware; official package and notices included without modifications.
- Canon EDSDK: proprietary and **not redistributed** in these betas.
- Supporting brand fonts: their original Open Font License files are included in the brand kit.

Oruvex beta binaries are free to evaluate, without a guarantee of compatibility or performance, subject to any mandatory rights that apply. Third-party terms remain independent. App source code is not published in this repository in this version. The identity assets do not authorize you to represent a modified product as an official Oruvex release.
