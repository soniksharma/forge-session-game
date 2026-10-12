# FORGE — submission draft

## One-line pitch

FORGE is a session-key gameplay layer that lets players run on-chain production loops without approving every move.

## Product description

On-chain games lose momentum when routine actions require a wallet approval each time. FORGE gives a player a scoped, revocable game session and uses a logistics factory to demonstrate the experience: mine ore, smelt plates, and trade inventory through a market. The session is restricted to game actions, expires, and cannot withdraw wallet funds. The long-term product is an integration SDK for games and other apps that need uninterrupted, user-controlled sessions.

## Demo walkthrough

1. Open the app and connect the demo wallet.
2. Grant the scoped session key. This starts the automated production line.
3. Mine ore or smelt manually; the UI records session-authorized actions without another wallet prompt.
4. Sell ore or plates through the order book and watch credits update.
5. Revoke the session and observe production stop. Permissions also expire after ten minutes.

## Current build and honest scope

The included `index.html` is a self-contained, interactive browser prototype. It demonstrates the intended permission and gameplay UX with local state. Wallet connection, signatures, session-key cryptography, an on-chain program, a live order book, and MagicBlock Ephemeral Rollup execution are **not implemented in this prototype**. Do not describe those integrations as already working in a submission or demo.

## Next technical milestone

Replace the demo wallet with a Solana wallet adapter; issue a temporary key stored client-side; enforce an explicit instruction allowlist and expiry on a Solana program; execute game state updates on a MagicBlock Ephemeral Rollup; periodically commit inventory and marketplace settlement to Solana. Keep assets and withdrawals outside the session's authority. Add an integration package only after the game loop validates the developer need.

## Initial customer and go-to-market

Start with Solana game studios and consumer dApps where repeated low-value actions create approval fatigue. Recruit a handful of teams to integrate the session flow into one existing action loop, measure completion rate and repeat usage, then package the proven wallet/session/permissions flow as an SDK. Potential revenue: usage-based or tiered developer plans, with an open-source client and paid hosted policy/relayer services.

## What to validate with users

- Do players abandon games because of repeated wallet prompts?
- Which actions should a session authorize, and what limits make players comfortable?
- Will game developers integrate a focused session SDK, or do they prefer wallet-native session features?

## Demo hosting

The prototype has no build step: open `index.html` in a modern browser, or publish the project directory with any static web host. For judging, record a short screen capture that includes grant, automatic production, a manual action, market sale, and revoke.
