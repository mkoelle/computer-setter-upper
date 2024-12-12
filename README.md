computer-setter-upper
=================

A tool to set your computer up just the way I like it.


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/computer-setter-upper.svg)](https://npmjs.org/package/computer-setter-upper)
[![Downloads/week](https://img.shields.io/npm/dw/computer-setter-upper.svg)](https://npmjs.org/package/computer-setter-upper)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g computer-setter-upper
$ csu COMMAND
running command...
$ csu (--version)
computer-setter-upper/0.0.0 darwin-arm64 node-v22.4.1
$ csu --help [COMMAND]
USAGE
  $ csu COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`csu hello PERSON`](#csu-hello-person)
* [`csu hello world`](#csu-hello-world)
* [`csu help [COMMAND]`](#csu-help-command)
* [`csu plugins`](#csu-plugins)
* [`csu plugins add PLUGIN`](#csu-plugins-add-plugin)
* [`csu plugins:inspect PLUGIN...`](#csu-pluginsinspect-plugin)
* [`csu plugins install PLUGIN`](#csu-plugins-install-plugin)
* [`csu plugins link PATH`](#csu-plugins-link-path)
* [`csu plugins remove [PLUGIN]`](#csu-plugins-remove-plugin)
* [`csu plugins reset`](#csu-plugins-reset)
* [`csu plugins uninstall [PLUGIN]`](#csu-plugins-uninstall-plugin)
* [`csu plugins unlink [PLUGIN]`](#csu-plugins-unlink-plugin)
* [`csu plugins update`](#csu-plugins-update)

## `csu hello PERSON`

Say hello

```
USAGE
  $ csu hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ csu hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/mkoelle/computer-setter-upper/blob/v0.0.0/src/commands/hello/index.ts)_

## `csu hello world`

Say hello world

```
USAGE
  $ csu hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ csu hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/mkoelle/computer-setter-upper/blob/v0.0.0/src/commands/hello/world.ts)_

## `csu help [COMMAND]`

Display help for csu.

```
USAGE
  $ csu help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for csu.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.19/src/commands/help.ts)_

## `csu plugins`

List installed plugins.

```
USAGE
  $ csu plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ csu plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.22/src/commands/plugins/index.ts)_

## `csu plugins add PLUGIN`

Installs a plugin into csu.

```
USAGE
  $ csu plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into csu.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CSU_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CSU_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ csu plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ csu plugins add myplugin

  Install a plugin from a github url.

    $ csu plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ csu plugins add someuser/someplugin
```

## `csu plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ csu plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ csu plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.22/src/commands/plugins/inspect.ts)_

## `csu plugins install PLUGIN`

Installs a plugin into csu.

```
USAGE
  $ csu plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into csu.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CSU_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CSU_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ csu plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ csu plugins install myplugin

  Install a plugin from a github url.

    $ csu plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ csu plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.22/src/commands/plugins/install.ts)_

## `csu plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ csu plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ csu plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.22/src/commands/plugins/link.ts)_

## `csu plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ csu plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ csu plugins unlink
  $ csu plugins remove

EXAMPLES
  $ csu plugins remove myplugin
```

## `csu plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ csu plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.22/src/commands/plugins/reset.ts)_

## `csu plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ csu plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ csu plugins unlink
  $ csu plugins remove

EXAMPLES
  $ csu plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.22/src/commands/plugins/uninstall.ts)_

## `csu plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ csu plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ csu plugins unlink
  $ csu plugins remove

EXAMPLES
  $ csu plugins unlink myplugin
```

## `csu plugins update`

Update installed plugins.

```
USAGE
  $ csu plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.22/src/commands/plugins/update.ts)_
<!-- commandsstop -->
