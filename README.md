# flare-fassets-cross-chain-agent

[![Solidity](https://img.shields.io/badge/Solidity-0.8.24-363636?logo=solidity)](https://soliditylang.org/)
[![Foundry](https://img.shields.io/badge/Built%20with-Foundry-FF4B4B.svg)](https://getfoundry.sh/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

State connector attestation verifier and non-smart contract asset minting agent on Flare.

## Architecture

```mermaid
graph TD
    User([User / DApp]) -->|Execute Transaction| Sequencer[Rollup Sequencer / Batcher]
    Sequencer -->|Submit State Batch| L2Verifier[L2 State Verification Contract]
    L2Verifier -->|State Finalization| Settlement[Ethereum L1 Settlement]
```

## Features
- **Gas Efficiency**: Optimized inline assembly and EVM via-IR compilation.
- **Security**: Built-in re-entrancy protection and cryptographic signature checks.
- **Compatibility**: Adheres to ERC-4337 and modular rollup standards.

## Testing & Compilation
```bash
forge build
forge test -vvv
```

## License
MIT
