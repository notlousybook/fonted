# fontic

<p align="center">
  <img src="assets/fontic.png" alt="Fontic — dark theme preview" width="150" />
</p>

An extension to change the UI font of VS Code. That's all it does.

> Based on https://github.com/blackmann/fonted but this is made better ig idk man

> [!IMPORTANT]
> For Cursor (and some other VS Code forks), the marketplace doesn't stay up to date with the current version of Fontic. Please use the [Releases](https://github.com/notlousybook/fontic/releases) page.


<img src="assets/dark.png" alt="Fontic — dark theme preview" />

## Features

- 🔤 Replace the VS Code UI font with any installed font
- 📐 Control `font-stretch` for variable-width fonts
- ♻️ Reload the font without manually editing files
- 🔙 Revert the title bar style if it breaks

## Usage

1. Install the extension.
2. Open **Settings** and set `fontic.font` to your desired font family:
   ```json
   "fontic.font": "Pragmata Pro Mono"
   ```
3. Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`) and run **Fontic: Enable**.
4. Restart VS Code when prompted.

> [!NOTE]
> You can safely ignore the notification: *"Your Code installation appears to be corrupt. Please reinstall."* — this is expected because the extension modifies an internal VS Code file.

## Commands

| Command              | Description                                      |
| -------------------- | ------------------------------------------------ |
| `Fontic: Enable`     | Inject the configured font into the VS Code UI   |
| `Fontic: Disable`    | Remove the injected font                         |
| `Fontic: Reload`     | Re-apply the font after changing settings         |
| `Fontic: Revert UI`  | Reset `window.titleBarStyle` back to `custom`     |

## Configuration

| Setting              | Type     | Description                                          |
| -------------------- | -------- | ---------------------------------------------------- |
| `fontic.font`        | `string` | Font family to use for the VS Code UI                |
| `fontic.fontStretch`  | `string` | CSS `font-stretch` value (e.g. `condensed`, `125%`)  |

## Known Limitations

- The extension patches VS Code's internal `workbench.html` file, which triggers a "corrupt installation" warning. This is cosmetic and harmless.
- A restart is required after every font change.
- If a VS Code update resets the workbench file, you'll need to re-run **Fontic: Enable**.
