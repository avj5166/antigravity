# TODOS

Deferred work captured during /plan-eng-review (2026-05-20). Each item has a trigger condition for when to act on it.

---

## v2: attestMilestone enforcement guard on queueDisbursement

**What:** Add a `milestoneAttested` boolean to `CharityCampaign.sol`. `attestMilestone()` sets it to `true`. `queueDisbursement()` adds `require(milestoneAttested, "No milestone attested")` and resets the flag after queuing.

**Why:** In v1, `attestMilestone()` is ceremonial — it records an IPFS hash but does not block disbursement. A technically savvy donor who reads the contract can notice that money moves without any on-chain evidence gate. This closes that transparency gap.

**Depends on / blocked by:** v1 audit complete. The guard adds new contract logic — do not add before the v1 audit or it needs to be re-audited.

**Trigger:** After v1 ships and the first disbursement cycle completes. Add before v2 goes to audit.

---

## v2: 2-of-3 multisig for approveDisbursement

**What:** Replace single-owner `approveDisbursement()` with a Gnosis Safe multisig. `approveDisbursement()` requires 2-of-3 signers (founder + two independent board members) before executing USDC transfer.

**Why:** In v1, the founder controls queue, approve, and veto — no separation of duties. The 24-hour time-lock creates a deliberate pause but no second party has real veto power. A charity lawyer reviewing the contract may flag self-approval as a governance risk depending on jurisdiction.

**Depends on / blocked by:** v1 ships and graduation criteria met (10 donors, 1 disbursement, 1 unsolicited message). Requires identifying and onboarding 2 additional signers.

**Trigger:** v1 graduation criteria met. This is the single most important trust upgrade for the protocol.

---

## Community v2: pgmq reliable fan-out for Telegram notifications

**What:** Replace the synchronous in-process fan-out loop (sleep 35ms between calls) in the Supabase Edge Function with a pgmq (PostgreSQL Message Queue) job per subscriber. Each job calls the Telegram Bot API independently; failed jobs are retried with exponential back-off. Dead-letter queue for permanently undeliverable messages.

**Why:** The v1 fan-out loop is synchronous and single-threaded. If the Edge Function times out mid-loop (Supabase Edge Function limit: 150s), subscribers beyond that point receive no notification. At ~1700 subscribers (30/sec limit → 57s), v1 is within the limit. Beyond ~3000 subscribers, reliable delivery without pgmq is not achievable.

**Depends on / blocked by:** Community v1 ships. pgmq requires installing the pgmq Postgres extension on the Supabase project. Community v1 subscriber count must approach the ~1700 cap before this is urgent.

**Trigger:** When total active subscribers exceed 500 (leading indicator) or when the first missed-delivery incident is reported by an organiser. Add before Community v2 organiser recruitment push.

---

## v2: AI routing agent (auto-queue disbursement on MilestoneAttested)

**What:** LangChain agent subscribes to `MilestoneAttested` events on-chain. On event receipt, the agent (a) fetches the IPFS evidence document, (b) runs a verification prompt to check the evidence meets the disbursement criteria, (c) calls `queueDisbursement(amount, beneficiary)` if verification passes. Founder's Telegram bot still provides the 24-hour veto window.

**Why:** In v1, the founder manually reviews evidence and calls `queueDisbursement()`. AI routing removes the founder as a bottleneck — the charity can process disbursements faster and at lower operational cost. This is the "agentic AI" differentiator that makes this more than a standard escrow contract.

**Depends on / blocked by:** v1 ships. LangChain + on-chain event listener is M scope (~2 weeks human / ~2 hours CC). Requires defining the verification prompt and success criteria for each campaign type.

**Trigger:** v1 graduation criteria met. Start design when v1 ships — this is the core v2 innovation.
