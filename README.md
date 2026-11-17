# PSY170 — Industrial/Organizational Psychology

Class activities and personality surveys for PSY170 at UC Merced. Each one is a single
self-contained HTML file: no build step, no dependencies, and nothing collected — no accounts, no
backend, no analytics.

**Live site:** https://rossdavilla.github.io/PSY170/

## Surveys

Each is laid out for a fixed **720 × 450** Top Hat iframe and reflows down to phone width.

| Page | What it measures |
| --- | --- |
| [Achievement Motivation Scale](https://rossdavilla.github.io/PSY170/achievementmotivationscale.html) | McClelland's needs for achievement, power and affiliation |
| [Commitment to UC Merced](https://rossdavilla.github.io/PSY170/commitmentscale.html) | Meyer & Allen's affective, continuance and normative commitment |
| [Big Five](https://rossdavilla.github.io/PSY170/Big%20Five%20(Survey)/embed.html) | Twenty IPIP-NEO items, one per screen, scoring the five factors |
| [The Dark Triad](https://rossdavilla.github.io/PSY170/Dark%20Triad%20(Survey)/embed.html) | Machiavellianism, narcissism and psychopathy — Halloween-themed |
| [Emotional & Social Intelligence](https://rossdavilla.github.io/PSY170/Emotional%20and%20Social%20Intelligence%20(Survey)/EQSQ.html) | How well you read your own emotions against how well you read other people |
| [Plot Your Past Bosses](https://rossdavilla.github.io/PSY170/Leadership%20Grid%20Survey/) | Rate three real bosses on task and relationship behaviors, and see each on Blake and Mouton's Leadership Grid. Add `?grid` for the instructor view with the blank-grid downloads. |

```html
<iframe src="https://rossdavilla.github.io/PSY170/Big%20Five%20(Survey)/embed.html"
        width="720" height="450" style="border:0;max-width:100%"
        title="Big Five Personality Survey"></iframe>
```

## In-class games

| Page | What happens |
| --- | --- |
| [Subtext](https://rossdavilla.github.io/PSY170/nonverbal-behavior.html) | Partners pass one phone back and forth, delivering lines like "Good job." with only nonverbal cues to carry a secret meaning. `Nonverbal (Subtext Game)/Subtext.html` is the earlier version. |
| [Groupthink: Four Cases](https://rossdavilla.github.io/PSY170/Groupthink%20Examples/) | Each student is dealt one of four real cases — from a Soviet submarine's near-launch to the Mozart effect — then finds classmates holding a different one. |
| [The Heist](https://rossdavilla.github.io/PSY170/thiefgame.html) | Secretly tells each student whether to steal a prize and whether to lie about it, so the class can practice detecting deception. |

The Groupthink cases and the Leadership Grid keep answers in the browser tab's `sessionStorage`,
so an accidental refresh doesn't erase them and closing the tab clears them.

## Running it

Serve the folder and open any page — several activities load local images, so a server works
better than opening files directly:

```bash
python3 -m http.server 8000
```

Folder names contain spaces, so URLs need `%20`.
