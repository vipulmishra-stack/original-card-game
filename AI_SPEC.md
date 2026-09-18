# AI_SPEC.md

## Objective
Computer opponents must play exactly the same game humans play.

## Non-negotiable
AI uses the same legal-move validator and round-resolution engine as humans. AI has no hidden information.

## Allowed
Own hand, required suit, current-round public cards, public history, visible card counts, active/finished players, own finish risk, previous public actions.

## Forbidden
Opponent hidden hands, hidden deck order, server random seed, future game state.

## Difficulty
Easy: legal play and simple hand-emptying.
Medium: suit management, card choice, pickup risk, finish status.
Hard: public card tracking, probability inference, finish-risk management.

Difficulty may change strategy, never legality.

Support deterministic seeds and AI-vs-AI simulation.