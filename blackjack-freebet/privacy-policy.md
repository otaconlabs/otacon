# Freebet Blackjack Privacy Policy

**Last updated:** June 9, 2026

Freebet Blackjack is a **play-money** Discord Activity created and maintained by **zedvawn**.
This Privacy Policy explains what data is stored, why, for how long, and how you can erase it.
By using Freebet Blackjack, you consent to the collection and use of information as described here.

---

## 1. Information We Collect

When you launch the Activity, we store, per user:

- **Identity from Discord:** your Discord user ID, username, and avatar hash. We never receive your password; the Discord OAuth flow returns only an access token, which is used once to read your public profile.
- **Game state:** your play-money chip balance and a rotatable provably-fair "client seed".
- **Bankroll ledger:** an append-only record of every chip movement (bet, payout, refund, top-up) with running balances — kept for integrity and dispute resolution.
- **Table and seat state:** which table and seat you occupy while playing.
- **Provably-fair audit log:** the seeds of retired shoes, so shuffles can be independently verified. Table-owned shoe reveals are not tied to a single user.

We do **not** store real-world identity, payment information (there are no payments), message content, or anything from your Discord account beyond the public profile fields above.

---

## 2. How We Use the Data

Collected data is used solely to run the game:

- Authenticating your session
- Persisting your play-money balance across sessions
- Seating you at multiplayer tables
- Providing provable fairness and an auditable chip ledger
- Monitoring performance and preventing abuse

---

## 3. Legal Basis and Sharing

Processing is necessary to provide the service you request by launching the Activity.
Your data is **never sold** and is **not shared** with third parties for advertising.
Data is stored in a private PostgreSQL database; our infrastructure providers (hosting and managed database services) process it on our behalf only as needed to operate the service.

---

## 4. Data Retention

- Data persists while your account is active.
- Idle, empty tables are cleaned up automatically.
- You may delete all of your data at any time (see Section 5).
- Operational backups are encrypted and age out on a fixed schedule.

---

## 5. Your Rights — Deleting Your Data

You can **permanently erase all of your data** from inside the app:

> **Privacy & data → Delete my data** (the gear/settings control at a table, or the "Privacy" link on the start screen) → confirm.

This deletes your user record and **cascades** to your rounds, seats, bankroll ledger, and per-user shuffle audit rows, then ends your session.
The action is immediate and irreversible. Residual copies may persist in encrypted backups until they age out per the retention schedule.

You may also request deletion manually by contacting the developer (see Section 8) with your Discord User ID.

---

## 6. Children

Freebet Blackjack is intended for users **18 years of age or older** and is play-money only.
We do not knowingly collect data from anyone under 18.

---

## 7. Third-Party Services

Freebet Blackjack operates within the Discord platform and does not integrate external analytics or advertising services.
Discord itself may collect additional data under its own [Privacy Policy](https://discord.com/privacy).

---

## 8. Contact

For privacy questions or data requests:

- **Developer:** zedvawn
- **GitHub:** [otaconlabs/otacon](https://github.com/otaconlabs/otacon/issues)

---

## 9. Changes to This Policy

This policy may be updated from time to time.
Material changes will be reflected here with a new "Last updated" date.
