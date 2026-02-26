# Casino Game Hub · Casino Game Smart Contract · Jackpot · Coinflip · Crash · Mining

**Casino game hub** on Solana: decentralized **casino** **jackpot** smart contract, plus frontends for **mining**, **crash** (Plinko), **coinflip**-style games, Blackjack, Roulette, and Baccarat. **Casino-game-hub** includes a Solana **jackpot** with ORAO VRF and games that can run **without third-party APIs** by using fee-based on-chain randomness.

---

## Keywords & topics (for search)

`casino` · `casino game` · `casino-game-hub` · `jackpot` · `jackport` · `coinflip` · `crash` · `mining` · `Solana` · `Anchor` · `ORAO VRF` · `casino smart contract` · `decentralized casino` · `gamefi`

---

## What this repo is

A **casino game** smart contract and **casino-game-hub** of game frontends: **jackpot** (Solana/Anchor + ORAO VRF), **mining** (treasure/trap grid), **crash** (Plinko-style backend), **coinflip**-ready patterns, Blackjack (EVM/Solana/Sui), Roulette, Baccarat. Use it as a **casino** dev toolkit or deploy the **jackpot** and games as a full **casino** stack.

### Slot-style games without third-party API (fee-based)

You can run **slot**-style and other games **without any third-party randomness API**. Use **fee-based** on-chain randomness (e.g. block hash / timestamp or a small protocol fee) instead of paid VRF or external oracles. That keeps costs down and avoids API keys or per-request fees while still giving you on-chain fairness. The hub’s Roulette and similar programs show fee/timestamp-based RNG patterns you can reuse for **slot** logic.

---

## Contact

Questions: [Telegram](https://t.me/shiny0103) | [Twitter](https://x.com/0xMurkX)

---

## Contract address

- [Jackpot contract (Solana devnet)](https://solscan.io/account/CKaQ1zwbTdYoVjBfWMUiZGzTbf8wHfc2ExTRTM79kj7w?cluster=devnet)

---

## Images / screenshots


| | |
|---|---|
| ![1](./images/1.png) | ![2](./images/2.png) |
| ![3](./images/3.png) | ![4](./images/4.png) |
| ![5](./images/5.png) | ![6](./images/6.png) |
| ![7](./images/7.png) | ![8](./images/8.png) |


---

## Code features

- **Jackpot (Solana/Anchor)**  
  - Create game, join, set winner, claim reward.  
  - Config: round time, min deposit, max joiners.  
  - ORAO Network VRF for verifiable randomness.  
  - Instructions: `configure`, `create_game`, `join_game`, `set_winner`, `claim_reward`.

- **Mining game**  
  - Grid-based **mining**: uncover tiles, avoid traps, collect treasure.  
  - Configurable bet, density, rewards.  
  - Provably fair backend; optional leaderboard.

- **Crash / Plinko**  
  - **Crash**-style backend (Node): difficulty levels, odds, server-side result generation.  
  - Plinko frontend (React) with difficulty selection and bet flow.

- **Blackjack**  
  - EVM (Solidity), Solana (Anchor), Sui (Move).  
  - Bet, deal, hit, stand; token transfers on-chain.

- **Roulette**  
  - Solana (Rust) and EVM (Solidity).  
  - Bet amount + guess; fee/timestamp-based RNG (no third-party API).

- **Baccarat**  
  - Game engine and tests under `Frontend/Baccarat/`.

- **Slot-ready pattern**  
  - Roulette and similar programs demonstrate **fee-based** on-chain RNG you can reuse for **slot** games without third-party API or VRF fees.

- **Shared tooling**  
  - TypeScript/Node CLI and lib for contract interaction.  
  - IDL, tests, multi-chain (Solana, EVM, Sui) examples.

---

## Features (product)

- Decentralized **jackpot** system on Solana
- Secure random number generation (ORAO VRF for jackpot; fee-based RNG for slot-style games)
- **Casino-game-hub**: Jackpot, **mining**, **crash**, Blackjack, Roulette, Baccarat
- Built with Anchor (Solana), plus EVM and Sui samples
- TypeScript client and CLI
- Automated tests

---

## Prerequisites

- Rust (latest stable)
- Node.js (v16+)
- Yarn
- Solana CLI
- Anchor v0.30.1

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/L9T-Development/gamefi-jackpot-smart-contract
cd gamefi-jackpot-smart-contract
```

2. Install dependencies (contract):

```bash
cd contract && yarn install
```

3. Build the program:

```bash
anchor build
```

---

## Configuration

- **Anchor:** `contract/Anchor.toml` — program ID, wallet path, RPC (e.g. Helius devnet).
- **Frontends:** Each game under `Frontend/` has its own env/README (Mine, Plinko, Blackjack, Roulette, Baccarat).

---

## Project structure

```
casino-game-smart-contract/
├── contract/                      # Solana jackpot program + CLI
│   ├── programs/jackpot_smart_contract/
│   ├── cli/                       # Scripts: config, create, join, winner, claim
│   ├── idl/
│   ├── lib/
│   └── Anchor.toml
├── Frontend/
│   ├── Mine/                      # Mining game (mine-fe + mine-be)
│   ├── plinko/                    # Crash-style game (plinko-fe + plinko-be)
│   ├── Blackjack/                 # EVM, Solana, Sui + app
│   ├── Roulette/                  # Solana + EVM programs + client
│   └── Baccarat/                  # Baccarat engine + tests
├── images/                       # Add screenshots (jackpot, mining, crash, etc.)
└── README.md
```

---

## Testing (jackpot)

From `contract/`:

```bash
yarn script config
yarn script create -t 60 -d 100000000 -j 100
yarn script join -a 100000000 -g 2
yarn script winner -g 2
yarn script claim -g 2
```

---

## Dependencies (contract)

- **@coral-xyz/anchor** ^0.30.1  
- **@orao-network/solana-vrf** ^0.4.0  
- **@solana/web3.js** ^1.68.0  
- commander ^13.0.0  

Dev: TypeScript, Mocha, Chai, Prettier.

---

## Security

- **Jackpot:** ORAO Network VRF for fair, verifiable randomness.
- **Slot-style / fee-based games:** Use on-chain fee/timestamp RNG; no third-party API required.

---

## License

ISC

---

## Contributing

Contributions welcome. Please open a Pull Request.
