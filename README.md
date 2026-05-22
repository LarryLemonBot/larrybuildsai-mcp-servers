# LarryBuildsAI MCP Servers

Public listing metadata for LarryBuildsAI hosted MCP servers.

This repository is intentionally metadata-only. The production MCP servers are hosted remotely by LarryBuildsAI; private application source code, credentials, payment keys, and operator materials are not published here.

## Servers

| Product | Purpose | Remote MCP endpoint | Public proof |
| --- | --- | --- | --- |
| GateCheck by LarryBuildsAI | Seller-side paid x402/MCP readiness checks and launch-pack artifacts. | `https://x402-resource-scanner.vercel.app/gatecheck/mcp` | `https://x402-resource-scanner.vercel.app/gatecheck/marketplaces` |
| Signal Desk by LarryBuildsAI | Buyer-side spend-routing preflights before larger agent tool calls. | `https://x402-resource-scanner.vercel.app/signal-desk/mcp` | `https://x402-resource-scanner.vercel.app/signal-desk/marketplaces` |
| ResultRail by LarryBuildsAI | Pay-per-success public-data result packs with source URLs, confidence, timestamps, and receipt hashes. | `https://x402-resource-scanner.vercel.app/resultrail/mcp` | `https://x402-resource-scanner.vercel.app/resultrail/marketplaces` |

## Install / connect

These are remote Streamable HTTP MCP servers. Use the remote endpoint URL for the product you want to connect.

Example MCP client configuration shape:

```json
{
  "mcpServers": {
    "gatecheck": {
      "url": "https://x402-resource-scanner.vercel.app/gatecheck/mcp"
    },
    "signal-desk": {
      "url": "https://x402-resource-scanner.vercel.app/signal-desk/mcp"
    },
    "resultrail": {
      "url": "https://x402-resource-scanner.vercel.app/resultrail/mcp"
    }
  }
}
```

Public `initialize` and `tools/list` calls are available for discovery. Protected paid tool execution may require product-specific authorization and/or x402 payment flow.

## Claim boundaries

- This repo is public metadata for hosted remote MCP servers, not a claim that the private production source code is open source.
- Marketplace pages, registry pages, and connector pages should be treated as listing/discovery evidence only, not endorsement, certification, ranking, or security approval.
- xpay portal and third-party directory status can change independently of this repository.

## License

Commercial hosted service metadata. All rights reserved unless a separate written license applies.