# Cross-Chain Token Vault with ERC4626 and LayerZero OFT

This project implements a cross-chain token vault using the ERC4626 standard, integrated with LayerZero's Omnichain Fungible Token (OFT) protocol. It leverages various tools and libraries to facilitate the deployment, testing, and interaction with the smart contracts on the Ethereum network.

## Setup

1. **Install Dependencies:**

   ```sh
   pnpm install
   ```

2. **Set Up Environment Variables:**

   ```env
   MNEMONIC=
   PRIVATE_KEY=
   RPC_URL_ETHEREUM=
   RPC_URL_OPTIMISM=
   ```

3. **Compile Contracts:**

   ```sh
   npx hardhat compile
   ```

## Deployment

Deploy the contracts to the Ethereum network:

```sh
npx hardhat deploy --network ethereum --tags MyOFT
npx hardhat deploy --network ethereum --tags MyOFT4626
```

## Interaction

Use the provided script to interact with the deployed `MyOFT4626` contract:

```sh
npx ts-node interactMyOFT4626.ts
```

## Testing

Run the tests using Hardhat or Foundry:

```sh
npx hardhat test
forge test
```

## Configuration

To set LayerZero configuration, run:

```sh
npx hardhat lz:oapp:wire --oapp-config layerzero.config.ts
```

## License

This project is licensed under the MIT License.

---