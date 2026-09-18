# TEST_SPEC.md

## Deck
Test 52 unique cards, four suits, thirteen ranks per suit, four players with 13 cards, no duplicate or missing card.

## Opening
Test exactly one A♠, correct holder, A♠ holder starts, A♠ is opening card, Spades become required suit, and no artificial first-round constraint.

## Follow Suit
Player with required suit must follow; player without it may play another suit. Reject cards not in hand, finished players, and wrong-turn players.

## Successful Round
P1 ♥7, P2 ♥K, P3 ♥3, P4 ♥10 → success, all four cleared, P2 starts if active.

## Pickup
P1 ♥7, P2 ♥K, P3 ♠A → P3's off-suit play is legal only with no Heart; round ends; P4 gets no turn; P2 picks all three and starts.

## Off-Suit Ace
P1 ♥K, P2 ♥7, P3 ♠A → P1 picks, not P3.

## Finish
Zero cards = FINISHED; record finish position once; finished players never turn again; remaining players continue.

## Invariants
No duplicate/lost cards; current turn is active; off-suit acceptance means zero required-suit cards; interruption prevents later plays; successful 4-player round has four required-suit plays; pickup returns every played card exactly once.

## Simulation
At least 10,000 completed AI-vs-AI games before release candidate. Detect hangs, illegal moves, duplication/loss, impossible turns, finished-player turns, and serialization divergence.

## Multiplayer
Test simultaneous, duplicate, stale, invalid-card, wrong-turn, disconnect/reconnect, duplicate-seat, and forged-result attempts.