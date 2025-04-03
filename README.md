# Uniswap V3 Subgraph for Vana Networks

This is a fork of the Uniswap V3 subgraph customized for deployment to Vana's networks via Goldsky.

## Deployment

### Prerequisites
- Node.js and yarn installed
- Logged in to Goldsky (`npx @goldskycom/cli login`)

### Network Configuration
This subgraph supports two Vana networks:
- **Moksha** (Testnet, Chain ID: 14800)
- **Vana** (Mainnet, Chain ID: 1480)

Network configurations are stored in the `config/` directory:
- `config/moksha/config.json` - Moksha testnet configuration
- `config/vana/config.json` - Vana mainnet configuration

### Deploy to Moksha Testnet
```bash
yarn goldsky:testnet
```

### Deploy to Vana Mainnet
```bash
yarn goldsky:mainnet
```

### Versioning
The current deployment uses version 1.0.0. For future versions:

1. Edit the version in the `goldsky:deploy-testnet` and `goldsky:deploy-mainnet` commands in `package.json`:
```json
"goldsky:deploy-testnet": "npx @goldskycom/cli subgraph deploy uniswap-v3-moksha/X.Y.Z --path .",
"goldsky:deploy-mainnet": "npx @goldskycom/cli subgraph deploy uniswap-v3-vana/X.Y.Z --path ."
```
Replace X.Y.Z with your new version number.

2. Deploy using the commands above

3. If you need to tag versions (for production/staging):
```bash
# Tag a version
npx @goldskycom/cli subgraph tag uniswap-v3-moksha/X.Y.Z prod

# Untag a version
npx @goldskycom/cli subgraph untag uniswap-v3-moksha/X.Y.Z prod
```

---

# Original Uniswap V3 and V3-Tokens Subgraph

## Development

1. Install dependencies
`yarn install`

2. Build a v3 subgraph
`yarn build --network <network> --subgraph-type v3`

3. Deploy a v3 subgraph
`yarn build --network <network> --subgraph-type v3 --deploy`

4. Build a v3-tokens subgraph
`yarn build --network <network> --subgraph-type v3-tokens`

5. Deploy a v3-tokens subgraph
`yarn build --network <network> --subgraph-type v3-tokens --deploy`

Note: Deployments will fail if there are uncommitted changes in the subgraph. Please commit your changes before deploying.

