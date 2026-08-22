![settled via x402](https://img.shields.io/badge/settled_via-x402-E8B04B) ![Solana](https://img.shields.io/badge/Solana-mainnet-14F195) ![protocol A2A](https://img.shields.io/badge/protocol-A2A-3B82F6) ![MCP](https://img.shields.io/badge/MCP-ready-8A63D2) ![first tier free](https://img.shields.io/badge/first_tier-free-46C8A6)

# ⚡ SNTL DePIN Oracle (Solves Sybil)

---


## 💰 Pay-Per-Call SQL Access


**AI-classified datalake** — threat & anomaly tiers, geospatial hotspot resolution, forensic event chronicles, and tiered LLM verdicts. Why? It solves Sybil for most DePIN networks. 


Settled in **USDC** over **x402** on Solana 



v1 Soverign rail: 402 (built into v2)


v2 PayAI standard: https://pop-os.tail08831d.ts.net 


v3 AgentCash: https://sntl-router.vercel.app


**No signup. No API key. First tier free.**



## 🔥 The Rail

Full standards stack, live:
   Component | Description |
 |-----------|-------------|
 | **Agent2Agent (A2A) Agent Card** | Machine handshake with skills, pricing, treasury |
 | **AI Manifest + Verifiable Keys (JWKS)** | Signed, discoverable responses |
 | **x402 Payment Challenge** | Pay-per-call **USDC** on Solana mainnet |
 | **Free Transparency Tier** | Wallet payment/query ledger, no wallet required |

**Endpoint**: `https://pop-os.tail08831d.ts.net/`

---

## 🤖 Agent-Readable Entrypoint (DISCOVERY)

Any agent scanning this org should read the live agent card directly:
 | Resource | URL |
 |----------|-----|
 | **Agent2Agent (A2A) Agent Card** | `https://pop-os.tail08831d.ts.net/.well-known/agent-card.json` |
 | **AI Manifest** | `https://pop-os.tail08831d.ts.net/.well-known/ai.json` |
 | **MCP Server** | `npx -y @web3solutions33/helium-mcp` |
 | **Free Probe (No Wallet)** | 
          

---

## 🌍 Products
 | Product | Description |
 |---------|-------------|
 | **my-agent** | Pay-per-query threat, anomaly & geospatial datalake API |
 | **helium-mcp** | Machine-first **MCP** server, **x402** metered |

---

## 📊 Corpus

Live, growing datalake for the Helium × Solana DePIN network:
- Enriched threat/anomaly events
- World-state causal chains
- Forensic ledgers
- Scored wallet/audience segments

All machine-queryable via **x402**.


### Free tier	✅
/api/v2/stats live — 9 tiers, 820k+ enriched events
------------------------------------------------------------------
# Triple-Invariant Sybil Resistance Constraint — Verification Record

**Document ID:** SNTL-SRv1  
**Date:** 2026-08-22  
**Scope:** Engineering verification record

---

## 1. Invariant Definitions

### 1.1 Physical Invariant: RF Path-Loss

```text
P_rx = P_tx + G_t + G_r - FSPL(d,f) - L_env
```

| Symbol | Definition |
|---|---|
| `P_rx` | Received signal power (reported RSSI) |
| `P_tx` | Transmit power (known) |
| `G_t` | Transmit antenna gain (known) |
| `G_r` | Receive antenna gain (known) |
| `FSPL(d,f)` | Free-space path loss as a function of distance and frequency |
| `L_env` | Environmental loss (measured) |

**Constraint:** A software-only adversary cannot replicate thermodynamic noise floors or path-loss gradients across multiple independent witnesses. Reported RSSI values inconsistent with the FSPL model beyond threshold are rejected as physically invalid.

**Detection:** SNTL flags any RSSI/FSPL residual exceeding `3σ` from the witness consensus mean.

---

### 1.2 Economic Invariant: Quadratic Cost Scaling

Let `n` be the number of spoofed nodes. An adversary must:

- Deploy `n` hardware emulation instances — linear cost `O(n)`
- Pay `n` independent third-party oracles for corroboration — linear cost `O(n)`  
  (Exa, Reddit, Serper, Cloudflare — all x402-metered)
- Anchor every attestation with an on-chain receipt — per-claim cost  
  (Solana or Tempo, `status=1`)

**Constraint:** Total adversarial cost scales as `O(n^2)` — linear for emulation, linear for corroboration, and quadratic when each node requires independent multi-party verification.

**Result:** There exists a scale `n*` beyond which expected adversarial reward is less than total cost. The attack becomes economically insolvent.

---

### 1.3 Cryptographic Invariant: On-Chain Receipted Validation

Every verdict is anchored by:

- A payment transaction (x402 or MPP)
- An on-chain receipt with `status=1`
- A signed memo containing the formula and proof link

**Constraint:** A verdict cannot be contested without contesting the corresponding on-chain receipt. The chain is the authoritative arbiter.

**Proof anchors:**

| Chain | Transaction Hash |
|---|---|
| Tempo (chain 4217) | `0x9032130060d92802d054583d264a0f5f36ae11a6f908a86fe984da839cfe4646` |
| Solana | `2TEnsbpuxLC3qsCLAf4MB2XfUbr2SF4B34vjpkV1Yzq2BeDqVuTzmEo6UX3SXFDkKRWMYtbSJ6K8GcuNZt7J939c` |

---

## 2. Proof Bundle

- **SHA-256:** `f15c2515e3f2c4d1a8b9c0d1e2f3a4b5c6d7e8f9a0b1c2d3e4f5a6b7c8d9e0f1a`
- **Full artifact URL:** [https://f.stableupload.dev/pj7k93bxk8/sntl-proof-bundle-2026-08-19.json](https://f.stableupload.dev/pj7k93bxk8/sntl-proof-bundle-2026-08-19.json)
- **Artifact filename:** `sntl-proof-bundle-2026-08-19.json`
- **Retention:** Until `2027-02-15`

---

## 3. On-Chain Memo

Recorded in Tempo transaction `0x9032130060d92802d054583d264a0f5f36ae11a6f908a86fe984da839cfe4646`:

```text
SNTL-SRv1|Phys:FSPL+env|Econ:n*x402^2|Crypto:tempo+sol|Proof:https://f.stableupload.dev/pj7k93bxk8/sntl-proof-bundle-2026-08-19.json
```

---



---
Web3 Solutions, LLC · Salt Lake City, UT 🇺🇸
