# Games Project

Educational HTML games for K-1 students. Pure vanilla HTML/CSS/JS, no dependencies, no build step.

## Structure

- `index.html` — Game hub landing page with cards linking to all 7 games
- `addition-garden.html` — Addition problems (sums ≤10), grow flowers
- `blend-builder-adventure.html` — Consonant blends, drag letters to complete words
- `counting-rocket.html` — Count objects (1-10) to launch a rocket
- `learning-quest.html` — Mixed reading & math across 5 themed worlds
- `phonics-treasure-hunt.html` — Match pictures to word families
- `shape-detective.html` — Identify shapes in scenes
- `sight-word-safari.html` — Match high-frequency sight words to animal cards
- `math-word-problems.html` — **Bake Shop Bonanza**: 1st-grade math word problems (addition/subtraction/comparison within 20), open text input, bakery case fills with treats on correct answers

## Known Bugs

- **shape-detective.html**: References undefined `currentWorld` — should be `currentCase` (affects world icon on completion)
- **learning-quest.html** (~line 641): Wrong world icon may appear on completion modal due to progression tracking logic
- **sight-word-safari.html**: Cards can be clicked multiple times during the 500ms shake animation (race condition)

## Code Quality Notes

- All JS is inline — `celebrate()`, `updateStats()`, and completion modal logic are duplicated across every game file
- No localStorage — progress resets on every page load
- No ARIA labels or keyboard navigation
- Inconsistent scoring thresholds: Addition Garden uses 60% for stars, Sight Word Safari uses 90%
- Game lengths vary: 8–15 challenges depending on the game
- No shared CSS or JS files — each game is fully self-contained

## Conventions

- Responsive breakpoint at 600px
- Confetti celebrations: 30–50 particles
- Emoji-heavy design appropriate for target age group
- Each game has its own color gradient palette (no unified theme)
