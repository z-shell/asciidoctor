<h3>

| **Package source:** | Source Tarball | Binary | Git | Node |             Gem              |
| :-----------------: | :------------: | :----: | :-: | :--: | :--------------------------: |
|     **Status:**     |      :x:       |  :x:   | :x: | :x:  | :heavy_check_mark: (default) |

</h3>

- [Introduction](#introduction)
- [Install](#install)
	- [Available `pack''` invocations](#available-pack-invocations)
	- [Default Profile](#default-profile)

# Introduction

> **[?]**
> This repository not compatible with previous versions (zplugin, zinit).
>
> Please upgrade to [ZI](https://github.com/z-shell-zi)

The [asciidoctor/asciidoctor](https://github.com/asciidoctor/asciidoctor) zsh package than can use the NPM package registry to automatically:

-   get the plugin's Git repository OR release-package URL,
-   get the list of the recommended ices for the plugin,
    -   there can be multiple lists of ices,
    -   the ice lists are stored in _profiles_; there's at least one profile, _default_,
    -   the ices can be selectively overridden.

# Install

## Available `pack''` invocations

[asciidoctor/asciidoctor](https://github.com/asciidoctor/asciidoctor) by using the [bin-gem-node](https://github.com/z-shell/z-a-bin-gem-node) annex:

```zsh
# Download the Gem of asciidoctor locally into the plugin directory
# Using the `@' prefix because of collision with the as'' ice
zi pack for @asciidoctor
```

## Default Profile

Provides the CLI command `asciidoctor`.

The Gem is installed locally into a null-plugin directory (feature of the
bin-gem-node annex) and provided to the command line through _shims_, i.e.:
automatic forwarder scripts created under `$ZPFX/bin` (which is added to the
`$PATH` by default; shims are also a bin-gem-node annex feature).

The ZI command executed will be equivalent to:

```zsh
zi lucid as=null node="!asciidoctor" sbin="g:bin/asciidoctor" for \
    z-shell/null
```
