# Aniimo Element Counter

A mobile-first web tool for checking elemental matchups in **Aniimo**. Pick one or two elements to see what they're weak to, what they resist, and what their skills hit hard.

**Live site:** [https://spidey337.github.io/aniimo-elem-counter/](https://spidey337.github.io/aniimo-elem-counter/)

## Features

- **Defending view.** Shows which elements hit a single- or dual-type Aniimo hard and which it resists, with dual-type multipliers (×2.56, ×1.6, ×0.625, ×0.39).
- **Attacking view.** Shows what each element's skills are strong against or resisted by, plus combined coverage when two elements are picked.
- **Full type chart.** A 9×9 attacker-vs-defender grid that highlights your picks.
- **Shareable links.** The URL saves your selection, e.g. `#Water+Ice`.
- **Light and dark mode.** Follows your device setting.
- **One file, no build step.** It's all in `index.html`.

## How damage works

| Matchup | Multiplier |
| --- | --- |
| Strong against | ×1.6 |
| Neutral | ×1 |
| Resisted | ×0.625 |

- Every element except Dark resists its own type.
- There are no immunities.
- For dual types, both multipliers are multiplied together. Two weaknesses give ×2.56, and a weakness paired with a resistance cancels out to ×1.
- A skill's own element sets the damage, not the Aniimo's type.

## Element chart

| Element | Strong against | Resisted by |
| --- | --- | --- |
| Fire | Grass, Ice | Earth, Fire, Light, Water |
| Water | Earth, Fire | Grass, Ice, Light, Water |
| Grass | Earth, Water | Fire, Grass, Light |
| Ice | Lightning, Water | Earth, Fire, Ice |
| Lightning | Water, Wind | Earth, Ice, Lightning |
| Earth | Fire, Ice | Dark, Earth, Grass, Water |
| Wind | Dark, Grass | Lightning, Wind |
| Light | Dark, Wind | Light, Lightning |
| Dark | Grass, Light, Lightning | Water, Wind |

## Run it locally

Download `index.html` and open it in any browser. The Baloo 2 font loads from Google Fonts; offline, it falls back to your system font.

## Data sources

The chart is community-sourced and matches the in-game Counters panel as reported by these guides:

- [Mobalytics – Aniimo Elemental Type Chart](https://mobalytics.gg/gamebase/guides/aniimo-elemental-type-damage-explained-chart)
- [GameTrek – List of All 9 Elements](https://gmtreks.com/aniimo/page/01M2J076DJWQE9F8KWVWFA74D0)
- [AllThings.How – Aniimo Type Chart](https://allthings.how/?p=184892)

If a matchup looks off, check the in-game Counters panel and open an issue.

## Disclaimer

This is an unofficial fan tool, not affiliated with or endorsed by Pawprint Studio. Aniimo is a trademark of its respective owner. The element icons are original artwork made for this project.
