<h1 align="center">
  <p><a href="https://github.com/z-shell/zi">
  <img src="https://github.com/z-shell/zi/raw/main/docs/images/logo.svg" alt="Logo" width="60px" height="60px" /></a>
	❮ ZI ❯ Package - Asciidoctor </p></h1>
<h3 align="center">
<table>
    <tr>
        <td><b>Package source:</b></td>
        <td>Source Tarball</td>
        <td>Binary</td>
        <td>Git</td>
        <td>Node</td>
        <td>Gem</td>
    </tr>
    <tr>
        <td><b>Status:</b></td>
        <td>❌</td>
        <td>❌</td>
        <td>❌</td>
        <td>❌</td>
        <td>✔️ (default)</td>
    </tr>
</table>
</h3><hr />

## Available `pack''` invocations

[asciidoctor/asciidoctor](https://github.com/asciidoctor/asciidoctor) by the [bin-gem-node](https://github.com/z-shell/z-a-bin-gem-node) annex:

```shell
# Download the Gem of asciidoctor locally into the plugin directory
# Using the `@' prefix because of collision with the as'' ice
zi pack for @asciidoctor
```

## Default Profile

Provides the CLI command `asciidoctor`.

The Gem is installed locally into a null-plugin directory (feature of the bin-gem-node annex) and provided to the command line through _shims_, i.e.: automatic forwarder scripts created under `$ZPFX/bin` (which is added to the `$PATH` by default; shims are also a bin-gem-node annex feature).

The ZI command executed will be equivalent to:

```shell
zi lucid as='null' for \
  node="!asciidoctor" sbin="g:bin/asciidoctor" \
    z-shell/null
```

---

> This repository compatible with [ZI](https://github.com/z-shell/zi)

The [asciidoctor/asciidoctor](https://github.com/asciidoctor/asciidoctor) zsh package than can use the [zsh-string-lib](https://github.com/z-shell/zsh-string-lib) to automatically:

- get the plugin's Git repository OR release-package URL,
- get the list of the recommended ices for the plugin,
  - there can be multiple lists of ices,
  - the ice lists are stored in _profiles_; there's at least one profile, _default_,
  - the ices can be selectively overridden.
