# Fake Doubler — Examples

This file provides a few concrete examples illustrating how the **central card** works in common and edge cases.
Unless otherwise stated, examples assume the player is **not disabled**.

---

## Example 1 — High Card → Pair (Doubling)

Hand:
- A♠ Q♦ 9♣ 7♥ 4♠

Central card:
- K♦

Result:
- The player does not hold a King.
- The central card is doubled.
- Final hand: **Pair of Kings**

---

## Example 2 — High Card → Straight (Completion)

Hand:
- 7♠ 8♦ 9♣ J♥ Q♠

Central card:
- 10♦

Result:
- The player does not hold a Ten.
- The central card provides the missing rank.
- Final hand: **Straight (8–9–10–J–Q)**

---

## Example 3 — Straight Rank Improvement

Hand:
- 9♠ 10♦ J♣ Q♥ K♠

Central card:
- A♦

Result:
- The straight is already complete.
- The player does not hold an Ace.
- The central card improves the straight’s rank.
- Final hand: **Ace-high straight**

---

## Example 4 — Trips → Full House

Hand:
- Q♠ Q♦ Q♣ 9♥ 4♠

Central card:
- 8♦

Result:
- The player does not hold an Eight.
- The central card is doubled, forming a pair of Eights.
- Final hand: **Full House (Queens full of Eights)**

---

## Example 5 — Disabled Central Card

Hand:
- 10♠ 10♦ 8♣ 6♥ 4♠

Central card:
- 10♣

Result:
- The player holds the same rank as the central card.
- The central card is **disabled**.
- Final hand remains: **Pair of Tens**

---

## Example 6 — Flush Completion via Suit Change

Hand:
- A♠ Q♠ 9♠ 5♠ 2♦

Central card:
- K♦

Result:
- The player does not hold a King.
- The central card changes suit to ♠.
- Final hand: **Ace-high flush**

---

## Example 7 — What the Central Card Cannot Do (No Quads)

Hand:
- J♠ J♦ J♣ 7♥ 4♠

Central card:
- J♥

Result:
- The player holds the same rank as the central card.
- The central card is disabled.
- **Four of a kind cannot be created via the central card.**

---

## Design Reminder

The central card:
- accentuates existing strength
- never replaces it
- never acts as a wild card
- never multiplies hands beyond their category

