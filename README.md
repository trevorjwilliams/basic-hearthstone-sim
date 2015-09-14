# basic-hearthstone-sim
Code to simulate a simplified version of Hearthstone in order to answer basic questions about optimal mana distribution and the like.

# Design Overview

## Constraints

- 40 cards
- 1- 10 mana
- 30 starting health

# Data Modeling

## Full model

- Card
- Cost
  - Stats
  - Specials
- Deck
  - 40x Cards
- Library (Deck in game)
  - Ordered Cards
- Hand
  - Ordered? Cards
- Side
  - Ordered? Minions
  - Ordered? Traps
- Minion
  - Card
  - Stats
  - Modifiers
- Battlefield
  - 2x Sides
- Player
  - Life (integer)
  - Hand
  - Library
- Game
  - 2x Players

## Simplified model

- Deck
  - Dictionary of mana cost to card count
- Hand/Library
  - Ordered list of mana costs.
- Card
  - Cost
- Tempo
  - Sum of mana cost of cards played
- Battlefield
  - Difference in tempos
- Life decreases by battlefield value / round