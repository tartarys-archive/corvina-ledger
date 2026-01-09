# Corvina Ledger — Entry 0004

## Title
Token Parameters Frozen (Corvina Sigil Jeton v1)

## Date
2026-01-09

## Summary
The core parameters of the Corvina Sigil Jeton (CSJ) token have been finalized and frozen
for the v1 smart contract implementation.

These parameters define the immutable technical identity of the token and may not be
altered without deploying a new contract version.

## Token Identity

- Name: Corvina Sigil Jeton
- Symbol (Ticker): CSJ
- Decimals: 0
- Standard: ERC-20 compatible (BNB Smart Chain)

## Supply Model (v1)

- Total Supply: 369,000 CSJ
- Supply Type: Fixed at deployment
- Inflation: None
- Deflation: None

The v1 supply is intentionally limited to serve as:
- a demonstrative minting example
- an initial liquidity and participation layer
- a historical anchor for future Corvina Sigil iterations

## Minting Rules (v1)

- Minting occurs once, during initial deployment
- Minting authority: Founder wallet
- Post-mint minting: permanently disabled via pause
- No automated or conditional minting logic

## Allocation Logic (Demonstrative)

The v1 mint reflects two allocation archetypes:
1. Founder allocation
2. Community (Treasury) allocation

Exact distribution is recorded off-chain in the Corvina Ledger
and reflected transparently via on-chain transfers.

## Design Rationale

- Zero decimals reinforce the concept of discrete, archival-backed jetons
- Fixed supply avoids speculative inflation narratives
- Absence of burn/mint loops prevents hidden monetary policy
- Human governance remains primary

## Status
Token parameters locked for v1.

## Ledger Integrity
This entry is immutable and recorded as part of the Corvina Ledger.
