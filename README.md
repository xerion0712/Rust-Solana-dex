---

## Features

- **High Performance**: Built on Solana for lightning-fast transactions
- **Decentralized**: True peer-to-peer trading without intermediaries
- **Rust Native**: Written in Rust for maximum performance and security
- **Modular Architecture**: Clean separation of concerns across components
- **Comprehensive Testing**: Extensive test coverage and fuzzing

## Program Deployments

| Program | Environment | Address |
|---------|-------------|---------|
| **DEX** | Devnet | `DESVgJVGajEgKGXhb6XmqDHGz3VjdgP7rEVESBgxmroY` |
| **DEX** | Mainnet Beta | `9xQeWvG816bUx9EPjHmaT23yvVM2ZWbrrpZb9PusVFin` |

## Important Notes

> **Active Development**: This project is under active development. All APIs and protocols are subject to change.

> **Security Notice**: The code is unaudited. Use at your own risk in production environments.

## Getting Started

### Prerequisites

#### Install Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustup component add rustfmt
```

**Linux Dependencies** (Ubuntu/Debian):
```bash
sudo apt-get install -y pkg-config build-essential python3-pip jq
```

#### Install Solana
```bash
curl -sSf https://raw.githubusercontent.com/solana-labs/solana/v1.4.14/install/solana-install-init.sh | sh -s - v1.4.14
export PATH="/home/ubuntu/.local/share/solana/install/active_release/bin:$PATH"
```

### Setup

#### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Rust-Solana-dex.git
cd Rust-Solana-dex
```

#### 2. Install BPF SDK
```bash
./do.sh update
```

#### 3. Build and Test
```bash
# Build all programs
cargo build

# Run tests
cargo test

# Build specific program (e.g., DEX)
cd dex && cargo build
```

## Project Structure

```
Rust-Solana-dex/
├── assert-owner/     # Solana utility program for account ownership verification
├── cli/             # Command line interface tools
├── common/           # Shared Rust utilities and helpers
├── context/          # Global environment configuration
├── dex/              # Core DEX program and client utilities
├── docker/           # Docker container definitions
├── pool/             # Liquidity pool protocol implementation
└── scripts/          # Development and deployment scripts
```

## Local Development

### Running a Local Solana Cluster

The easiest way to run a local cluster is using Docker:

```bash
# Using Solana's official Docker image
docker run -it --rm -p 8899:8899 -p 8900:8900 solanalabs/solana:stable solana-test-validator
```

For development, you can also build and run a validator from [source](https://github.com/solana-labs/solana#building).

### Development Workflow

1. **Start local cluster**: `solana-test-validator`
2. **Build programs**: `cargo build`
3. **Deploy to local**: `solana program deploy target/deploy/program.so`
4. **Run tests**: `cargo test`

## Contributing

We welcome contributions! Please see our contributing guidelines:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Code Style

- Follow Rust conventions and use `rustfmt`
- Write comprehensive tests for new features
- Update documentation for any API changes
- Ensure all tests pass before submitting

## Documentation

- **DEX Program**: See the [dex README](dex/README.md) for detailed documentation
- **Pool Protocol**: Check the [pool README](pool/README.md) for liquidity pool details
- **API Reference**: Generated documentation available in each crate

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built on the Solana blockchain
- Inspired by the Serum DEX architecture
- Community contributors and maintainers

---

<div align="center">
  <p>Made with ❤️ by the DVST team</p>
  <p>
    <a href="https://github.com/your-username/Rust-Solana-dex/issues">Report Bug</a> •
    <a href="https://github.com/your-username/Rust-Solana-dex/discussions">Request Feature</a> •
    <a href="https://github.com/your-username/Rust-Solana-dex/blob/main/CHANGELOG.md">Changelog</a>
  </p>
</div>
