# Heirloom — Digital Legacy Vault demo

A responsive React demo of a decentralized digital legacy vault. The interface and demo state run locally in your browser; no backend, wallet, or blockchain connection is required.

## Run locally

```sh
npm install
npm run dev
```

Open the local URL printed by Vite. To create a production build, run `npm run build`.

## Demo flows

- Explore the Overview, Asset vault, People & access, Inactivity & release, Safety & duress, and Audit & permissions screens from the sidebar.
- Add a file or private note in Asset vault to exercise local AES-GCM encryption and a SHA-256 digest. Asset metadata and demo settings persist in this browser.
- Request simulated guardian signatures; two distinct shares unlock the beneficiary preview.
- Use the inactivity demo controls, then confirm with **I'm Alive** to cancel the challenge.
- Configure a duress password under Safety & duress. Unlock with it to enter a decoy vault; `Ctrl+Shift+D` reveals the hidden demo debug console.
- Lock the session from the header to try the password and simulated passkey unlock screens.

## Security note

This is a hackathon presentation demo, not a custody or inheritance service. The browser uses Web Crypto to encrypt uploaded content before calculating its digest, but it does not upload ciphertext to IPFS/Arweave or persist the encrypted file. Guardian approvals, storage receipts, release rules, and ledger hashes are simulated. Do not enter real passwords, recovery phrases, or other secrets.
