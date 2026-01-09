# Corvina Ledger — Entry 0010

## Title
Smart Contract v1 — Intent Mapping

## Date
2026-01-09

## Purpose
This entry maps each function of the Corvina Sigil Jeton (CSJ)
v1 smart contract to its explicit intent.

The goal is to ensure that:
- code behavior is never ambiguous
- no function exists without a declared purpose
- reviewers can understand *why* a function exists, not only *what* it does

This document binds code to meaning.

## Design Philosophy

The v1 smart contract is:
- minimal
- non-upgradeable
- intentionally incomplete

It is not designed to scale.
It is designed to **demonstrate truthfully**.

## Function Map

---

### Function: `mint(address to, uint256 amount)`

**Intent**
Create CSJ only as the result of:
- completed physical archival
- recorded ledger declaration
- declared mint quantity

**Constraints**
- callable only by Founder/Minter role
- callable only while minting is unpaused
- callable only to Treasury address

**Ethical Rule**
Minting is an act of documentation, not of creation.
Value precedes the token.

---

### Function: `pauseMinting()`

**Intent**
Seal the minting phase permanently.

**Constraints**
- callable only by Founder/Minter role
- once called, cannot be reversed

**Ethical Rule**
History must not be editable.
Completion is more important than flexibility.

---

### Function: `transfer(address to, uint256 amount)`

**Intent**
Distribute CSJ after minting
to Founders, Keepers, or early supporters.

**Constraints**
- standard ERC-style transfer rules
- does not affect total supply

**Ethical Rule**
Distribution follows transparency.
No transfer hides origin.

---

### Function: `balanceOf(address owner)`

**Intent**
Allow anyone to verify balances.

**Ethical Rule**
No secrecy of ownership within the system.

---

### Function: `totalSupply()`

**Intent**
Expose final CSJ supply.

**Ethical Rule**
Scarcity must be observable, not promised.

---

## Explicit Non-Functions (v1)

The following are intentionally absent:

- ❌ no burn()
- ❌ no upgrade()
- ❌ no role reassignment
- ❌ no batch minting
- ❌ no hidden allocation logic

**Reason**
Anything not essential to the first demonstration
is postponed to later versions.

## Relationship to Ledger

- Ledger defines *what may happen*
- Smart contract executes *what already happened*

If a conflict exists:
- the ledger entry is examined first
- the transaction is interpreted second

## Auditability

This mapping allows:
- human audit
- legal reasoning
- ethical review

without requiring trust in the deployer.

## Status
Smart contract v1 intent fully mapped.

## Closing Note
Code is not neutral.
Every function is a statement.
Silence is also a choice.
