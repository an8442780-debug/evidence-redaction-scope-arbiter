# Verification

## Runtime

- Python 3.13.6
- `genlayer-py` 0.16.3
- `genlayer-test` 0.29.2 (`gltest`)
- `genvm-lint` 0.11.1rc2
- GenLayer CLI 0.39.2
- Studio Next chain ID 61997 (`eth_chainId` returned `0xf22d`)

## Checks

- `genvm-lint check contracts/evidence_redaction_scope_arbiter.py`: PASS; lint and schema validation; 6 methods.
- `py -3.13 -m pytest -q -p no:cacheprovider`: PASS; 3 tests.
- `gltest tests -q -p no:cacheprovider`: PASS; 3 tests.

No signing, deployment, contract write, GitHub push, or Vercel action has occurred.
