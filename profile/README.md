# Prism

A plural system management app with zero-knowledge encrypted sync.

Prism helps plural systems track fronting, chat between members, log sleep, build habits, run polls, and keep shared notes — all encrypted end-to-end, synced across your devices. It's an independent project. No VC funding, no corporate parent, no investors to please. Just software made by people who actually need it.

## The repos

**[prism-app](https://github.com/prismplural/prism-app)** — the Flutter client for iOS, Android, macOS, and web. This is what you install. It handles the UI, local encrypted database, and all the features: members, fronting, chat, polls, habits, sleep, notes, groups, custom fields, Simply Plural import, PluralKit sync.

**[prism-sync](https://github.com/prismplural/prism-sync)** — the Rust sync engine and relay server. Field-level CRDTs with Hybrid Logical Clocks, end-to-end encryption with post-quantum hybrid signatures, and a self-hostable relay that only ever sees encrypted blobs. Used by the app via Dart FFI bindings, but it's designed as a standalone library — you can build other apps on it.

## Why it's built this way

**Your data lives on your devices.** Prism is local-first. The relay is a delivery mechanism for sync, not a home for your data. Plural system data is deeply personal — who's fronting, what members say to each other, sleep patterns, habits. It shouldn't live on someone else's infrastructure by default.

**Encryption isn't optional.** The local database is encrypted the moment you open the app. Sync data is end-to-end encrypted before it leaves your device. You can't turn it off. Security that's opt-in isn't security — it's a checkbox most people never find.

**No account required.** No email, no username, no identity. Sync uses a PIN. We don't know who you are unless you tell us.

**No clinical language by default.** The UI uses neutral terms like "members" and "system," and lets you rename even those. Not every system identifies with a clinical framework, and an app shouldn't impose one.

**No behavioral analytics.** No third-party SDKs, no ad networks, no per-screen engagement tracking. We are not interested in optimizing retention curves.

**Open source, end to end.** The app, the sync engine, and the relay server. Audit the code, verify the claims, or self-host the whole thing. "Trust us" is not a security model.

Prism is built by a plural system that actually uses it every day.

It started from lived experience. Other apps we tried seemed to assume one kind of user: someone with the time, energy, vision, memory, and dexterity to keep up with a dense interface every day. That leaves younger, older, or disabled system members behind, and it made it harder for us to build the habit of actually using them. So we made the app we wanted.

We use Claude extensively as a coding tool. The security architecture, design decisions, and the feel of the app are ours. The encryption is fully auditable and open source regardless of what tools wrote it.


## Links

- **Site** — [prismplural.com](https://prismplural.com)
- **Docs** — [prismplural.com/docs](https://prismplural.com/docs/)
- **How the encryption works** — [prismplural.com/encryption](https://prismplural.com/encryption/)
- **About** — [prismplural.com/about](https://prismplural.com/about/)
- **Beta access** — [get@prismplural.com](mailto:get@prismplural.com)
- **Contact** — [hello@prismplural.com](mailto:hello@prismplural.com)

If you find a security issue, please email us directly instead of opening a public issue.
