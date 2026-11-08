SolWall — A Message Wall That Lives on Solana
A public message wall where every message is a real transaction on the Solana blockchain (devnet).
There is no server and no database — the chain itself is the wall.

Built during the MLH Solana Hackathon (Nov 6–8, 2026).

What it does
Create a demo wallet in the browser — a throwaway Solana keypair generated locally and kept in localStorage. No signup, no extension needed.
Airdrop 1 devnet SOL — free test tokens from the Solana devnet faucet, so anyone can try it with zero real funds.
Post a message on-chain — the message is sent as a transaction to the Solana Memo Program (MemoSq4gqABAXKb96qnH8TysNcWxMyWCqXgDLGmfcHr) with a SOLWALL| tag, signed by the demo wallet.
Read the wall back from the chain — the app scans recent Memo Program transactions, filters for SolWall messages, and renders them, each linked to its transaction on Solana Explorer.
Why Solana
Cheap enough for a message wall: a memo transaction costs a fraction of a cent in fees, so "one message = one transaction" is actually viable.
Fast confirmation: posts confirm in about a second, so the wall feels like a normal web app.
Permanent & public: messages can't be edited or deleted by anyone — the wall is censorship-resistant by construction.
Run it
It's a single static file — no build step.

Live demo: open the GitHub Pages link for this repo.
Locally: just open index.html in a browser (internet needed for the Web3.js CDN and the devnet RPC).
Tech
Solana Web3.js (@solana/web3.js via CDN)
Solana Memo Program on devnet
Vanilla HTML / CSS / JS — one file, zero dependencies to install
Notes & limits
Devnet only: the demo wallet and its SOL have no real-world value.
The wall view scans the most recent Memo Program transactions, so very old SolWall posts eventually rotate out of the visible list (they remain on-chain forever).
Devnet faucet is occasionally rate-limited; if an airdrop fails, wait a minute and retry.
