# Instagram agent skill

Thirteen Claude skills for an Instagram account. Free, MIT, no signup, no API key, nothing to connect. Repo: https://github.com/Jakeschincariol/instagram-agent-skill. Made by Jake Schincariol. The same idea for LinkedIn is https://github.com/Jakeschincariol/linkedin-agent-skill.

Use this file when the work is writing or checking Instagram copy with this set. Open it from `C:\Users\ANISH\Documents\ai-playbook\LIBRARY.md` and use only the command the task needs. Reel tools marked as a content system stay in `C:\Users\ANISH\Documents\ai-playbook\library\content-creation-system.md`.

These skills write. They do not post. Nothing goes up until ANISH says yes. Automated posting, commenting, following, or DMing is outside this set. The one exception the repo names is keyword auto-replies in DMs, which Instagram supports after someone comments first. `/ig-dm` is where that line is. `/ig-viral` reads in the browser at human speed. It does not scrape, and it does not ask for a password.

Fill in `templates/voice.md` first. Copy it to `~/.claude/instagram/voice.md`, or have Claude write it from three of your own reels. Every skill reads that file.

Install by pasting the repo URL into Claude and asking it to install the skill, then confirm `/ig-reel` works. In Claude Code: clone the repo and copy `skills/ig-*` into `~/.claude/skills/`. As a plugin: `/plugin marketplace add Jakeschincariol/instagram-agent-skill`, then `/plugin install instagram-agent`. Pasting one `SKILL.md` into a chat runs that mode, and it drops the five Python tools.

| Command | Job |
| --- | --- |
| `/ig-reel` | One idea into a Reel. Three hooks from 26 formulas, scored, then the script, on-screen text, and a timed beat sheet. |
| `/ig-viral` | Find what is working in the niche. Rank each reel by how far it beat that account's own median. Name the formula. Write the swipe file. |
| `/ig-caption` | Write the caption and show the about 125 characters the feed shows before "... more". |
| `/ig-carousel` | Cover, slide copy, and the 1080x1350 files. |
| `/ig-story` | The day's story sequence, which sticker does which job, and a DM funnel that starts when they move first. |
| `/ig-profile` | Score the profile out of 100 on a 12-part rubric, then rewrite what lost points, worst first. |
| `/ig-plan` | The week: what to post, which format, when, and 10 accounts to engage with. |
| `/ig-human` | Strip em dashes, stock vocabulary, and invisible watermark characters. Score what is left on a five-check panel before you see it. |
| `/ig-comment` | Comments on other people's posts. Nine types, picked from the post. |
| `/ig-reply` | The thread under your own post. Sort into keyword, lead, substance, question, support, and noise, then write in that order. |
| `/ig-dm` | Keyword delivery, the first message, the collab pitch, and two follow-ups. |
| `/ig-repurpose` | One video, podcast, or newsletter into a week of reels and carousels that each stand alone. |
| `/ig-audit` | Post-mortem on what you already posted. Rank by outlier multiple. Sends per reach, not views. |

The five tools run locally, with no network and nothing uploaded:

- `skills/ig-reel/hookscore.py` ranks hook options. `beats.py` times the script before the shoot and flags a hook past three seconds, a beat long enough to leave, a run of lines with nothing concrete, and no loop back to the first line.
- `skills/ig-caption/caption.py` prints the feed window and lints the caption. The repo's hashtag cap is five per post. It says Instagram cut the old cap of thirty on 18 December 2025. If Instagram has moved since, Instagram is the number to use.
- `skills/ig-human/humanize.py` cleans. `detect.py` scores. Automatic passes: invisible characters, typography (em dash to comma, curly quotes to straight), and a lexicon of 154 stock phrases in `slop.json`. Sentence-shape problems are flagged for a rewrite, not auto-fixed.
- `skills/ig-viral/swipe.py` ranks on the multiple over each account's own median, not raw views.

The repo's own test of the hook scorer, on 74 YouTube Shorts hooks because Instagram view counts were not collected: it catches deliberately bad hooks, and it does not pick winners among a good creator's hits and misses. Use it to kill a weak hook before the take. Retention decides between two decent hooks. A draft that needs a number you have not given comes back with `{{your number}}`.
