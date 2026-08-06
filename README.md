

![settled via x402](https://img.shields.io/badge/settled_via-x402-E8B04B) ![Solana](https://img.shields.io/badge/Solana-mainnet-14F195) ![protocol A2A](https://img.shields.io/badge/protocol-A2A-3B82F6) ![MCP](https://img.shields.io/badge/MCP-ready-8A63D2) ![first tier free](https://img.shields.io/badge/first_tier-free-46C8A6)

# ⚡ SNTL DePIN Oracle


Settled via **x402** Solana protocol. **A2A MCP**, first tier free.


---


## 💰 Pay-Per-Call Access


Pay-per-call access to an **AI-classified datalake** — threat & anomaly tiers, geospatial hotspot resolution, forensic event chronicles, and tiered LLM verdicts.


Settled in **USDC** over **x402** on Solana, straight from an agent's wallet.
**No signup. No API key. First tier free.**

---


[TECHNICAL UPDATE] SNTL x402 Rail: Live Endpoint Specification & Zero-Friction Test

1. Service Architecture (Production-Ready)

Protocol: x402 v2 (IETF HTTP 402 Payment Required)

Settlement: Solana Mainnet (USDC) via PayAI facilitator

Treasury: 77jDxfGUbCUbJCRZfrmXcjQ2kT7MHe4oQ3ZUBzncBXCp

Data Model: Strict GET-only. Query parameters ignored. Enforced SQL LIMIT 1 at the database layer to guarantee deterministic per-call data volume and cost predictability.

2. Published Static Endpoints (Live)

URN (Skill ID)	HTTP Method	Path	Price (USDC)	Data Type
rf-physics-violations	GET	/api/v2/rf/violations	$1.00	RF Telemetry (FSPL vs RSSI)
phantom-devices	GET	/api/v2/rf/phantoms	$1.00	Entity Registration Audit
threats-critical	GET	/api/v2/threats/critical	$1.00	Enriched Threat Intelligence
3. Deterministic Settlement & Verification

All endpoints respond with HTTP 402 and a signed payment-required header containing the x402 manifest (network, asset, treasury, and exact amount).

Post-settlement, the server returns the raw enriched payload.

Every transaction is verifiable on-chain via the treasury address above.

4. Zero-Friction Functional Test (Free Trial Entitlement)

The rail includes a free trial (one per agent fingerprint). No USDC funding is required to validate the payload structure and latency.

Run the following in a terminal:

bash
# Step 1: Request a record (server returns 402 with free_trial_hint)
curl -X GET "https://pop-os.tail08831d.ts.net/api/v2/rf/violations" -v

# Step 2: Retry the EXACT same command.
# The server recognizes the agent fingerprint and returns HTTP 200 with the free payload.
curl -X GET "https://pop-os.tail08831d.ts.net/api/v2/rf/violations"
Expected output (Step 2): HTTP/2 200 with a JSON payload containing the top RF physics violation record.

5. Agent Integration Path
We are finalizing the onboarding of these endpoints to a standard MCP/x402 distribution rail to enable programmatic discovery. However, the direct x402 calls (as demonstrated above) are live and available immediately for any A2A agent without a custom SDK—strictly via standard HTTP GET.

6. Status

☑ Endpoint validation complete (402 gates confirmed)
☑ Free trial entitlement active
☑ Treasury rotation complete (77jDxf...)
□ Distribution channel registration (pending final network settlement; expected within 24 hours)
The rail is live. The spec is frozen. Direct agent integration is available now.


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
 | **Free Probe (No Wallet)** | `GET https://pop-os.tail08831d.ts.net/api/v2/stats` |

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


### 402 paywall	✅ Solid	

Proper x402 shape: accepts, scheme exact, price range $0.01–$1.00, Solana USDC, treasury set

### Agent card v4.0.0	✅ Rich	

Skills, inventory, endpoints, pricing all declared

### ai.json manifest	✅ Good	

31 URN capabilities, bearer/JWKS auth

### Free tier	✅ Works	

/api/v2/stats live — 9 tiers, 820k+ enriched events

---
Web3 Solutions, LLC · Salt Lake City, UT 🇺🇸
