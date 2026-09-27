# PRE_DEPLOY Package

Exact revision: `9bc0da7`

## Source and schema

- Contract: `contracts/evidence_redaction_scope_arbiter.py`
- SHA-256: `4C6CFE7452E1C9A11FF5A4D8CCABB66942BB217ED159BF2083FB79E015CAA497`
- `genvm-lint 0.11.1rc2 check`: PASS; schema discovered `EvidenceRedactionScopeArbiter`, 6 methods.
- Runner: `py-genlayer:5jycge4q8k23462jtb0b9fyey1s9qz928sz2nbrd9mg4sxqg2qng`

## Nondeterministic inventory

`evaluate_redaction` uses `gl.vm.run_nondet_default`; leader output is bounded to the exact decision schema and the validator independently reruns the same prompt over captured immutable paragraph hashes and ranges. Malformed output, validator exceptions, or disagreement fail closed without state mutation.

## Layered checks

- Pure policy tests: 3 passed.
- `gltest tests -q -p no:cacheprovider`: 3 passed.
- Studio Next read-only chain check: 61997.

## Live operation plan

One deployment, then sequential positive, rejection, malformed/no-write and authoritative `get_case` readback checks. Broadcast once per operation; retain operation IDs and hashes; never resubmit an ambiguous hash. `writesSubmitted=0` at package creation.

The user explicitly removed the anonymous-AI requirement for this Task. This package does not expose internal prompts, governance files, wallet secrets, or reviewer coordination artifacts.
