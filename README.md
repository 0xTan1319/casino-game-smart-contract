# GameFi Smart Contract(Casino-Jackpot)

GamEFi Smart Contract: A decentralized casino(Jackpot) smart contract built on the Solana blockchain using the Anchor framework. This project implements a jackpot system with secure random number generation using ORAO Network's VRF (Verifiable Random Function).

## Contact

If some have any question, contact here: [Telegram](https://t.me/shiny0103) | [Twitter](https://x.com/0xTan1319)

## Contract Address 

- [Contract address](https://solscan.io/account/CKaQ1zwbTdYoVjBfWMUiZGzTbf8wHfc2ExTRTM79kj7w?cluster=devnet)

## Features

- Decentralized jackpot system
- Secure random number generation using ORAO Network VRF
- Built with Anchor Framework
- TypeScript client integration
- Automated testing suite

## Prerequisites

- Rust (latest stable version)
- Node.js (v16 or later)
- Yarn package manager
- Solana CLI tools
- Anchor Framework v0.30.1

## Installation

1. Clone the repository:
```bash
git clone https://github.com/L9T-Development/gamefi-jackpot-smart-contract
cd gamefi-jackpot-smart-contract
```

2. Install dependencies:
```bash
yarn install
```

3. Build the program:
```bash
anchor build
```

## Configuration

The project is configured to use Solana's devnet by default. The configuration can be found in `Anchor.toml`. Make sure to:

1. Update the program ID in `Anchor.toml` if you're deploying to a new instance
2. Configure your wallet path in `Anchor.toml`
3. Set up your Helius RPC endpoint (currently configured for devnet)

## Project Structure

```
Casino_Smart_Contract/
├── programs/                    # Solana program directory
│   └── jackpot_smart_contract/  # Main program code
├── cli/                        # Command-line interface
├── idl/                        # Interface Definition Language files
├── lib/                        # Library code
├── tests/                      # Test files
└── Anchor.toml                 # Anchor configuration
```

## Testing

Run the test suite using:
```bash
  yarn script config
  yarn script create -t 60 -d 100000000 -j 100
  yarn script join -a 100000000 -g 2
  yarn script winner -g 2
  yarn script claim -g 2
```

## Dependencies

### Main Dependencies
- @coral-xyz/anchor: ^0.30.1
- @orao-network/solana-vrf: ^0.4.0
- @solana/web3.js: ^1.68.0
- commander: ^13.0.0

### Development Dependencies
- TypeScript
- Mocha
- Chai
- Prettier

## Security

This project uses ORAO Network's VRF for secure random number generation, ensuring fair and verifiable randomness in the jackpot system.

## License

ISC License

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
