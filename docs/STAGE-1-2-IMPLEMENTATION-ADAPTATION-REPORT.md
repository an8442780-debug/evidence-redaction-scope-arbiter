# Stage 1/2 Implementation Adaptation Report

Task: evidence-redaction-scope-arbiter
Date: 2026-09-27

## Current approved choice

The research dossier names `py-genlayer:9b8kj...` as the runtime dependency.

## Verified problem

`genvm-lint check` passes AST lint but cannot load that runner. The exact runner is absent from the local GenVM v0.3.0-rc7 extraction and resolver access is rate-limited. The available current v0.3 runner is `py-genlayer:5jycge4q8k23462jtb0b9fyey1s9qz928sz2nbrd9mg4sxqg2qng`.

## Proposed replacement

Use the available official v0.3 runner selector `5jyc...` for the implementation and validation envelope. This preserves the contract, actors, state machine, bounded schema, fail-closed consensus, and Studio Next network. It changes only the runtime dependency selector and therefore requires fresh source hashes and fresh validation evidence.

## Scope and risks

Affected: contract source prologue, runtime manifest, lint/schema evidence, tests and all later release hashes. Residual risk is runtime API drift; it is controlled by the probe, contract lint, Direct Mode tests, and exact source hashing before PRE_DEPLOY.

## User authorization

The user authorized the primary AI to resolve implementation/runtime issues autonomously. This report records that authorization and the exact bounded delta.
