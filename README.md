# 🧠 Vana Uniswap V3 Subgraph

This is a fork of the official [Uniswap V3 subgraph](https://github.com/Uniswap/v3-subgraph) customized for the **Vana Network** and deployed via [Goldsky](https://goldsky.com).

It indexes Uniswap V3-like smart contracts on Vana’s testnet and mainnet.

---

## 🔧 Deployment

### ✅ Prerequisites

- [Node.js](https://nodejs.org/) and [Yarn](https://yarnpkg.com/) installed
- Logged in to Goldsky:
  ```bash
  npx @goldskycom/cli login

---

🌐 Supported Networks

| Network          | Chain ID | Config File Path            |
| ---------------- | -------- | --------------------------- |
| Moksha (Testnet) | `14800`  | `config/moksha/config.json` |
| Vana (Mainnet)   | `1480`   | `config/vana/config.json`   |


🚀 Deploy Commands

🧪 Deploy to Moksha (Testnet)
```bash
yarn goldsky:testnet
```

🟢 Deploy to Vana (Mainnet)

```bash
yarn goldsky:mainnet
```

🔁 Versioning
Default deployment uses version: 1.0.0

To deploy a new version:

1. Edit the version number in package.json:
```bash
"goldsky:deploy-testnet": "npx @goldskycom/cli subgraph deploy uniswap-v3-moksha/X.Y.Z --path .",
"goldsky:deploy-mainnet": "npx @goldskycom/cli subgraph deploy uniswap-v3-vana/X.Y.Z --path ."
```

2. Replace X.Y.Z with the new version, then run the deploy command again.

Optional tagging:

```bash
# Tag a deployment
npx @goldskycom/cli subgraph tag uniswap-v3-moksha/X.Y.Z prod

# Untag a version
npx @goldskycom/cli subgraph untag uniswap-v3-moksha/X.Y.Z prod
```
🧱 Subgraph Build & Deployment (Manual)
You can also build/deploy without Goldsky wrappers:

Build & Deploy V3 Subgraph
```bash
yarn build --network <network> --subgraph-type v3 [--deploy]
```

Build & Deploy V3-Tokens Subgraph
```bash
yarn build --network <network> --subgraph-type v3-tokens [--deploy]
```
Note: Deployments will fail if there are uncommitted changes in the subgraph. Please commit your changes before deploying.

📁 Directory Overview
config/vana/ – Mainnet config for Vana (Chain ID 1480)

config/moksha/ – Testnet config for Moksha (Chain ID 14800)

abis/ – All relevant contract ABIs

template.env / .subgraph-env – Environment variables

*.template.yaml – Subgraph manifest templates

---

📜 License
GNU GPLv3

---

🫱🏽‍🫲🏼 Acknowledgements
Based on the open-source Uniswap V3 subgraph. Extended and customized for the Vana ecosystem.



