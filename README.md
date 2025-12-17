# bun-as-node

Force system to use Bun as Node.js and prevent Node.js installation on Arch Linux.

## Description

This package creates symbolic links to make Bun act as a drop-in replacement for Node.js, npm, and npx. It also prevents the installation of the official Node.js package by declaring conflicts.

## Features

- Creates symlinks: `node`, `nodejs`, `npm`, `npx` → `bun`
- Provides: `nodejs`, `npm`, `npx`
- Conflicts with: `nodejs`, `npm`
- Prevents accidental Node.js installation

## Installation

### From Source

1. Build and install the package:

```bash
makepkg -si
```

## Usage

After installation, all Node.js commands will automatically use Bun:

```bash
node --version    # Uses bun
npm install       # Uses bun
npx some-package  # Uses bun
```

## Uninstallation

To remove the package and restore the ability to install Node.js:

```bash
sudo pacman -R bun-as-node
```

## Notes

- This package requires `bun` to be installed
- Installing this package will prevent you from installing the official `nodejs` and `npm` packages
- If you need to use the official Node.js, uninstall this package first

## License

[MIT](LICENSE)
