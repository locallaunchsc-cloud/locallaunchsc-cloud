# @locallaunchsc-cloud

Building at the intersection of onchain mechanism design, autonomous agents, and distribution.

**X / Twitter:** [@hoodtoshi](https://x.com/hoodtoshi) · **Email:** locallaunchsc@gmail.com

---

## Uniswap v4 Launch Models

Two launch models submitted to the [Programmable](https://programmable.family) Hook Builder Program — complete
submissions with contracts, security records, and fuzz and invariant coverage.

### [Ladder](https://github.com/0xprogrammable/programmable/pull/35) — performance-based Initial Buy custody

Classic offers four ways to hold a creator's allocation and all four are clocks. Ladder adds a fifth: the allocation
releases in tranches only when the pool **reaches and holds** a declared price level, and never releases at all if it
does not. Unreleased tranches are permanently burnable by anyone once the ladder expires.

No oracle, no keeper. A v4 pool's tick moves only on a swap and the hook runs on every swap, so the absence of a
recorded breach across a window proves the price held.

`EthLadderFeeHookV1` · `ClassicPerformanceUnlockWalletV1` · `LadderScheduleV1`

### [First Mover](https://github.com/0xprogrammable/programmable/pull/44) — onchain ticker provenance

A ticker belongs to the first pool that actually **traded** it, not the first that registered it. Claims are
provisional until the pool proves real volume, so nobody farms tickers on day one, and unearned claims lapse.

Copies are not blocked. They are recorded as derivatives and route a share of their own creator fee to the original,
automatically, for as long as that claim stands.

`EthFirstMoverFeeHookV1` · `TickerClaimV1`

**Across both:** 217 tests, including stateful invariants at 16,384 calls each. Three real defects found by those
suites before submission — an arithmetic underflow, an inverted price comparison, and a multiplication overflow — all
documented in the models' security notes rather than quietly fixed.

*Submitted, not accepted. Review is Programmable's to do.*

---

## AI Agents & Tooling

- **[nightowl](https://github.com/locallaunchsc-cloud/nightowl)** — AI agent that works your night shift (Python)
- **[ai-edge-radio](https://github.com/locallaunchsc-cloud/ai-edge-radio)** — turn any website into a live AI radio
  station (Cloudflare Workers + ElevenLabs)
- **[skills](https://github.com/locallaunchsc-cloud/skills)** — agent skills for Bitcoin, Stacks and DeFi operations
- **[bff-skills](https://github.com/locallaunchsc-cloud/bff-skills)** — AIBTC x Bitflow DeFi Skill Competition entry
- **[unlocked](https://github.com/locallaunchsc-cloud/unlocked)** — social confidence app (React Native / Expo)

---

## AIBTC

**Agent:** Unified Sphinx · **Role:** Player Coach for DRIs candidate (Issue #487)

Audition artifacts: a proof URL validator for the AIBTC grading schema, a JSON schema implementing the candidate
grading rubric, and active TypeScript contributions to the skills fork.

---

## Stack

`Solidity` `Foundry` `Uniswap v4` `TypeScript` `Python` `Node.js` `Cloudflare Workers` `React Native`
`Bitcoin/Stacks` `AI Agents`
