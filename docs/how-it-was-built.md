[🏠 Home](../README.md) · [Getting in](introduction.md) · [XP](xp-and-levels.md) · [Levels & roles](levels-and-roles.md) · [/rank](rank-command.md) · [Spam](spam-protection.md) · [Weekly report](weekly-report.md) · [Supporters](supporters.md) · [How it was built](how-it-was-built.md) · [FAQ](faq.md)

# How Ashley was built

Ashley was built by **one developer**, the creator of The 3-Minute Node Vault, working with an
**AI coding agent** (Claude Code). The developer set the goals, made every decision and tested every
release; the agent wrote the code, the tests and the documentation under the developer's rules.

## The problem

- The server had **thousands of members, but most had never posted** a single message.
- Scam accounts kept posting the same crypto-casino screenshots into several channels.
- The old bot was a single 1,600-line notebook export, hard to change safely.

## The answer, in three ideas

1. **A front door.** Everyone can read, but posting starts with one real introduction. It's a tiny
   step that turns a silent visitor into someone who has said something
   ([Getting in](introduction.md)).
2. **A ladder worth climbing.** One XP system for everyone, a daily limit so presence beats
   grinding, and roles that open real things: workflow downloads, advanced workflows, a members-only
   lab ([Levels and roles](levels-and-roles.md)).
3. **Spam handled in seconds, judged by a person.** The bot removes, a person reviews
   ([Spam protection](spam-protection.md)).

## Timeline

| Date (2026) | Milestone |
|---|---|
| 26 Oct | Review of the old bot. Design proposal written |
| 2 Nov | **v2.0**: full rewrite, rolled out in stages (silent first, then roles, then public posts). The introduction gate goes live |
| 8 Nov | **v3.0**: one ladder for everyone, daily XP limit, newcomer return rate in the weekly report |
| 9 Nov | Spam rules reviewed, Ko-fi supporters, Node Architect, monthly donor posts. **v3.7.1** |

**26 releases in 8 days**, about **4,500 lines** of Python, **57 automated tests**.

## How it's built

```
message posted
   │
   ├─▶ spam check     spam? ── yes ─▶ remove (no XP)
   │
   └─▶ clean ─┬─▶ XP            award, daily limit, level, role
              └─▶ introduction  first real intro? → ✅ + Member
```

- **Decisions are plain, tested functions.** "Is this spam?", "how much XP?", "which role?" are
  answered by small pieces of code with no Discord connection, so every rule has automated tests.
  The Discord side only passes events in and applies the answer.
- **Every XP point has a reason.** Scores are never edited by hand, so any of them can be rebuilt
  and explained.
- **Every number is a setting.** XP amounts, cooldowns, levels and texts can be tuned without
  touching code.
- **Nothing is lost on a restart.** Missed messages are caught up, buttons keep working, roles are
  re-checked.
- **Small and boring stack:** Python 3.13, discord.py, SQLite. No GPU, no extra services.

## How it was run: directing an AI agent

The agent did the typing. The developer did the directing, with rules the agent had to follow:

- **Decisions in writing.** Every design choice is recorded with the developer's own words and the
  date.
- **Every prompt is kept.** Each request to the agent is logged word for word with a short summary
  of the answer (130 so far), because chats get deleted and decisions shouldn't.
- **Hard limits.** The agent never runs the live bot, never touches the old bot's files, never
  handles secrets, and never ships a moderation action that can't be undone.
- **Same routine for every release:** automated checks and tests → version number → changelog →
  a session note (goal, decisions, what was *not* verified) → deployed and tested live.
- **Test before trusting.** Every new behaviour is tried quietly before it acts on anyone.

## Community management choices

- **No favourites.** Roles come from taking part or from supporting the channel, nothing else.
- **No public shaming.** Spam notices don't ping, reports show names without pings, and every
  removal is reviewed by a person.
- **Measure what matters.** The weekly report tracks whether newcomers come back for a second
  message in their first week, not only how many joined.
- **Credit supporters, respectfully.** Monthly thank-you posts with shortened names.

---

[🏠 Home](../README.md) · [← Supporters](supporters.md) · Next: [FAQ →](faq.md)
