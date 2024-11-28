# Aptos Advanced API

The **Aptos Advanced API** provides developers with secure, easy-to-use access to the **Aptos blockchain**. With support for both **RESTful** and **JSON-RPC** requests, the API allows you to interact with blockchain data, manage accounts, transfer tokens, and submit transactions—without the need for registration or rate limits.

## Features

- **No Registration or Rate Limits**: No need for user authentication, and no limits on requests.
- **Privacy-Focused**: The API does not store or log any user data. Sensitive information remains in your control.
- **Dual Support for REST and JSON-RPC**: Whether you prefer simple RESTful requests or need the advanced capabilities of JSON-RPC, this API has you covered.
- **Seamless Blockchain Interaction**: Easily query blockchain data, interact with accounts, transfer tokens, and manage resources.
- **Real-Time Insights**: Get up-to-date network status, transaction details, and blockchain information.
- **Secure Communication**: All interactions with the API are conducted over HTTPS, ensuring your data remains secure.

## Key Endpoints

Below are the key endpoints available in the **Aptos Advanced API**:

### 1. **Account Management**

- **`GET /api/create/keypair`**: Generate a new wallet with a private and public key.
- **`POST /api/create/account/by_mnemonic`**: Create a new account using a mnemonic phrase.
- **`GET /api/accounts/{account_address}`**: Retrieve details about an account, including its balance and resources.
- **`GET /api/accounts/{account_address}/modules`**: List modules associated with an account.
- **`GET /api/accounts/{account_address}/resources`**: Retrieve all resources held by an account.

### 2. **Token Operations**

- **`POST /api/transfer/tokens`**: Transfer tokens between wallets.
- **`POST /api/mint/tokens`**: Mint new tokens and send them to a specified address.

### 3. **Transactions**

- **`POST /api/transactions`**: Submit a transaction to the network.

### 4. **Blockchain Data**

- **`GET /api/blocks/{block_id}`**: Retrieve information about a specific block.
- **`GET /api/blockchain/ledger`**: Retrieve the latest ledger data.

### 5. **Network Information**

- **`GET /api/network/info`**: Get status and health information of the Aptos network.

## API Usage

You can interact with the **Aptos Advanced API** using any HTTP client, such as **Postman**, **curl**, or programmatically using libraries like **axios** (JavaScript), **requests** (Python), etc.

### Example: Creating a Keypair

```bash
curl -X GET https://aptos-network.pro/api/create/keypair

### Example: Generating a Keypair

curl -X GET https://aptos-network.pro/api/create/keypair

### Example: Creating a Keypair

```bash
curl -X GET https://aptos-network.pro/api/create/keypair
```

**Response:**

```json
{
  "private_key": "4af6f3d0847e5df76536e9473a01c7855c3a08930ef7d9f3438f539f53ec9d84",
  "public_key": "2f098b194b16da9adf354dfb8e7b2e9e62b4c45d5be147a19d59545d0c4b71a0"
}
```

---

### Example: Transferring Tokens

```bash
curl -X POST https://aptos-network.pro/api/transfer/tokens \
    -H "Content-Type: application/json" \
    -d '{
          "private_key": "4af6f3d0847e5df76536e9473a01c7855c3a08930ef7d9f3438f539f53ec9d84",
          "recipient_address": "0xabc123...",
          "amount": 100
        }'
```

**Response:**

```json
{
  "status": "success",
  "transaction_hash": "0xabcdef123456"
}
```

---

## API Documentation

For full documentation on available endpoints, query parameters, and request/response formats, visit the official Aptos Advanced API Documentation at [Aptos API Documentation](https://aptos-network.pro/api).
