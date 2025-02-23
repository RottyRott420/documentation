---
title: npm-repo
section: 1
description: Open package repository page in the browser
github_repo: npm/cli
github_branch: release/v8
github_path: docs/content/commands/npm-repo.md
redirect_from:
  - /cli-commands/npm-repo
  - /cli-commands/repo
  - /cli-documentation/cli-commands/npm-repo
  - /cli-documentation/cli-commands/repo
  - /cli-documentation/commands/npm-repo
  - /cli-documentation/commands/repo
  - /cli-documentation/npm-repo
  - /cli-documentation/repo
  - /cli-documentation/v8/cli-commands/npm-repo
  - /cli-documentation/v8/cli-commands/repo
  - /cli-documentation/v8/commands/npm-repo
  - /cli-documentation/v8/commands/repo
  - /cli-documentation/v8/npm-repo
  - /cli-documentation/v8/repo
  - /cli/cli-commands/npm-repo
  - /cli/cli-commands/repo
  - /cli/commands/npm-repo
  - /cli/commands/repo
  - /cli/npm-repo
  - /cli/repo
  - /cli/v8/cli-commands/npm-repo
  - /cli/v8/cli-commands/repo
  - /cli/v8/commands/repo
  - /cli/v8/npm-repo
  - /cli/v8/repo
  - /commands/npm-repo
  - /commands/repo
---

### Synopsis

<!-- AUTOGENERATED USAGE DESCRIPTIONS START -->
<!-- automatically generated, do not edit manually -->
<!-- see lib/commands/repo.js -->

```bash
npm repo [<pkgname> [<pkgname> ...]]
```

<!-- automatically generated, do not edit manually -->
<!-- see lib/commands/repo.js -->

<!-- AUTOGENERATED USAGE DESCRIPTIONS END -->

### Description

This command tries to guess at the likely location of a package's
repository URL, and then tries to open it using the `--browser` config
param. If no package name is provided, it will search for a `package.json`
in the current folder and use the `repository` property.

### Configuration

<!-- AUTOGENERATED CONFIG DESCRIPTIONS START -->
<!-- automatically generated, do not edit manually -->
<!-- see lib/utils/config/definitions.js -->
#### `browser`

* Default: OS X: `"open"`, Windows: `"start"`, Others: `"xdg-open"`
* Type: null, Boolean, or String

The browser that is called by npm commands to open websites.

Set to `false` to suppress browser behavior and instead print urls to
terminal.

Set to `true` to use default system URL opener.

<!-- automatically generated, do not edit manually -->
<!-- see lib/utils/config/definitions.js -->

#### `registry`

* Default: "https://registry.npmjs.org/"
* Type: URL

The base URL of the npm registry.

<!-- automatically generated, do not edit manually -->
<!-- see lib/utils/config/definitions.js -->

#### `workspace`

* Default:
* Type: String (can be set multiple times)

Enable running a command in the context of the configured workspaces of the
current project while filtering by running only the workspaces defined by
this configuration option.

Valid values for the `workspace` config are either:

* Workspace names
* Path to a workspace directory
* Path to a parent workspace directory (will result in selecting all
  workspaces within that folder)

When set for the `npm init` command, this may be set to the folder of a
workspace which does not yet exist, to create the folder and set it up as a
brand new workspace within the project.

This value is not exported to the environment for child processes.

<!-- automatically generated, do not edit manually -->
<!-- see lib/utils/config/definitions.js -->

#### `workspaces`

* Default: null
* Type: null or Boolean

Set to true to run the command in the context of **all** configured
workspaces.

Explicitly setting this to false will cause commands like `install` to
ignore workspaces altogether. When not set explicitly:

- Commands that operate on the `node_modules` tree (install, update, etc.)
will link workspaces into the `node_modules` folder. - Commands that do
other things (test, exec, publish, etc.) will operate on the root project,
_unless_ one or more workspaces are specified in the `workspace` config.

This value is not exported to the environment for child processes.

<!-- automatically generated, do not edit manually -->
<!-- see lib/utils/config/definitions.js -->

#### `include-workspace-root`

* Default: false
* Type: Boolean

Include the workspace root when workspaces are enabled for a command.

When false, specifying individual workspaces via the `workspace` config, or
all workspaces via the `workspaces` flag, will cause npm to operate only on
the specified workspaces, and not on the root project.

This value is not exported to the environment for child processes.

<!-- automatically generated, do not edit manually -->
<!-- see lib/utils/config/definitions.js -->

<!-- AUTOGENERATED CONFIG DESCRIPTIONS END -->

### See Also

* [npm docs](/cli/v8/commands/npm-docs)
* [npm config](/cli/v8/commands/npm-config)
