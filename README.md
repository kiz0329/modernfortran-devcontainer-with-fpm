# Modernfortran Devcontainer With Fpm

A Fortran development environment using gfortran and fpm (Fortran Package Manager).  
Configured as a VS Code Dev Container so you can start developing Fortran right away.

## Development Environment

| Tool | Version |
|------|---------|
| gfortran | 14.2.0 |
| fpm | 0.13.0 |
| Python | 3.12 |

## Prerequisites

- [Docker](https://www.docker.com/)
- [VS Code](https://code.visualstudio.com/) + [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Setup

### Using as your own repository

```bash
git clone <repository-url>
cd modernfortran-devcontainer-with-fpm
```

### Contributing to another's repository

1. **Fork** the repository on GitHub
2. Clone your forked repository
   ```bash
   git clone <your-fork-url>
   cd modernfortran-devcontainer-with-fpm
   ```
3. Add the upstream repository as a remote
   ```bash
   git remote add upstream <original-repository-url>
   ```

### Starting the Dev Container

1. Open the folder in VS Code and select "Reopen in Container"
2. Once the container build completes, the development environment is ready to use

## Usage

### Create a new project with fpm

```bash
fpm new my_project
cd my_project
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

## VS Code Extensions

The following extensions are automatically installed in the container:

- **Modern Fortran** (`fortran-lang.linter-gfortran`) — Syntax highlighting, linter, formatter
- **Even Better TOML** (`tamasfe.even-better-toml`) — Editing support for fpm.toml

## License

[CC0 1.0 Universal](LICENSE)
