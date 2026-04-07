# 🛡️ ProveLab

**Cryptographic proof for any web data. Screenshots can be faked. Proofs can't.**

<!-- TODO: Replace with actual demo GIF -->
<!-- ![ProveLab Demo](assets/demo.gif) -->

<p align="center">
  <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-blue?style=flat-square" alt="Platforms">
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/built%20with-Rust%20%2B%20React-orange?style=flat-square" alt="Built with">
</p>

---

ProveLab generates **tamper-proof cryptographic certificates** from live web data using [TLS Notary](https://tlsnotary.org). Instead of screenshotting a dashboard and hoping someone believes you, ProveLab lets you **prove it mathematically**.

Your credentials never leave your machine. No server sees your login. Just math.

---

## ⚡ Download

| Platform | Download | Notes |
|----------|----------|-------|
| 🪟 **Windows** | [ProveLab-Setup.exe](https://github.com/alphapulsx-jpg/ProveLab-io/releases/latest/download/ProveLab_2.0.0_x64-setup.exe) | Recommended |
| 🪟 **Windows** | [ProveLab.msi](https://github.com/alphapulsx-jpg/ProveLab-io/releases/latest/download/ProveLab_2.0.0_x64_en-US.msi) | Alternative installer |
| 🍎 **macOS (Apple Silicon)** | [ProveLab.dmg](https://github.com/alphapulsx-jpg/ProveLab-io/releases/latest/download/ProveLab_2.0.0_aarch64.dmg) | M1 / M2 / M3 / M4 |
| 🐧 **Linux (Ubuntu/Debian)** | [ProveLab.deb](https://github.com/alphapulsx-jpg/ProveLab-io/releases/latest/download/ProveLab_2.0.0_amd64.deb) | `sudo dpkg -i` |
| 🐧 **Linux (Universal)** | [ProveLab.AppImage](https://github.com/alphapulsx-jpg/ProveLab-io/releases/latest/download/ProveLab_2.0.0_amd64.AppImage) | Any distro |
| 🐧 **Linux (Fedora/RHEL)** | [ProveLab.rpm](https://github.com/alphapulsx-jpg/ProveLab-io/releases/latest/download/ProveLab-2.0.0-1.x86_64.rpm) | `sudo dnf install` |

---

## 🤔 Why?

Anyone can fake a screenshot in 30 seconds. That's a problem when:

- A brand wants to **verify your follower count** before paying you $10K
- A VC asks you to **prove your revenue numbers** during due diligence
- Your client wants **proof your ad campaign actually delivered results**
- An auditor needs to **verify financial statements aren't fabricated**

ProveLab makes the question *"Can you prove it?"* trivially easy to answer.

---

## 🎯 What You Can Prove

### Financial & Business
| Use Case | What You Prove |
|----------|---------------|
| **Bank Statements** | Account balances, transaction history from your bank's dashboard |
| **Trading P&L** | Profit/loss from brokerage accounts (Robinhood, Interactive Brokers, etc.) |
| **Portfolio Returns** | Investment performance from any portfolio tracker |
| **Revenue Reports** | SaaS dashboards, Stripe, payment processor data |
| **Tax Returns** | Filed tax documents from government portals |
| **Proof of Funds** | Bank balance verification for loans, rentals, immigration |
| **Net Worth Statements** | Aggregated financial position from wealth platforms |
| **Asset Valuations** | Property values, investment holdings, appraisals |

### Creator & Social Media
| Use Case | What You Prove |
|----------|---------------|
| **Follower Counts** | Real follower/subscriber numbers from any platform |
| **Subscriber Stats** | YouTube, Substack, Patreon subscriber verification |
| **Engagement Rates** | Likes, comments, shares, watch time from analytics dashboards |
| **App Downloads** | Download counts from App Store Connect, Google Play Console |
| **Ad Spend Verification** | Actual ad spend and ROAS from Meta, Google, TikTok ads |
| **Conversion Rates** | Funnel metrics from analytics platforms |
| **Referral Tracking** | Affiliate and referral program performance |
| **User Metrics** | DAU, MAU, retention from any analytics tool |

### Identity & Credentials
| Use Case | What You Prove |
|----------|---------------|
| **KYC Verification** | Identity documents and verification status |
| **Academic Transcripts** | Grades, degrees, certifications from university portals |
| **Employment Records** | Employment history, salary from HR platforms |
| **Certification Status** | Professional certifications and licenses |
| **Background Checks** | Criminal record checks, reference verifications |
| **Identity Attestation** | Government ID verification from official portals |
| **Licensing Proof** | Professional, business, or driver's license verification |
| **Credit Scores** | Credit reports from bureaus |

### Compliance & Legal
| Use Case | What You Prove |
|----------|---------------|
| **Audit Trails** | System logs, access records, change history |
| **Contract Terms** | Agreement terms from e-signature platforms |
| **Insurance Claims** | Policy details, claim status from insurer dashboards |
| **Regulatory Submissions** | Filed regulatory documents and confirmations |
| **Property Ownership** | Title records, deeds from government registries |
| **SLA Compliance** | Uptime records, service level metrics |
| **ESG Compliance** | Environmental, social, governance reporting data |
| **Supply Chain Verification** | Origin, certification, chain of custody data |
| **Compliance Audits** | Audit results and findings from compliance platforms |
| **Chain of Custody** | Evidence handling records, transfer documentation |

### Technical & Operations
| Use Case | What You Prove |
|----------|---------------|
| **API Usage Stats** | API call volumes, rate limits from developer portals |
| **Server Uptime** | Uptime records from monitoring dashboards |
| **Sales Figures** | CRM data, pipeline metrics from Salesforce, HubSpot |
| **Inventory Audits** | Stock levels, warehouse data from inventory systems |
| **Carbon Credits** | Carbon offset purchases and retirement records |
| **Patent Filings** | Patent application status from USPTO/WIPO portals |
| **Voting Records** | Shareholder voting records, governance participation |
| **Board Resolutions** | Corporate governance documents and decisions |

> **If it's on a web page, you can prove it.**

---

## 🔬 How It Works

```
┌──────────┐     ┌──────────────┐     ┌──────────┐
│  You +   │────▶│  TLS Notary  │────▶│  Tamper-  │
│ ProveLab │     │  Protocol    │     │  Proof    │
│          │     │  (MPC-TLS)   │     │  Cert     │
└──────────┘     └──────────────┘     └──────────┘
     │                  │                    │
  Your data       Neutral witness      Anyone can
  stays private   co-signs the TLS     verify this
                  session              certificate
```

1. **You browse normally** — ProveLab connects to the website through a standard TLS session
2. **A neutral notary co-signs** — Using multi-party computation, a notary server witnesses the TLS session *without ever seeing your data*
3. **You select what to reveal** — Choose exactly which fields to include in the proof (selective disclosure)
4. **Certificate generated** — A cryptographic proof that anyone can independently verify

**Zero trust required.** The notary never sees your credentials or your data. The proof is mathematically verifiable by anyone, anywhere.

---

## ✅ Verify a Proof

Anyone can verify a ProveLab proof — no account, no app install needed.

**[→ Open the Online Verifier](https://alphapulsx-jpg.github.io/provelab/verify/)**

Just drag and drop a `.json` proof file. Verification runs entirely in your browser — no data is sent anywhere.

---

## 🆚 Why Not Just Screenshot?

| | Screenshot | ProveLab |
|---|---|---|
| **Can be faked?** | ✅ Yes, in 30 seconds | ❌ Cryptographically impossible |
| **Verifiable?** | ❌ No way to verify | ✅ Anyone can verify independently |
| **Timestamp proof?** | ❌ Can be edited | ✅ Cryptographic timestamp |
| **Data integrity?** | ❌ Pixels can be changed | ✅ Hash-locked to source |
| **Privacy?** | ❌ Shows everything | ✅ Selective disclosure |
| **Legal weight?** | ⚠️ Weak, easily challenged | ✅ Mathematically verifiable |

---

## 🏗️ Architecture

| Component | Technology |
|-----------|-----------|
| **Desktop App** | [Tauri 2.x](https://v2.tauri.app/) — lightweight, cross-platform |
| **Frontend** | React 18 + TypeScript + Tailwind CSS |
| **Proof Engine** | Rust + [TLS Notary](https://tlsnotary.org/) MPC-TLS |
| **Signatures** | Ed25519 + TLS Notary attestations |
| **Storage** | SQLite (local — your proofs never leave your machine) |
| **Bundle Size** | ~15MB installed |

---

## 🗺️ Roadmap

- [x] Desktop app (Windows, macOS, Linux)
- [x] Ed25519 cryptographic proofs
- [x] Twitter/X profile verification
- [x] GitHub data verification
- [x] Generic URL proof generation
- [x] Proof export & independent verification
- [ ] MPC-TLS with live notary server
- [ ] Browser extension (one-click proof from any page)
- [ ] Mobile app
- [ ] API for programmatic proof generation
- [ ] Proof sharing & public verification page

---

## 🔒 Security & Privacy

- **Your credentials never leave your machine** — ProveLab runs locally
- **No server sees your login data** — the TLS Notary protocol ensures privacy through multi-party computation
- **Selective disclosure** — you choose exactly which data fields to include in a proof
- **Open verification** — anyone can verify a proof without contacting ProveLab
- **No telemetry** — the app doesn't phone home

---

## 📄 License

[MIT](LICENSE)

---

<p align="center">
  <b>If ProveLab is useful to you, a ⭐ helps others find it.</b>
</p>
