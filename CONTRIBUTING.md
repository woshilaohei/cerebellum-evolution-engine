# Contributing to Cerebellum Evolution Engine

Thank you for your interest in contributing to this project. This document outlines the process for contributing to the Cerebellum Evolution Engine.

## How to Contribute

1. **Fork** the repository
2. **Create a branch** for your feature or fix (`git checkout -b feature/your-feature`)
3. **Make your changes** with clear commit messages
4. **Submit a Pull Request** with a detailed description of changes

## Code Standards

- Python code follows PEP 8
- Rust code follows standard Rust formatting (`rustfmt`)
- All security-critical modules must maintain deterministic threshold rules
- New features must not bypass the Cerebellum's single-entry/single-exit architecture

## Security Considerations

This project implements AI safety architecture. When contributing:

- **Never introduce backdoors or debug switches** in L1 protection code
- Maintain the **read-write separation** principle — only the Cerebellum writes to the memory pool
- All new security rules must use **deterministic numerical thresholds** (not probabilistic models)
- Cross-domain extension should follow the independent detection domain pattern

## Discussion

For design philosophy discussions and architectural questions, please open an Issue with the `discussion` label.

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
