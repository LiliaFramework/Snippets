# Lilia Snippets

Visual Studio Code extension providing snippet completions and a small helper command for the [Lilia](https://github.com/Lilia-Framework) framework used in Garry's Mod.

<p align="center">
  <img src="https://github.com/LiliaFramework/Lilia/blob/main/logo.png?raw=true" alt="Lilia Logo" width="150" />
</p>

## Features

- Snippet packs for modules, items, hooks, classes, libraries and more.
- Supports both **Lua** and **GLua** languages.
- Includes a `GLUA: class to className` command to rename `class` attributes in the current selection or file.

## Installation

The extension can be compiled from this repository or installed from the VS Code Marketplace once published.

1. Clone the repository and run `npm install`.
2. Build the extension with `npm run vscode:prepublish`.
3. In VS Code choose **Extensions: Install from VSIX** and select the generated `.vsix` file.

## Development

Use `npm run compile` to watch and rebuild on changes. The source TypeScript can be found under the `src` folder and snippets are stored in the `snippets` directory.

## License

This project is licensed under the [MIT License](./LICENSE).
