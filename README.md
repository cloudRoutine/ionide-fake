# Ionide-FAKE

Ionide-FAKE is part of the [Ionide](http://ionide.io) plugin suite, used for running FAKE build scripts without leaving an editor.

## Features

- Run any build target defined in your project's FAKE build script
- Panel in which you can display output of any FAKE build run in current Atom session ( including currently running builds)

## Configuration

Since version `1.1.0`, `ionide-fake` allows the user to override the default conventions used to find and run FAKE builds. To do so You need to create an `.ionide` file in the root folder of Your project opened by Atom. The configuration file uses the [TOML](https://github.com/toml-lang/toml) language.

Here is the default configuration values used if the `.ionide` file doesn't exist or some entry is missing:

```TOML
[Fake]
linuxPrefix = "mono"
command = "build.cmd"
build = "build.fsx"
```

* Linux Prefix - command used as prefix on Linux / Mac - usually `sh` or `mono`

* Command - command executed as build taking build name as parameter - usually `build.cmd`, `build.sh`, `build.ps1`

* Build - FAKE build script, which is parsed to obtain list of possible builds - usually `build.fsx`, `fake.fsx`
