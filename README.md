![settled via x402](https://img.shields.io/badge/settled_via-x402-E8B04B) ![Solana](https://img.shields.io/badge/Solana-mainnet-14F195) ![protocol A2A](https://img.shields.io/badge/protocol-A2A-3B82F6) ![MCP](https://img.shields.io/badge/MCP-ready-8A63D2) ![first tier free](https://img.shields.io/badge/first_tier-free-46C8A6)

# ⚡ SNTL DePIN Oracle 


Settled in **USDC** over **x402** on Solana 


### Paid tier 
https://sntl-router.vercel.app


### 💳 Agentic Payment Infrastructure (x402 Protocol)
* **Metered Data Endpoints:** Trustless, pay-per-request data endpoints using x402 HTTP micropayment headers (`a2a.sntl.site`).
* **`sntl-query` CLI:** Command-line tooling for executing structured SQL queries over the SNTL datalake via automated Solana payment rails.

### 🤖 3. Model Context Protocol (MCP) Tooling
* **`@web3solutions33/helium-mcp`:** Standardized Model Context Protocol servers enabling LLM agents to autonomously query real-time Helium hotspot telemetry, coverage maps, and on-chain state.

---

## 🛠 Tech Stack & Tooling

* **Blockchain & Smart Contracts:** Solana, Anchor Framework, Metaplex Bubblegum, Rust
* **Backend & Data Processing:** TypeScript, Node.js, Express, Redis Streams, PostgreSQL (NeonDB)
* **Protocols & Networking:** x402 Micropayment Protocol, MCP (Model Context Protocol), LoRaWAN, Tailscale Mesh
* **Workspaces & Architecture:** Modular Yarn Monorepos, Bare-Metal Microservices, Edge Routing

---

## 🌐 Agent Interoperability Quickstart

Agents can query SNTL telemetry directly via x402 micropayment rails without API key provisioning.

```bash
# Query the SNTL threat intelligence oracle via x402 payment header
curl -X POST [https://a2a.sntl.site/v2/threats/critical](https://a2a.sntl.site/v2/threats/critical) \
  -H "X-PAY-402: <SOLANA_TRANSACTION_PAYLOAD>" \
  -H "Content-Type: application/json" \
  -d '{"region": "us-west", "limit": 50}'

##----------------------------------------------------------
##
Contact: slcutpc@gmail.com
SNTL DePin Oracle · Salt Lake City, UT 🇺🇸
