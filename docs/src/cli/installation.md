# Installation
**selene** is written in Rust, and the recommended installation method is through the [Cargo package manager](https://doc.rust-lang.org/cargo/).

To use Cargo, you must first install Rust. [rustup.rs](https://rustup.rs/) is a tool that makes this very easy.

Once you have Rust installed, use either command:

**If you want the most stable version of selene**
```
cargo install selene
```

**If you want the most up to date version of selene**
```
cargo install --branch main --git https://github.com/Kampfkarren/selene selene
```

### Disabling Roblox features
selene is built with Roblox specific lints by default. If you don't want these, type `--no-default-features` after whichever command you choose.

### pre-commit

You can use Selene with [pre-commit](https://pre-commit.com/).
There are 2 possible pre-commit hooks available:

- `selene`: automatically installs the relevant prebuilt binary from GitHub releases.
- `selene-system`: runs a `selene` binary available on the PATH. The binary must be pre-installed

Add the following to your `.pre-commit-config.yaml` file:

```yaml
- repo: https://github.com/Kampfkarren/selene
  rev: v0.27.1
  hooks:
    - id: selene # or selene-system
```
