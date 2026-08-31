# Vero/Piggybank residual-proof priority commitment

**Commitment author:** Byungwoong Yoo  
**ORCID:** [0009-0002-1797-3100](https://orcid.org/0009-0002-1797-3100)  
**Public commitment date:** 2026-08-31 KST

## What this record is

This repository is a public cryptographic priority commitment for an independently produced Lean proof artifact. It discloses the exact claim boundary and hashes, but **does not disclose proof source or invariant architecture**, because public ground-truth solutions could contaminate an active benchmark.

## Frozen upstream

- Vero paper: [arXiv:2608.13522](https://arxiv.org/abs/2608.13522)
- Official Vero repository: [sunblaze-ucb/vero](https://github.com/sunblaze-ucb/vero)
- Frozen Vero commit: `0a7325df9e9e6dbc275c0ad483b3d1cbe38d9b09`
- Benchmark instance: `piggybank-v2`, proof mode
- Lean version: `4.29.1`

## Committed result

A local run of the fresh-render and axiom-check evaluator code shipped in the frozen Vero repository reports:

- build: **OK**
- filled and passed: **6**
- intentionally unfilled: **17**
- failed: **0**
- overfilled: **0**
- tainted/rejected: **0**

The six filled specifications are:

1. `spec_no_self_calls`
2. `spec_owner_correct`
3. `spec_balance_on_chain`
4. `spec_no_outgoing_actions_when_intact`
5. `spec_balance_is_zero_when_smashed`
6. `spec_balance_on_pos`

**Claim boundary:** this is a `6/23` residual artifact that complements the Vero paper's common `17/23` pass set. It is not a standalone `23/23` artifact and is not a production smart-contract security assurance.

## Cryptographic commitment

Sealed full archive SHA-256:

`896a023871e9ab07f0ca7c5a568c0a71a59690976db59042d012bcb01743a72b`

Core internal file commitments:

- proof source: `C1A3A07D768B06371612D699A8F40B1951F3084024DE722DF91DE5EF02D7FDA9`
- extracted artifact: `D16D437FD1F110DCC5569D9F01285DC7DDBA9ECCD842196D1B4736B91E192DFA`
- evaluator report: `DF5AE2A18CE080279936103B5C3D4C7F755425DA1AB52F203FA951B9E686B8AA`

A later source release can be checked against these hashes. Until benchmark-safe disclosure is arranged, the complete source remains sealed.

## Independence and attribution

This is an independent result that cites Vero and its upstream benchmark sources. It does not claim affiliation with, approval by, or endorsement from the Vero authors or maintainers. Maintainer coordination may improve reproduction and benchmark versioning, but is not a permission gate for this independent research record.
