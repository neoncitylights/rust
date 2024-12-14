# Rust Repository Template 🦀
Repository template to get quickly started with writing Rust libraries, ready for distributing.

## Features
- [x] Remote development support with [GitHub Codespaces](https://github.com/features/codespaces)
- [x] CI/CD support with [GitHub Actions](https://github.com/features/actions)
- [x] Deploys latest/nightly docs to GitHub Pages (without `gh-pages` branch) via [`actions/deploy-pages`](https://github.com/actions/deploy-pages) action
- [x] Running unit/integration/doc tests
- [x] Running [Rustfmt](https://github.com/rust-lang/rustfmt) and [Clippy](https://github.com/rust-lang/rust-clippy) for detecting formatting and linting errors, respectively
- [x] Weekly, midnight scheduled audits of Rust packages for software vulnerabilities with [`cargo-audit`](https://crates.io/crates/cargo-audit) via [`rustsec/audit-check`](https://github.com/rustsec/audit-check) action (maintained by the Secure Code Working Group).
- [x] Includes dual licenses under [MIT](./LICENSE-MIT)/[Apache-2.0](./LICENSE-APACHE) by default to ensure compatibility with the Rust ecosystem (see [`C-PERMISSIVE`](https://rust-lang.github.io/api-guidelines/necessities.html#crate-and-its-dependencies-have-a-permissive-license-c-permissive) section from Rust API Guidelines book)

## Getting started
### Creating a new repository
Choose a method:
- **GitHub UI**: Press the "Use this template" button in the top-right corner of this page.
- **GitHub CLI**: Install [GitHub CLI](https://cli.github.com). Then run one of the following:
  ```shell
  gh repo create --template neoncitylights/php --public --clone {{repository}}  # clone as public
  gh repo create --template neoncitylights/php --private --clone {{repository}} # clone as private
  ```

### Replace placeholders
Replace the following placeholders with your editor's find-and-replace:
- `{{library}}` - The name of the library.
- `{{desc}}` - The description of the library.
- `{{author}}` - The author's name of the library. For example, this could be a username, nickname, or real name.
- `{{email}}` - The author's email address. This is optional and can be deleted.
- `neoncitylights/rust` - Replace this with the name of your repository.
- `my-crate`, `my_crate` - Replace this with the name of your crate.

## Configure
| Tool                     | File path                                                | Reference                                                                                                        |
|--------------------------|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| GitHub Codespaces        | [`devcontainer.json`](./.devcontainer/devcontainer.json) | [Reference](https://containers.dev/implementors/json_reference/)                                                 |
| GitHub Actions           | [`.github/workflows`](./.github/workflows)               | [Reference](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions)               |
| Cargo package            | [`Cargo.toml`](crates/pkg1/Cargo.toml)                            | [Reference](https://doc.rust-lang.org/cargo/reference/manifest.html)                                             |
| Clippy (Rust linter)     | [`.clippy.toml`](./.clippy.toml)                         | [Repository](https://github.com/rust-lang/rust-clippy), [Reference]( https://rust-lang.github.io/rust-clippy/) |
| Rustfmt (Rust formatter) | [`.rustfmt.toml`](./.rustfmt.toml)                       | [Repository](https://github.com/rust-lang/rustfmt), [Reference](https://rust-lang.github.io/rustfmt/)           |

## Run scripts locally
| Script      | Command |
|-------------|---------|
| Run unit/integration/doc tests | `cargo test` |
| Run Rustfmt | `cargo fmt` |
| Run Clippy | `cargo clippy` |
| Generate API docs for crate | `cargo doc` |
| Generate mdBook docs for crate | `mdbook build` (in `crates/**/book`) |
| Run security audits | `cargo audit`[^cargo-audit] |

[^cargo-audit]: Requires installing [`cargo-audit`](https://crates.io/crates/cargo-audit) locally
