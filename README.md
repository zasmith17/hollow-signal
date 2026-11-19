# Hollow Signal

**A community-owned phone app for life underground.** Built for Patriot HackFest Fall 2026 ("Life underground").

**Live demo:** https://YOUR-USERNAME.github.io/hollow-signal/

## The problem

In the Hollow, the deep levels get hit first by blackouts, heat, bad water and flooding, usually with no warning. The Directorate controls the network and the official numbers, and it can shut both off.

## The solution

Hollow Signal runs on a mesh of phones and repeaters, so it keeps working when the Directorate's network is down. Every message is digitally signed, chats are end-to-end encrypted, and the app covers all 15 problems in the brief:

| Problems | Where in the app |
|---|---|
| #1, #3, #4, #5: blackouts, heat, bad water, flooding | **Sensors** predict when each one will hit danger and warn you ahead of time. **Shelters** run on their own reserved power. |
| #2: fair sharing | **Food & Water** (rations by level, donation banks) and **Power** (share charge with the levels running lowest) |
| #6: finding space | **Explore**: volunteer teams map new areas, which can become overflow shelters |
| #7: network shutdowns | **Network**: mesh routing, offline device certificates, traffic priority tiers. **Chat** is encrypted. |
| #8: families | **Family**: check-ins and detailed help requests. **Map**: locations estimated from mesh signal strength. |
| #9: real outbreak numbers | **Medical → Report symptoms** and isolation shelters with separate air |
| #10: medical help | **Medical → Get help**: triage, nearest free medic, supply caches |
| #11: mental health | **Wellbeing**: mood check-ins with charts, counseling appointments, anonymous support chat |
| #12: neighborhood food | **Food & Water → Food**: growers list crops, neighbors request food |
| #13, #14, #15: the surface | **Surface**: air, temperature and UV probes; scouting missions with safety checklists; move-up requests with volunteer helpers |

Also: a **Volunteer** board that assigns tasks by how critical they are, and **Settings** where you choose which notifications can interrupt you. Life-safety alerts are always on.

## Security, for real

- **Signed messages (ECDSA P-256):** every device has a key pair. A "Hollow Council" key certifies each device, so any phone can verify a message offline. Fakes and stolen (revoked) phones are blocked.
- **Encrypted chat (AES-256-GCM, ECDH):** "Show what the Directorate sees" displays the real ciphertext.
- **Tamper-evident water ledger (SHA-256 hash chain):** an edited record is caught right away and restored from mesh copies.

All of this cryptography runs for real in the browser using the Web Crypto API.

## How to run it

Open `index.html` in any modern browser. There's nothing to install. The side panel has demo controls (power failure, Directorate attacks) and a short "Try this" tour.

## Notes

- All data is simulated for the demo. 1 second = 1 minute in the Hollow.
- Built from scratch during the event (Nov 14–20, 2026) as a single HTML file with plain JavaScript and no libraries.
- Built with help from Claude, an AI assistant, as allowed by the event rules.
