# Ashley: community bot guide

> **Information only.** This repository explains how **Ashley**, the bot of **The 3-Minute Node
> Vault** Discord server (home of the ComfyUI YouTube channel), works. It contains **no source code,
> configuration, IDs or credentials**. The bot itself lives in a private repository.

Ashley does three jobs:

1. **Opens the door.** New people introduce themselves once, and the whole server unlocks.
2. **Rewards taking part.** Every real message, showcase post, helpful reply and reaction earns XP.
   XP brings levels, and levels bring roles with more access.
3. **Keeps spam out.** Scam posts are removed in about a second, and every removal is reviewed by
   a person.

## The short version

1. **Introduce yourself once** in `#🙋‍♂️-introduction`. Where you're from, what you make, or an image
   with a line about it. You get **level 2** and the **Member** role right away, and the workflow
   downloads unlock.
2. **Keep taking part.** Chat, share results in showcase, help people in the help forum, react to
   good posts. Up to **100 XP a day** counts.
3. **Climb the ladder.** Member (L2) → Sampler (L4) → Checkpoint (L7) → Verified Node (L11) →
   Node Architect (L15). Each role adds access.
4. **Check your progress** with `/rank` or the **📊 My progress** button in `#🙋‍♂️-introduction`.
   Only you see the answer.

## Pages

Read them in order, or jump to what you need. Every page links back here.

| # | Page | Answers |
|---|---|---|
| 1 | [Getting in: the introduction](docs/introduction.md) | Why can't I post? What counts as an intro? |
| 2 | [How XP works](docs/xp-and-levels.md) | How do I earn XP? What's the daily limit? |
| 3 | [Levels and roles](docs/levels-and-roles.md) | What does each level unlock? How long does it take? |
| 4 | [The `/rank` command](docs/rank-command.md) | How do I see my level, and what does the card mean? |
| 5 | [Spam protection](docs/spam-protection.md) | What gets removed, and what if it was a mistake? |
| 6 | [Weekly report](docs/weekly-report.md) | What's in the Monday post? |
| 7 | [Supporters (Ko-fi)](docs/supporters.md) | How does supporting on Ko-fi unlock Verified Node? |
| 8 | [How Ashley was built](docs/how-it-was-built.md) | One developer, an AI coding agent, and how it was run |
| 9 | [FAQ](docs/faq.md) | Quick answers |

## XP at a glance

| Action | XP | Limit |
|---|---|---|
| A real message (8+ characters) | 10 | once a minute |
| An image in showcase | +15 | once every 5 minutes |
| A reply in someone else's help thread | +15 | once every 5 minutes |
| Giving a reaction (Members only) | 2 | once a minute |
| Getting a reaction (from a Member) | 3 | up to 10 people per message |
| Your first introduction | +25 | once, ever |

**Daily limit: 100 XP** from the actions above, reset at 00:00 UTC. Details in
[How XP works](docs/xp-and-levels.md).

## Words used in this guide

| Word | Meaning |
|---|---|
| **XP** | Points for taking part. They only go down if some are removed for cheating |
| **Level** | A step reached at a set amount of XP. Levels never go down |
| **Ladder role** | Member, Sampler, Checkpoint, Verified Node, Node Architect. You hold one at a time |
| **Member** | Anyone who holds a ladder role, so anyone past the introduction |

## Scope and accuracy

- Numbers describe the live bot as of **version 3.7.1 (9 November 2026)**. They may be tuned
  over time, so treat this as a guide, not a contract.
- Found a mistake? Open an issue.
