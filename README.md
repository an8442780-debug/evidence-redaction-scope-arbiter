# Evidence Redaction Scope Arbiter

A bounded GenLayer contract for validator-consensus decisions on proposed redaction ranges over public documents.

## Network

- Studio Next, chain ID `61997`
- RPC: `https://studio-dev.genlayer.com/api`
- Runtime selector: `py-genlayer:5jycge4q8k23462jtb0b9fyey1s9qz928sz2nbrd9mg4sxqg2qng`

## Lifecycle

`SUBMITTED -> REVIEWED -> FROZEN -> APPLIED|REJECTED|UNRESOLVED`

The contract bounds documents to 32 paragraphs and redaction proposals to 32 ranges. Nondeterministic output is schema-validated and compared by an equivalence validator; malformed or ambiguous output cannot mutate state.

Deployed on Studio Next at `0x1666a2d32C26cfb9eD7D63b887BE35d470eB76FA`; see [`docs/DEPLOYMENT-MANIFEST.md`](docs/DEPLOYMENT-MANIFEST.md) for the finalized transaction and readback evidence.

Public frontend: https://frontend-phi-wheat-56.vercel.app (Vercel production deployment, account/team `pcong`).
