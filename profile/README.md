# PromptCloak
An 8-layer, zero-trust prompt injection defense system designed for edge deployment.

## 📊 Performance
* **Recall:** 95.5%
* **Precision:** 98.1%
* **Avg Latency:** 7.94ms (p95: 16ms)

## 🏗️ Architecture

This system is split into two components:

**PromptCloak API:** The server control plane built on Cloudflare Workers and SQLite Durable Objects. Contains the IP-protected L2-L6 detection logic, policy engine, and billing enforcement.

**PromptCloak Core:** The client-side SDK (Wasm/ONNX) responsible for PII masking, L1 heuristics, and local fast-gate execution.

For a deep dive into the distributed systems decisions (Cache Poisoning, Split-Brain defense, Edge ML optimization), read the Full Architecture Decision Log.

