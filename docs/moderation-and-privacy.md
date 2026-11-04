# Moderation and privacy

## Spam protection

Ashley watches for the patterns that hijacked or throwaway accounts use:

- Posts with several images and almost no text (the "image grid" scam style).
- The same message or attachment sent into several channels in a short time.
- Discord invite links from people who are not staff.
- Mass mentions and `@everyone` / `@here` attempts.

When something matches, the message is deleted, related copies are removed, and the author can be
**timed out for 24 hours**. A card is sent to the private moderator channel with **Ban** and
**Release** buttons. A person decides about bans, and a timeout can be lifted with one click if
Ashley got it wrong. **Ashley never bans on her own.**

Staff are exempt. Messages the filter removes earn no XP.

If you were caught by mistake, ask a moderator to release you and explain what you posted.

## Data Ashley keeps

Ashley keeps a record in a private database so XP, levels, leaderboards and moderation work:

| Data | Used for |
|---|---|
| Your Discord user ID and current/previous display names | Showing the leaderboard, helping staff identify accounts |
| Message log (IDs, channel, timestamps, text, attachment info, edits, deletes) | Catching up after downtime, spam checks, a server archive |
| Reactions on messages | XP for reactions and spam checks |
| An XP ledger (amount, reason, message, time) | Showing where every point came from, audits |
| Join and leave events | Server statistics |
| Spam actions | Reviewing and undoing moderator decisions |

What Ashley does **not** do: read direct messages, collect payment or personal details, or share the
database. The database is private to the server owner and is backed up nightly (the last 14 copies
are kept).

Requests to see or remove your data should go to the server owner.

## Automatic reports

- A **weekly** stats and leaderboard post in the public system-logs channel. The leaderboard names
  the top members by XP, so being active means appearing there.
- A **nightly** database backup (not visible to members).
- Moderator-only logs for joins, leaves, name changes, and errors.

## Staff tools

Moderators can adjust XP (with a written reason), start bonus events, review spam actions, switch
spam handling between "log only" and "enforce", and run reports. These tools are owner-only and
are not documented here.

See also: [FAQ](faq.md)
