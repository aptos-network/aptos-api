# aptos-api
Aptos Advanced API

The Aptos Advanced API is a powerful, privacy-focused API that provides seamless access to the Aptos blockchain. It supports both RESTful and JSON-RPC request methods and allows developers to interact with the Aptos network for a variety of use cases, including blockchain data retrieval, token transfers, account management, and more.
Features

    No Registration or Rate Limits: No authentication required, and there are no request limits.
    Privacy-Focused: User data is not stored or logged. You maintain full control over your private keys and data.
    Dual Support: Supports both RESTful and JSON-RPC requests, making it flexible for different development environments.
    Blockchain Interaction: Direct access to blockchain data such as account balances, transactions, and block information.
    Secure Communication: All API interactions use HTTPS for secure data transmission.
    Real-Time Insights: Get live updates on network health, block data, and account information.

Key Endpoints

Here’s a brief overview of the available endpoints:
1. Account Management

    GET /api/create/keypair – Generate a new keypair (private and public keys).
    POST /api/create/account/by_mnemonic – Create an account using a mnemonic phrase.
    GET /api/accounts/{account_address} – Retrieve details about an account, including balances and resources.
    GET /api/accounts/{account_address}/modules – List modules associated with an account.
    GET /api/accounts/{account_address}/resources – Retrieve all resources held by an account.

2. Token Operations

    POST /api/transfer/tokens – Transfer tokens from one wallet to another.
    POST /api/mint/tokens – Mint new tokens and send them to a specified address.

3. Transactions

    POST /api/transactions – Submit a transaction to the network.

4. Blockchain Data

    GET /api/blocks/{block_id} – Retrieve details about a specific block.
    GET /api/blockchain/ledger – Retrieve the latest ledger data.

5. Network Information

    GET /api/network/info – Retrieve status and health of the Aptos network.

Usage

You can start making requests to the Aptos Advanced API using standard HTTP clients like Postman, curl, or programmatically with libraries like axios (JavaScript), requests (Python), etc.

Here’s an example of how you can use the API with curl:
Example: Creating a Keypair

curl -X GET https://aptos-network.pro/api/create/keypair

Response:

{
  "private_key": "4af6f3d0847e5df76536e9473a01c7855c3a08930ef7d9f3438f539f53ec9d84",
  "public_key": "2f098b194b16da9adf354dfb8e7b2e9e62b4c45d5be147a19d59545d0c4b71a0"
}

Example: Transferring Tokens

curl -X POST https://aptos-network.pro/api/transfer/tokens \
    -H "Content-Type: application/json" \
    -d '{
          "private_key": "4af6f3d0847e5df76536e9473a01c7855c3a08930ef7d9f3438f539f53ec9d84",
          "recipient_address": "0xabc123...",
          "amount": 100
        }'

Response:

{
  "status": "success",
  "transaction_hash": "0xabcdef123456"
}

API Documentation

For full details about the available endpoints and how to interact with them, please refer to the Aptos API Documentation.
