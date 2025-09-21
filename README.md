# Rust template
A repository template to get started with writing Rust projects.

## Features
- [x] CI/CD support with [GitHub Actions](https://github.com/features/actions)
  - [x] Deploy Rustdoc documentation to GitHub Pages
  - [x] Run tests with LLVM code coverage
  - [x] [Rustfmt](https://github.com/rust-lang/rustfmt) and [Clippy](https://github.com/rust-lang/rust-clippy) for formatting and linting
  - [x] [cargo-audit](https://crates.io/crates/cargo-audit) for security auditing (by the Secure Code WG)
  - [x] [Trusted Publishing](https://crates.io/docs/trusted-publishing) with OIDC (OpenID Connect)
- [x] Includes [MIT](./LICENSE-MIT) & [Apache-2.0](./LICENSE-APACHE) licenses for ecosystem compatibility (see [Rust API Guidelines](https://rust-lang.github.io/api-guidelines/necessities.html#crate-and-its-dependencies-have-a-permissive-license-c-permissive) book)

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
- `my_crate` - Replace this with the name of your crate.

## Configure
| Tool                | File path                                  | Reference                                                                                                      |
|---------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| GitHub Actions CI   | [`.github/workflows`](./.github/workflows) | [Reference](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions)             |
| Cargo package       | [`Cargo.toml`](./Cargo.toml)     | [Reference](https://doc.rust-lang.org/cargo/reference/manifest.html)                                           |
| Clippy (Linter)     | [`.clippy.toml`](./.clippy.toml)           | [Repository](https://github.com/rust-lang/rust-clippy), [Reference]( https://rust-lang.github.io/rust-clippy/) |
| Rustfmt (Formatter) | [`.rustfmt.toml`](./.rustfmt.toml)         | [Repository](https://github.com/rust-lang/rustfmt), [Reference](https://rust-lang.github.io/rustfmt/)          |

## Run scripts locally
| Script      | Command |
|-------------|---------|
| Run tests | `cargo test` |
| Run Rustfmt | `cargo fmt` |
| Run Clippy | `cargo clippy` |
| Build crate documentation | `cargo doc` |
| Run security audits | `cargo audit` (with [`cargo-audit`](https://crates.io/crates/cargo-audit)) |
