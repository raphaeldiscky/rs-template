<h1 align="center">Rust Template</h1>

A simple Rust project template with pre-configured linting, formatting, security scanning, git hooks, and CI.

## Quick Start

Install the pinned toolchain, then the project tools and dependencies:

```sh
proto use          # installs every toolchain pinned in .prototools
task install_tools # project tools + dependencies + git hooks
```

Day to day:

```sh
task sync          # install the exact deps in the lockfiles (after cloning or pulling)
task upgrade       # bump all deps to their latest versions and update the lockfiles
```

## Commands

| Command | Description |
| --- | --- |
| `task install_tools` | Install tools, dependencies and git hooks |
| `task sync` | Install exact dependencies from the lockfiles |
| `task upgrade` | Upgrade all dependencies to latest |
| `task format` | Run cargo fmt |
| `task lint` | Run clippy with -D warnings |
| `task deadcode` | Check for dead code |
| `task security` | Security and license checks (cargo deny) |
| `task unused_deps` | Find unused dependencies (cargo machete) |
| `task test` | Run tests with nextest |
| `task test:doc` | Run doc tests |
| `task build` | Build the project |
| `task run_ci` | Run the CI pipeline locally |

## Toolchain versions

Every language and tool version lives in **`.prototools`** — one file, read by
both `proto use` locally and `moonrepo/setup-toolchain` in CI. To upgrade a
language, edit that one line.


## Technologies - Libraries

- **[rust-lang/rustfmt](https://github.com/rust-lang/rustfmt)** - Rust code formatter
- **[rust-lang/rust-clippy](https://github.com/rust-lang/rust-clippy)** - Rust linter with pedantic, nursery, and cargo lint groups
- **[nextest-rs/nextest](https://github.com/nextest-rs/nextest)** - Next-generation test runner for Rust
- **[EmbarkStudios/cargo-deny](https://github.com/EmbarkStudios/cargo-deny)** - Security advisories, license compliance, and dependency checks
- **[bnjbvr/cargo-machete](https://github.com/bnjbvr/cargo-machete)** - Unused dependency detection
- **[go-task/task](https://github.com/go-task/task)** - A task runner / simpler Make alternative
- **[evilmartians/lefthook](https://github.com/evilmartians/lefthook)** - Fast and powerful Git hooks manager
- **[conventional-changelog/commitlint](https://github.com/conventional-changelog/commitlint)** - Lint commit messages
