# PSY170 — Industrial/Organizational Psychology

Class activities and surveys for **PSY170** at UC Merced. Live at
<https://rossdavilla.github.io/PSY170/>.

## Layout

Each activity is either a single `.html` file at the root or its own folder. Everything is plain
HTML/CSS/JS inline in one page — no build step, no framework, no package manager.

| Path | Activity |
|---|---|
| `achievementmotivationscale.html` | Achievement Motivation Scale — McClelland's needs for achievement, power and affiliation |
| `commitmentscale.html` | Commitment to UC Merced — Meyer & Allen's affective / continuance / normative dimensions |
| `nonverbal-behavior.html` | **Subtext** — partners pass a phone back and forth, delivering lines like "Good job." with only nonverbal cues |
| `Nonverbal (Subtext Game)/Subtext.html` | The earlier version of Subtext, kept for reference (listed in the directory as a link on Subtext's card) |
| `thiefgame.html` | The Heist — secretly tells each student whether to steal and whether to lie (the PSYCH-C1000 repo has its own copy) |
| `Big Five (Survey)/embed.html` | Big Five — 20 IPIP-NEO items, one per screen |
| `Dark Triad (Survey)/embed.html` | The Dark Triad — Machiavellianism, narcissism, psychopathy (Halloween-themed) |
| `Emotional and Social Intelligence (Survey)/EQSQ.html` | Emotional & Social Intelligence — reading your own emotions vs. reading other people |
| `Leadership Grid Survey/index.html` | Plot Your Past Bosses — rate three real bosses, see them on Blake and Mouton's grid. `index.html?grid` is the instructor view with the blank-grid downloads |
| `Groupthink Examples/index.html` | Groupthink: Four Cases — each student gets one of four real cases, then finds classmates holding a different one |
| `Need for Cognition Scale/index.html` | Need for Cognition — Cacioppo & Petty's 6-item short form, scored low / moderate / high |

## Conventions

- **The surveys are 720 × 450 Top Hat embeds.** `achievementmotivationscale.html`,
  `commitmentscale.html`, both `embed.html` files, `EQSQ.html`,
  `Leadership Grid Survey/index.html` and `Need for Cognition Scale/index.html` are each laid
  out to fit that frame exactly and must not scroll at that size. The two phone-passing games
  (`nonverbal-behavior.html`, the Groupthink cases) are not frame-constrained. Folder names contain spaces, so URLs need `%20`.
- **Nothing is collected.** These run in class on students' own phones; there is no backend, no
  analytics, and no account. The Groupthink and Leadership Grid activities keep answers in the
  tab's `sessionStorage` only, so a refresh does not wipe them and closing the tab clears them.
  Keep that pattern — do not add persistence or a server.
- Several folders carry their own notes next to the activity: `Groupthink Examples/cases.md` and
  `Image Generation Instructions.docx`, `Leadership Grid Survey/README.md`. Read those before
  changing that activity.
- Illustrations live in the activity's own `img/` folder, named after the case or trait they
  belong to (`case1-arkhipov.jpg`, `narcissism.jpg`).

## Publishing

GitHub Pages serves `main` from the repository root, so a push to `main` is the deploy.

Note: `Leadership Grid Survey/README.md` says Netlify redeploys the folder. That is stale — this
repo publishes through GitHub Pages like the others.

After adding a new activity, add it to `data/sites.json` in the
[`rossdavilla.github.io`](https://github.com/rossdavilla/rossdavilla.github.io) repo with the
`PSY170` tag. A 720 × 450 embed of an activity already listed goes in that app's `links`, not a
card of its own.
