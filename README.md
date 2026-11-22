<div align="center">

# LoadQuestThings

**LoadQuestThings** is a browser‑based sideloader for Meta Quest headsets. It lets you install custom APKs on the Meta Quest directly from your web browser. Developer mode must be enabled on your headset.

This fork was created by treat. QuestLoad was created by [Frizzle](https://github.com/FrizzleM/QuestLoad).

<br/>
  <a href="https://LoadQuestThings.nerdcoder.dev">
    <img alt="Launch LoadQuestThings" src="https://img.shields.io/badge/Launch-Open%20App-6cb6ff?style=for-the-badge">
  </a>
  
  <a href="https://github.com/treatwashere/LoadQuestThings/issues">
    <img alt="Issues" src="https://img.shields.io/github/issues/nerd-coder/LoadQuestThings?style=for-the-badge&color=ef4444">
  </a>

</div>

<img width="1030" alt="LoadQuestThings installing a game bundle on a connected Quest 3" src="docs/screenshot.png" />

## Requirements

- Meta Quest headset (2, 3, 3S, Pro)
- Developer mode enabled on your headset
- Browser with WebUSB support (Chrome, Edge, ect.)

## Quick Start

Follow these steps to sideload an app:

### 1. Launch LoadQuestThings
Open [LoadQuestThings.nerdcoder.dev](https://LoadQuestThings.nerdcoder.dev).

### 2. Connect your Quest
Plug your Quest into the computer and click **Connect Quest**. Pick the headset in your browser's device list, then put on the headset and select **Allow** on the USB debugging prompt. LoadQuestThings shows the headset model once it's connected.

### 3. Choose what to install
Under **Choose what to install**, pick one. You can do this before or after connecting.
- **APK**: drop an `.apk` file on the **Drop an APK here** tile, or click the tile to choose one.
- **Bundle folder**: for games with OBB files, click **Choose a bundle folder** and select a folder with one APK at its top level and an OBB folder named after the package. LoadQuestThings checks the layout as soon as you pick it:

  ```text
  bundle/
  ├── com.CMGames.IntoTheRadius.apk
  └── com.CMGames.IntoTheRadius/
      ├── main.161562.com.CMGames.IntoTheRadius.obb
      └── patch.161562.com.CMGames.IntoTheRadius.obb
  ```

### 4. Install
Click **Install APK** or **Install bundle**. The progress bar and the **Activity** log show each step.

### 5. Launch the app on your Quest
After the install finishes, go to **Apps → Unknown Sources** on your headset and launch the app. When you're done, click **Disconnect** in LoadQuestThings.

## Future updates
- Ability to export games from the headset

## Games sources

LoadQuestThings can load games lists from sources you add. A source is a URL and a password: LoadQuestThings
requests the URL with the password in the `x-api-password` header and expects the games list as
JSON. None are set up by default.

Click **Games sources** in the top bar, then **Add source**. Enter the URL and password, or click
**Paste a JSON config** to fill them in from:

```json
{
  "url": "https://example.com/api/games",
  "password": "replace-this-password"
}
```

## Contributing

If you are interested in contributing, please see our [CONTRIBUTING.md](CONTRIBUTING.md).

## Credits

Copyright © 2026 [Frizzle](https://github.com/FrizzleM/LoadQuest) and treat

