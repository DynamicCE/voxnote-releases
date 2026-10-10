# Voxnote Privacy Policy

_Last updated: 2026-10-10_

Voxnote is a Windows desktop app that turns speech into note cards. This page
explains what leaves your computer, what does not, and what we keep.

## What stays on your computer

- **Your notes.** Every note is stored only on your PC, in `notes.json` inside
  the app's data folder (`%APPDATA%\Voice to List`, the app's original name).
  We never upload, sync, or read your notes.
- **Your settings and license key.** On first start the app receives a
  license key for its free trial from our server and stores it encrypted on
  your PC (Windows credential encryption via Electron `safeStorage`). For
  that request the app generates a random **device id** (a UUID, not tied to
  your hardware, your Microsoft account or your name) and keeps it in its
  settings file; it is used only so that each install gets one trial.
- **A local log file** (`app.log`, same folder) with technical events such as
  "recording started" and error messages. It does not contain audio or the
  text of your notes. You decide whether to attach it to a bug report.

## What leaves your computer, and when

Voxnote records the microphone **only while you are dictating** (between the
two presses of the hotkey, or while "Listen" is on). Nothing is recorded in
the background.

Where the recording goes:

| Mode | Audio is sent to | Why |
|------|------------------|-----|
| Voxnote hotkeys (trial or subscription) | Our server, which forwards it to OpenAI or OpenRouter | To transcribe the recording with our account; you never need your own key. |
| Windows dictation (`Win+H`) | Microsoft, under Microsoft's own terms | Voxnote is not involved; Windows handles the speech recognition. |

The "Clean up" and "Translate to" options also send the **transcribed text**
(not the audio) from our server to the language-model provider for processing.

## Our server

- **Audio is not stored.** The server forwards the recording to the
  transcription provider and returns the text. It does not write audio or
  transcripts to disk.
- **Usage counting.** For each license key the server keeps the key itself,
  the device id described above, when it was created, the trial or
  subscription end date, and the number of minutes used per day and per
  month. This is needed to enforce the trial and the fair-use limits.
- **Subscriptions.** Payment is handled entirely by the Microsoft Store; we
  never see your card or billing details. After a purchase, and on later
  starts, the app gives our server a purchase key issued by Windows for your
  Store account; the server uses it to ask Microsoft whether your Voxnote
  subscription is active and until when, and stores only that answer (the
  expiry date), so your key keeps working. The key reveals no name, e-mail
  or payment data to us.
- **Error logs.** The server logs technical errors (time, request path, error
  message). These logs do not contain audio or text.
- **Third parties.** Our server currently sends audio and text to
  [OpenRouter](https://openrouter.ai/privacy), which routes them to the
  transcription and language model providers. Their data policies apply. We
  will update this page if the provider changes.

## Updates

The app is installed and updated by the Microsoft Store. It does not contact
GitHub or any other update server itself.

## No analytics, no ads, no accounts

Voxnote has no analytics, no tracking, no advertising, and no user accounts.
We do not sell or share personal data.

## System audio capture

The optional "system audio" setting mixes what you hear (for example a call)
into the recording. It is off by default. **Recording other people may require
their consent under the laws that apply to you; that is your responsibility.**

## Your choices and rights

- Delete your notes: delete the cards in the app or remove `notes.json`.
- Stop all network use: uninstall the app, or do not press the hotkeys and
  use Windows dictation (`Win+H`) instead.
- Delete server-side data: contact us with your device id (in `config.json`)
  and we will revoke the key and remove its usage record.
- Cancel a subscription: at <https://account.microsoft.com/services>, like
  any Microsoft Store subscription.
- For users in the EU/EEA and the UK: we process the device id and usage
  data to provide the trial and the service you subscribed to (performance of
  a contract). It is kept while the key is active and deleted on request. You
  can ask for access, correction or deletion through the contact below.

## Changes

We will update this page when the app's behaviour changes and note the date
at the top.

Contact: open an issue at
<https://github.com/DynamicCE/voxnote-releases/issues>.
