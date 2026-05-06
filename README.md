# VS Code Custom Extensions, Colors, and Themes Setup

## Installed tools:

### Extensions
- **Material Theme (But I Won't Sue You)** By Theo
- **Custom CSS and JS Loader** By be5invis

To install run these commands inside VS Code terminal:

```bash
ext install be5invis.vscode-custom-css
ext install t3dotgg.vsc-material-theme-but-i-wont-sue-you
```

### Fonts

- Installed font `Operator Mono` from [this directory](./fonts/). 
- Clone the repo and install the fonts inside it by double-clicking it

### Setup Methodology

- Open settings.json via `Ctrl + Shift + P `
- Insert the given code snippet inside it.

```code
"editor.fontFamily": "Operator Mono Lig",
"editor.fontLigatures": true,
"vscode_custom_css.imports": [
    "file:///home/safal_gtm/.vscode_custom/vscode_style.css"
],
"security.workspace.trust.enabled": false,
"vscode_custom_css.policy": true
```
- Save custom CSS as `vscode_custom.css` in safe location like:
```text
/home/safal_gtm/.vscode_custom/vscode_style.css
```
Custom CSS be like:
```code
/* === Operator Mono Lig Neon Hacker Theme === */

/* Base font */
.monaco-editor {
  font-family: "Operator Mono Lig", monospace !important;
  font-size: 15px;
  background-color: #0f0f1a !important; /* Dark, moody background */
  color: #eee !important;
}

/* Comments - neon green italic */
.token.comment,
.comment {
  font-family: "Operator Mono Lig Italic", monospace !important;
  font-style: italic !important;
  color: #00FF7F !important; /* Neon green */
}

/* Keywords - bright neon yellow with glow */
.token.keyword,
.keyword {
  color: #FFFF33 !important;
  font-weight: bold !important;
  font-style: italic !important;
  text-shadow: 0 0 6px #FFFF99;
}

/* Functions - electric cyan */
.token.function,
.function {
  color: #00FFFF !important;
  font-weight: bold !important;
  text-shadow: 0 0 5px #00FFFF;
}

/* Strings - vivid pink/magenta */
.token.string,
.string {
  color: #FF33FF !important; /* Neon magenta */
  text-shadow: 0 0 6px #FF66FF;
}

/* Classes & Types - purple */
.token.class-name,
.token.type,
.class-name,
.type {
  color: #9B30FF !important; /* Purple */
  font-weight: bold !important;
  text-shadow: 0 0 5px #BF40BF;
}

/* Numbers - orange */
.token.number,
.number {
  color: #FF8C00 !important; /* Neon orange */
}

/* Operators - light blue */
.token.operator,
.operator {
  color: #66CCFF !important;
}

/* Variables - white */
.token.variable,
.variable {
  color: #FFFFFF !important;
}
```
### Permission Setup
We need to provide permission to  change the vscode permission by 
```bash
sudo chown -R $USER /opt/visual-studio-code
```
### Reload Custom CSS
Reload the custom css by pressing `Ctrl + Shift + P ` followed by `Reload Custom CSS and JS`.
It will restart the vscode
```note
It may appear like Installation appears to be corrupt [Unsupported] just ignore it
```

