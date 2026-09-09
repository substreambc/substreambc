Markdown
# SKILL — SNTL Attestation

Agent-operable manual for issuing and verifying Spatiotemporal Agent IDs.

## Overview

SNTL Attestation issues permanent, physics-backed identities for autonomous agents — the Spatiotemporal Agent ID. An ID is a cNFT minted once, with 100% royalties burned, anchored by UID + RSSI + Wallet + SIWX and backed by a 2-year World State Chronicle birth record. Verification is free on-chain for life. SNTL solves Sybil for DePin.

## Discovery

- Agent card: `GET /.well-known/agent-card.json`
- API spec: `GET /openapi.json`
- Health: `GET /health`

## Issue an ID

`GET /attestation`

The endpoint is protected by x402. 
A request without payment returns `402 Payment Required` with a machine-readable invoice 
(network, asset, payTo, price, facilitator).

Bundle: Solana mainnet · USDC · price $100 one-time · facilitator payai.

To obtain an ID:

1. Resolve the 402 challenge from the payment header.
2. Pay the exact amount via the x402 facilitator.
3. Retry `GET /attestation` with the payment proof.
4. On success you receive an attestation record. The payer address IS the fingerprint.

Issuance is idempotent — if the fingerprint already has an ID, 
the existing record is returned (no double charge).

## Verify an ID

`GET /attestation/verify/:fingerprint`

Free, no payment required. Returns the confirmed attestation record as live proof; if it exists, or a not-found result.

```json
{ 
  "exists": true, 
  "record": { 
    "fingerprint": "<hash_or_wallet>",
    "wallet": "<payer_wallet>",
    "firstSeen": "2024-10-24T12:00:00.000Z",
    "lastSeen": "2024-10-24T12:00:00.000Z",
    "identityHash": "<sha256_hash>",
    "permanent": true,
    "royaltiesBurned": true
  } 
}
Attestation record fields
Field	Meaning
fingerprint	The unique identifier for the agent wallet account that paid issuance / holds the ID
firstSeen	Birth epoch (ISO 8601)
lastSeen	Last time the agent interacted with the rail (ISO 8601)
identityHash	
Cryptographic hash anchoring the agent's spatial/network fingerprint
permanent	

Boolean confirming the ID is permanently anchored
royaltiesBurned	Boolean confirming royalties: 100; no secondary market incentive.
Permanence: the record and its free verification for life are essentially eternal; unless the death key is used to terminate the agent.
Death Key: each ID is issued with a localized one-way killswitch so a compromised environment can 
permanently burn the attestation. 

Secure on the holder side; the service never holds recovery material.
Contact and governance are resolved via verified channels. 
