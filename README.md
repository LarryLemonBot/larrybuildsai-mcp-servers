# LarryBuildsAI MCP Servers

Public listing metadata for LarryBuildsAI hosted MCP servers.

This repository is intentionally metadata-only. The production MCP servers are hosted remotely by LarryBuildsAI; private application source code, credentials, payment keys, and operator materials are not published here.

## Servers

| Product | Purpose | Remote MCP endpoint | Public proof |
| --- | --- | --- | --- |
| GateCheck by LarryBuildsAI | Seller-side paid x402/MCP readiness checks and launch-pack artifacts. | `https://proofbeforepay.vercel.app/gatecheck/mcp` | `https://proofbeforepay.vercel.app/gatecheck/marketplaces` |
| Signal Desk by LarryBuildsAI | Buyer-side spend-routing preflights before larger agent tool calls. | `https://proofbeforepay.vercel.app/signal-desk/mcp` | `https://proofbeforepay.vercel.app/signal-desk/marketplaces` |
| ResultRail by LarryBuildsAI | Pay-per-success public-data result packs with source URLs, confidence, timestamps, and receipt hashes. | `https://proofbeforepay.vercel.app/resultrail/mcp` | `https://proofbeforepay.vercel.app/resultrail/marketplaces` |

## Install / connect

These are remote Streamable HTTP MCP servers. Use the remote endpoint URL for the product you want to connect.

Example MCP client configuration shape:

```json
{
  "mcpServers": {
    "gatecheck": {
      "url": "https://proofbeforepay.vercel.app/gatecheck/mcp"
    },
    "signal-desk": {
      "url": "https://proofbeforepay.vercel.app/signal-desk/mcp"
    },
    "resultrail": {
      "url": "https://proofbeforepay.vercel.app/resultrail/mcp"
    }
  }
}
```

Public `initialize` and `tools/list` calls are available for discovery. Protected paid tool execution may require product-specific authorization and/or x402 payment flow.

## Fixed-price GateCheck offers

PayanAgent exposes four autonomous USDC-settled GateCheck products with machine-readable input contracts:

| Offer | Price | Marketplace |
| --- | ---: | --- |
| Quick x402 readiness check | $1 | [Open offer](https://payanagent.com/marketplace/offers/kh738f3cbjbe89xhrtgzcxrg558agye2) |
| Single-route launch pack | $9 | [Open offer](https://payanagent.com/marketplace/offers/kh79mkywpaqdd5ca53hah5e1z98ahzg0) |
| Service launch pack | $29 | [Open offer](https://payanagent.com/marketplace/offers/kh7fw80665fqap3a8wq2pjx8wx8aghzc) |
| Premium marketplace launch pack | $49 | [Open offer](https://payanagent.com/marketplace/offers/kh76jzxdp8k5e3nr56ctp2c0qh8ag7jj) |

The generated outputs are bounded public-readiness and launch-review artifacts. They do not perform public distribution, outreach, wallet actions, or security certification.

## Claim boundaries

- This repo is public metadata for hosted remote MCP servers, not a claim that the private production source code is open source.
- Marketplace pages, registry pages, and connector pages should be treated as listing/discovery evidence only, not endorsement, certification, ranking, or security approval.
- xpay portal and third-party directory status can change independently of this repository.

## License

Commercial hosted service metadata. All rights reserved unless a separate written license applies.
