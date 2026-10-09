# Voxnote Privacy Policy

_Last updated: 2026-10-10_

Voxnote is a Windows desktop app that turns speech into note cards. This page
explains what leaves your computer, what does not, and what we keep.

## What stays on your computer

- **Your notes.** Every note is stored only on your PC, in `notes.json` inside
  the app's data folder (`%APPDATA%\Voice to List`, the app's original name).
  We never upload, sync, or read your notes.
- **Your settings and API key.** If you enter your own OpenAI or OpenRouter
  key, it is stored encrypted on your PC (Windows credential encryption via
  Electron `safeStorage`). It is only sent to the provider you chose.
- **A local log file** (`app.log`, same folder) with technical events such as
  "recording started" and error messages. It does not contain audio or the
  text of your notes. You decide whether to attach it to a bug report.

## What leaves your computer, and when

Voxnote records the microphone **only while you are dictating** (between the
two presses of the hotkey, or while "Listen" is on). Nothing is recorded in
the background.

Where the recording goes depends on the mode you use:

| Mode | Audio is sent to | Why |
|------|------------------|-----|
| Windows dictation (default, `Win+H`) | Microsoft, under Microsoft's own terms | Voxnote is not involved; Windows handles the speech recognition. |
| Your own OpenAI / OpenRouter key | OpenAI or OpenRouter directly | To transcribe the recording. Their privacy terms apply. |
| Voxnote license key (`vtl-…`) | Our server, which forwards it to OpenAI or OpenRouter | To transcribe the recording with our account, so you do not need your own key. |

With a license key, the "Clean up" and "Translate to" options also send the
**transcribed text** (not the audio) from our server to OpenAI for processing.

## Our server (license-key users only)

- **Audio is not stored.** The server forwards the recording to the
  transcription provider and returns the text. It does not write audio or
  transcripts to disk.
- **Usage counting.** For each license key the server keeps the key itself, a
  label we set when issuing it (usually the e-mail address the key was sold
  to), when it was created, and the number of minutes used per day and per
  month. This is needed to enforce the fair-use limits.
- **Error logs.** The server logs technical errors (time, request path, error
  message). These logs do not contain audio or text.
- **Third parties.** Our server currently sends audio and text to
  [OpenRouter](https://openrouter.ai/privacy), which routes them to the
  transcription and language model providers. Their data policies apply. We
  will update this page if the provider changes.

## Updates

On start the app asks GitHub whether a newer version exists (a request for a
small version file). Nothing is downloaded until you click "Download". This
request reveals your IP address to GitHub, like any web request.

## No analytics, no ads, no accounts

Voxnote has no analytics, no tracking, no advertising, and no user accounts.
We do not sell or share personal data.

## System audio capture

The optional "system audio" setting mixes what you hear (for example a call)
into the recording. It is off by default. **Recording other people may require
their consent under the laws that apply to you; that is your responsibility.**

## Your choices and rights

- Delete your notes: delete the cards in the app or remove `notes.json`.
- Stop all network use: use Windows dictation mode and remove any API or
  license key from Settings.
- Delete server-side data: contact us and we will revoke the key and remove
  its usage record.
- For users in the EU/EEA and the UK: we process license-key usage data to
  provide the service you bought (performance of a contract). It is kept
  while the key is active and deleted on request. You can ask for access,
  correction or deletion through the contact below.

## Changes

We will update this page when the app's behaviour changes and note the date
at the top.

Contact: open an issue at
<https://github.com/DynamicCE/voxnote-releases/issues>.
