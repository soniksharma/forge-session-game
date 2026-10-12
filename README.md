# FORGE

**A logistics game prototype for exploring scoped, uninterrupted gameplay sessions.**

FORGE demonstrates a factory loop: mine ore, smelt plates, and trade inventory through an order-book-style market. A temporary, revocable session controls the gameplay loop so the player can experience the intended flow without repeatedly approving routine actions.

## Run the prototype

Open `index.html` in a modern browser. There is no build step or dependency installation.

## Prototype status

This is a front-end prototype backed by local browser state. It does not connect a wallet, produce cryptographic session keys, submit Solana transactions, use MagicBlock, settle a live order book, or persist game state on-chain. Session controls and market activity are simulated for demonstration.

## Product direction

The longer-term direction is a Solana game using scoped, expiring, revocable session authority for routine gameplay actions, with high-frequency simulation on an ephemeral execution environment and periodic settlement to Solana. Any real implementation must enforce instruction allowlists and ensure the session cannot withdraw or transfer wallet assets.

The broader product hypothesis is an SDK for games and consumer dApps that need lower-friction, user-controlled sessions. That need should be validated with developers before treating the SDK or business model as proven.

## Files

- `index.html` — interactive game and session UX prototype
- `SUBMISSION.md` — hackathon submission copy, demo walkthrough, and implementation roadmap

