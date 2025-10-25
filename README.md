# Discord Anime Presence Extension

A Chromium browser extension that updates your Discord Rich Presence based on the anime you are watching on HiAnime or HiAnimeZ.

## Features
- Automatically detects anime title, episode, and playback status from HiAnime/HiAnimeZ.
- Updates Discord Rich Presence in real time via a native messaging host (Node.js).
- Popup UI for connection status and manual reconnect.

## Setup Instructions

### 1. Extension Installation
1. Go to `chrome://extensions` in your Chromium browser (Chrome, Brave, Edge, etc.).
2. Enable "Developer mode" (top right).
3. Click "Load unpacked" and select this project folder.
4. Ensure the following files are present:
   - manifest.json
   - content.js
   - background.js
   - popup.html

### 2. Native Messaging Host Setup
1. Install Node.js from https://nodejs.org/
2. In your project directory, run:
   ```sh
   npm install discord-rpc
   ```
3. Open `native_host.js` and replace `YOUR_DISCORD_APP_CLIENT_ID` with your Discord application's client ID.
4. Register the native messaging host with your browser. (See [Chrome Native Messaging documentation](https://developer.chrome.com/docs/apps/nativeMessaging/) for details.)
5. Start the native host:
   ```sh
   node native_host.js
   ```

### 3. Usage
- Open HiAnime or HiAnimeZ and start watching an anime.
- The extension will automatically update your Discord Rich Presence.
- Use the extension popup to check connection status or reconnect if needed.

## Troubleshooting
- If Discord Rich Presence does not update, ensure the native host is running and connected.
- Make sure your Discord client is open and you are logged in.
- Check browser console and Node.js terminal for errors.

## License
MIT