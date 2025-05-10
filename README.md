# 🧪 Mush Mock Registry

## What is this?

**Mush Mock Registry** is a collection of lightweight mock packages designed for [Mush](https://github.com/javanile/mush). Each package simulates the behavior of common CLI tools like `kubectl`, `docker`, or `terraform`—without executing any real side effects.

These mocks were born from real-world needs during the development and testing of shell-based CI/CD pipelines. When you're scripting infrastructure processes, the ability to simulate a tool's behavior can dramatically simplify testing, reduce setup time, and avoid unintended consequences.

## Why Mocking?

When working with DevOps workflows, infrastructure automation, or shell scripting, mocking CLI tools provides a safe, fast, and reliable testing environment. These mock tools help in:

* 🧪 **Testing shell scripts in CI/CD pipelines**
* 🚀 **Simulating deployment workflows without touching real infrastructure**
* 🧼 **Avoiding destructive side effects during testing**
* ☁️ **Keeping tests cloud-agnostic and portable**
* 💡 **Exploring Terraform-like logic without requiring real providers**
* ⚡ **Speeding up test execution and environment bootstrapping**
* 🐳 **Using a Docker image with all mocks preinstalled for immediate use**

## Supported Testing Frameworks

You can integrate these mocks with any shell testing framework, including:

* [`bats-core`](https://github.com/bats-core/bats-core)
* [`shellspec`](https://github.com/shellspec/shellspec)
* [`bashunit`](https://github.com/pgrange/bashunit)
* Plain `bash` with manual assertions

These tools, combined with the Mush Mock Registry, provide a solid foundation for writing high-quality, testable shell scripts.

## Available Mock Packages

| Command     | Package          | Status       |
| ----------- | ---------------- | ------------ |
| `kubectl`   | `kubectl-mock`   | ✅ Ready      |
| `docker`    | `docker-mock`    | ✅ Ready      |
| `helm`      | `helm-mock`      | 🚧 WIP       |
| `terraform` | `terraform-mock` | 🔍 Exploring |
| `git`       | `git-mock`       | 🔜 Planned   |

Each package installs a mock binary that mimics the original CLI’s output and behavior, making it easy to run test scripts without actually needing the full toolchain or real backends.

## 🐳 Docker Image

To make things even easier, we provide a **Docker image** with all mocks preinstalled. This lets you:

* Run tests in isolated environments
* Simulate a full DevOps toolchain
* Avoid any host system dependencies

```bash
docker run --rm -it ghcr.io/your-org/mush-mock-registry bash
```

Inside this container, you can call `kubectl`, `docker`, `terraform`, etc.—and they’ll all behave as expected for testing purposes, but without any external effects.

## 📦 Installation with Mush

To install a mock package with Mush:

```bash
mush install kubectl-mock
```

Once installed, the `kubectl` command becomes available in your scripts, returning mock responses suitable for testing.

You can install multiple mocks as needed:

```bash
mush install docker-mock terraform-mock
```

## 🔗 Learn More

* [Mush Project](https://github.com/javanile/mush) – Minimalist package manager for Bash environments
* [bats-core](https://github.com/bats-core/bats-core) – Bash Automated Testing System
* [shellspec](https://github.com/shellspec/shellspec) – Full-featured BDD testing framework for POSIX shells
* [bashunit](https://github.com/pgrange/bashunit) – Lightweight unit testing for bash scripts
* [Docker best practices for test environments](https://docs.docker.com/develop/dev-best-practices/)

## 📜 License

This project is licensed under the [MIT License](LICENSE).
