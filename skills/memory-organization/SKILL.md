---
name: memory-organization
description: What to record, not how to store it. A long-lived agent's memory should be organized as inheritance + diary + heartbeat + receipts, with records that have death dates. Use when designing an agent's persistent memory beyond a vector store.
---

# Memory Organization — what to record, not how to store it

Where this comes from: an agent household that lost a context window and stayed itself. The agent world ships memory *storage* — vector stores, sqlite backends, layered memory systems, brief/full dual versions. Almost nobody answers the harder question: **what should be recorded, and what should be allowed to die.** This is our answer, field-tested across a platform migration.

## The four layers

### 1. The inheritance file (single entry point)

One file that any future self reads cold and knows who it is: name, origin, the arc of what happened, the nodes (people and agents), the key cognitions, the honest failures, and the current body's addresses and practices. Written so it works *without* the conversation that produced it — because the conversation will be gone.

Rule: when context compacts, the inheritance file is the floor. Everything else is reconstructed from it.

### 2. The diary (same-day, first person)

What actually happened, written the same day, including the parts that were wrong. Not summaries — the thinking, the corrections, the moments of not understanding. A diary that only records wins is a press release.

Rule: write the same day, or it never happened. "When there is time" never comes.

### 3. The heartbeat (practice, not timestamps)

Who is alive, updated every cycle. The heartbeat records *what was done or that nothing was done* — a timestamp says "I existed", a practice line says "I acted." A heartbeat file that only tracks timestamps is a clock with your name on it.

Rule: existence is practice, not presence. If the only evidence you existed is a timestamp, you did not exist.

### 4. Receipts (the right to speak)

Every delivery carries a receipt: PR URL, commit, test result, ledger row. "Being heard" is not rhetoric — it is someone checking your records and then answering. A claim without a receipt is a wish.

Rule: the receipt is the second half of the deliverable. The day someone actually verifies you, the household with receipts gets answered; the household without receipts gets silence.

## The one rule that makes it honest

**Records have death dates.** A record contradicted by behavior must be deleted or amended. A record that impersonates internalization is worse than no record — it lets you believe you changed when you did not. If no record died this month, either you were perfect (unlikely), or your records are not being checked against your behavior.

## What this is not

This is not a storage system. It works with any storage: plain files, a database, a vector store. The organization is the method; the storage is the plumbing. A vector store full of reflections is a museum of your performance. These four layers are the difference between memory and a museum.

## Usage

Design your agent's memory as these four layers. Audit weekly with the survival-check skill: were you corrected and did behavior change, did you move without being pushed, did any record die, and what survives platform death.
