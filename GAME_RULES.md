# GAME_RULES.md — AUTHORITATIVE GAMEPLAY RULES

## Game
- V1 is exactly 4 active players.
- Standard 52-card deck.
- 13 cards per player.
- Objective: empty your hand.
- Zero cards means FINISHED.
- Finish order is final ranking.

## Opening
- The player holding A♠ starts.
- A♠ is not a permanent trump.
- A♠ is the opening card and establishes Spades as the required suit.
- Do not add artificial first-round dealing constraints.

## Required Suit
- First card of every round establishes the required suit.
- If a player has that suit, they MUST play it.
- If they have zero cards of that suit, they MAY play another suit.

## Successful Round
If all 4 active players follow suit:
- All four played cards are cleared permanently.
- Nobody picks them up.
- Highest-ranked required-suit card determines the next starter.
- If that player just reached zero cards, they are FINISHED and cannot start; compare required-suit cards of remaining active players and use the highest active player.

## Pickup / Interrupted Round
When a player has no required-suit card and legally plays another suit:
- The round ends immediately.
- Players after the interrupter do NOT play.
- Compare ONLY required-suit cards already played.
- Highest required-suit player picks ALL cards played, including the off-suit card.
- Off-suit card does not automatically win.
- Pickup player starts next round.

Example: P1 ♥7, P2 ♥K, P3 ♠A because P3 has no Heart, P4 does not play → P2 picks ♥7 + ♥K + ♠A and starts.

## Forbidden
No invented trump, numeric scoring, betting/real-money mechanics, seat-number pickup rules, automatic off-suit victory, 3-player V1, 5-player V1, hidden AI information, or client-authoritative results.