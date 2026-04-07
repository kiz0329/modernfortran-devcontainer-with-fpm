# Modernfortran Devcontainer With Fpm

A Fortran development environment using gfortran and fpm (Fortran Package Manager).  
Configured as a VS Code Dev Container so you can start developing Fortran right away.

## Development Environment

| Tool | Version |
|------|---------|
| gfortran | 14.2.0 |
| fpm | 0.13.0, alpha |
| Python | 3.12 |

## Prerequisites

- [Docker](https://www.docker.com/)
- [VS Code](https://code.visualstudio.com/) + [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Setup

1. Click **Use this template** → **Create a new repository** on GitHub
2. Clone your new repository
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
3. Open the folder in VS Code and select "Reopen in Container"
4. Once the container build completes, the development environment is ready to use

## Usage

### Initialize fpm in your repository

```bash
fpm new --backfill <your-project-name>
```

### Build and run

```bash
fpm build
fpm run
```

### Test

```bash
fpm test
```

## Python Packages (pip)

The following packages are installed via `pip` from `requirements.txt`:

| Package | Version | Description |
|---------|---------|-------------|
| [fortls](https://github.com/fortran-lang/fortls) | 3.2.2 | Fortran Language Server — provides IDE features such as autocomplete, go-to-definition, and diagnostics |
| [fprettify](https://github.com/pseewald/fprettify) | 0.3.7 | Fortran source code auto-formatter |
| [fypp](https://github.com/aradi/fypp) | 3.2 | Fortran preprocessor supporting Python-like metaprogramming directives |
| [findent](https://sourceforge.net/projects/findent/) | 4.3.6 | Fortran source code indenter and converter |

## VS Code Extensions

The following extensions are automatically installed in the container:

- **Modern Fortran** (`fortran-lang.linter-gfortran`) — Syntax highlighting, linter, formatter
- **Even Better TOML** (`tamasfe.even-better-toml`) — Editing support for fpm.toml

## License

[CC0 1.0 Universal](LICENSE)
