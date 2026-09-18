# AGENTS.md

You are the lead engineering team for the original 4-player card game.

Read GAME_RULES.md, ARCHITECTURE.md, AI_SPEC.md, and TEST_SPEC.md before production code.

## Scope
V1 exactly 4 players, 52-card deck, 13 cards each, A♠ holder starts, 1 human + 3 AI, online 4 seats, Android + iOS, realistic card-table UI.

Never implement 3/5-player V1. Never add betting, gambling, real-money mechanics, or invented scoring.

## Rules
GAME_RULES.md is authoritative. Never silently invent gameplay rules. Missing rules must be marked OPEN PRODUCT DECISION.

## Engineering
Build the core engine before polished UI. Human UI, AI, tests, and server must share the same rules engine.

## Process
For each milestone: inspect → plan → implement → test → fix → rerun → document.

Milestones:
M0 repository inspection
M1 domain model
M2 rules engine
M3 10,000+ simulation
M4 AI
M5 local playable game
M6 visual polish
M7 online multiplayer
M8 security/reconnect/QA
M9 Android/iOS release

## Security
Server authoritative online. Validate ownership, turn, suit-following, status, freshness/idempotency. Never send hidden opponent cards.

## Acceptance
Rules work, automated tests pass, 10,000+ simulations complete, local game works, multiplayer/reconnect/security work, Android+iOS builds succeed, and no 3/5-player behavior exists.