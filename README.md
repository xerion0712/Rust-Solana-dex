<div align="center">
  <img height="170" src="https://avatars.githubusercontent.com/u/81713343?s=200&v=4?raw=true" />

  <h1>dvst-dex</h1>

  <p>
    <strong>DVST Rust Monorepo</strong>
  </p>

  

## Program Deployments

| Program | Devnet | Mainnet Beta |
| --------|--------|------------- |
| [DEX](/dex)     | `DESVgJVGajEgKGXhb6XmqDHGz3VjdgP7rEVESBgxmroY` | `9xQeWvG816bUx9EPjHmaT23yvVM2ZWbrrpZb9PusVFin` |

## Note

* **Is in active development so all APIs and protocols are subject to change.**
* **The code is unaudited. Use at your own risk.**

## Contributing

### Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustup component add rustfmt
```

On Linux systems you may need to install additional dependencies. On Ubuntu,

```bash
sudo apt-get install -y pkg-config build-essential python3-pip jq
```

### Install Solana

```bash
curl -sSf https://raw.githubusercontent.com/solana-labs/solana/v1.4.14/install/solana-install-init.sh | sh -s - v1.4.14
export PATH="/home/ubuntu/.local/share/solana/install/active_release/bin:$PATH"
```

### Download the source

```bash
git clone https://github.com/
```

### Install the BPF SDK

```bash
./do.sh update
```

### Build, deploy, and test programs

See individual crates for documentation. For example, to build the dex see its [README](https://github.com/project-serum/serum-dex/tree/master/dex).

## Running a local Solana cluster

The easiest way to run a local cluster is to run the docker container provided by Solana.
Instructions can be found [here](https://solana-labs.github.io/solana-web3.js/). For local development, however, it's often convenient to build and run a validator from [source](https://github.com/solana-labs/solana#building).

## Directories

* `assert-owner`: Solana utility program for checking account ownership.
* `cli`: Serum command line interface.
* `common`: Common rust utilities.
* `context`: Global environment used by Serum crates, read from a configuration file.
* `dex`: Serum DEX program and client utility.
* `docker`: Docker image definitions.
* `pool`: Serum pool protocol.
* `scripts`: Bash scripts for development.
