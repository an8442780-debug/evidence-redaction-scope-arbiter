# Studio Tool Readiness

- Toolchain: `E:\Genlayer-Tools\studio-next-toolchain`
- JavaScript packages: `genlayer 0.40.0-rc.3`, `genlayer-js 2.0.0-rc.1`, `@genlayer/transaction-kit 0.1.0-rc.2`
- RPC: `https://studio-dev.genlayer.com/api`
- Chain ID: `61997` verified by `eth_chainId -> 0xf22d`
- Actor: `ic-deployer`, `0xf5c66e5155a62e27047ad4cce729593d6b9c03fc`
- Balance: `0x1607a4c6ef81d21` observed through read-only RPC
- Private key handling: external encrypted keystore only; no secret copied into the project
- Broadcasts: `0`

Deployment remains a separate governed action and will use one stable operation ID, one broadcast, and independent finality/semantic/readback reconciliation.
