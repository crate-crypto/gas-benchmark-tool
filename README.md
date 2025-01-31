# Odometer

A tool for benchmarking Ethereum clients.

## Prerequisites

Docker required.

## Usage

- Start up docker cli
- Type `cargo run` to run the binary.

## Project structure

```sh
Cargo.toml                  # Workspace configuration
📁 clients                  # Docker files for clients
├── geth.yaml
└── ...
📁 config
├── config.toml             # Project configuration
├── entrypoint.sh           # Docker entrypoint file
├── genesis.json            # Genesis configuration
└── jwt.hex                 # Jwt token
📁 profiler                 # Benchmarking logic
├── Cargo.toml
└── 📁 src
    ├── bench_summary.rs    # Payload interface
    ├── docker.rs           # Docker interface
    ├── engine_api.rs       # Engine API interface
    ├── kute.rs             # Client interface
    └── main.rs             # Entrypoint
```

## License

MIT/APACHE

## Acknowledgements

The idea to use engine api and benchmark engine api requests was from [Nethermind's gas benchmarking tool](https://github.com/NethermindEth/gas-benchmarks)
