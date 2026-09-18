# ARCHITECTURE.md

## Principles
Build a real Android + iOS application, not a mockup. Keep the rules engine independent from UI, AI, and networking.

## Core
- One authoritative domain/rules engine.
- Human UI, AI, tests, and server use the same rules logic.
- Explicit state transitions.
- Deterministic test states.
- Serialization/replay support.

## Domain
Card, Suit, Rank, Deck, Player, Game, Round, PlayedCard, status, commands/events as appropriate.

## Engine owns
Deal, A♠ opening, required suit, legal moves, successful rounds, pickup rounds, starter selection, finish order, completion, invariants.

Do not duplicate business rules in UI, controllers, AI, or network handlers.

## Online
Server is authoritative. Validate every command. Support rooms, four seats, real-time updates, reconnect, timeout handling, duplicate/stale command protection.

Never send hidden opponent cards to clients.

## UI
Premium realistic card-table experience with four player positions, own hand, opponent card backs/counts, required suit, turn indicator, pickup/success animations, and finish state.

## Build order
Engine → tests → simulation → AI → local game → UI polish → multiplayer → security/reconnect → mobile release.

Choose and document a maintainable cross-platform technology after inspecting the repository.