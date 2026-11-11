# One Dark Modern Theme

A dark theme plugin for JetBrains IDEs, based on the [One Dark Modern](https://github.com/jdinhlife/vscode-onedark-modern) color palette.

## Features

- **UI theme** — Dark chrome, tuned buttons (solid secondary + blue primary), popups, tool windows, trees, and lists
- **Editor scheme** — One Dark syntax colors for code, comments, strings, keywords, diffs, and console output
- **New UI** — Layout tweaks (tree/list row height, spacing) for IntelliJ Platform 2025.1+

## Requirements

- IntelliJ Platform **2025.1** or later (`sinceBuild = 251`)
- Compatible with IntelliJ IDEA Community/Ultimate and other JetBrains IDEs built on the same platform version

## Installation

### From source

1. Clone this repository.
2. Build the plugin:

   ```bash
   ./gradlew buildPlugin
   ```

3. Install the generated plugin archive from `build/distributions/` via **Settings → Plugins → ⚙ → Install Plugin from Disk…**

### Run in a sandbox IDE

```bash
./gradlew runIde
```

## Usage

**Settings → Appearance & Behavior → Appearance & UI → Theme** → choose **One Dark Modern**.

The editor color scheme **One Dark Modern** is applied automatically with the theme. IntelliJ IDEA default icons are used.

## Development

Palette and UI keys are maintained in `scripts/update-theme.js`. After editing colors there, regenerate theme assets:

```bash
node scripts/update-theme.js
```

| Path | Purpose |
|------|---------|
| `src/main/resources/theme/one_dark_modern.theme.json` | UI theme definition |
| `src/main/resources/theme/one_dark_modern.xml` | Editor color scheme |
| `src/main/resources/META-INF/plugin.xml` | Plugin descriptor |
| `scripts/update-theme.js` | Palette sync script |

## Credits

- UI theme and editor scheme are based on the [One Dark Modern](https://github.com/jdinhlife/vscode-onedark-modern) color palette.

## License

This project is licensed under the [MIT License](LICENSE).
