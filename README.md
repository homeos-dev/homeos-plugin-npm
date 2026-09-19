# homeos-plugin-npm

![License](https://img.shields.io/badge/license-MIT%20OR%20Apache--2.0-blue)

A [homeos](https://github.com/homeos-dev/homeos) plugin for [npm](https://github.com/npm/cli), a JavaScript package manager.

## Usage

Add the plugin to your homeos repository:

```sh
homeos plugin add npm
```

Create a package using this plugin:

```sh
homeos package add tsx --plugin npm --param name=tsx
```

## Parameters

| Parameter | Description |
|-----------|-------------|
| `name` | npm package name (e.g., `tsx`) |

## Actions

| Action | Command |
|--------|---------|
| install | `npm install -g {{name}}` |
| update | `npm update -g {{name}}` |
| uninstall | `npm uninstall -g {{name}}` |

> [!NOTE]
> The templates do not invoke `sudo`. This assumes a user-space Node.js installation (via nvm, volta, fnm, etc.) where global packages do not require elevated privileges. If you use a system-installed Node.js, edit the scripts after `homeos package add` to prepend `sudo`.

## License

Licensed under either of

 * Apache License, Version 2.0
   ([LICENSE-APACHE](LICENSE-APACHE) or <http://www.apache.org/licenses/LICENSE-2.0>)
 * MIT license
   ([LICENSE-MIT](LICENSE-MIT) or <http://opensource.org/licenses/MIT>)

at your option.

## Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
