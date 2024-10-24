# Data Marketplace Smart Contract

A decentralized marketplace for buying and selling digital data assets on the Stacks blockchain. This smart contract enables secure data trading with automated payment processing, access control, and user reputation management.

## Features

### Core Functionality
- List data assets with encrypted access keys
- Purchase data assets using STX tokens
- Automated fee distribution
- Secure access key management
- User reputation tracking
- Transaction history

### Security Features
- Ownership verification
- Access control mechanisms
- Encrypted data access keys
- Protected buyer/seller interactions
- Input validation

### Administrative Features
- Configurable marketplace fees
- Platform statistics tracking
- User profile management
- Asset listing management

## Contract Structure

### Data Maps
1. **data-asset-listings**
   - Stores all active and inactive data asset listings
   - Contains price, description, category, and status

2. **marketplace-user-profiles**
   - Tracks user statistics and reputation
   - Stores sales history and activity timestamps

3. **marketplace-transactions**
   - Records all purchase transactions
   - Maintains buyer-seller relationship data

4. **data-access-credentials**
   - Stores encrypted access keys for purchased data
   - Manages access control for buyers

## Usage Guide

### Listing a Data Asset
1. Prepare your data asset and generate an access key
2. Encrypt the access key off-chain
3. Call `create-data-asset-listing` with required parameters
4. Asset will be listed with a unique ID

### Purchasing an Asset
1. Identify the asset ID you want to purchase
2. Ensure sufficient STX balance
3. Call `purchase-data-asset` with the asset ID
4. Retrieve access key using `retrieve-asset-access-key`

## Fee Structure
- Platform fee: 2% (configurable)
- Seller receives: 98% of sale price
- Fees are automatically processed during purchase

## Error Codes

| Code | Description |
|------|-------------|
| u100 | Unauthorized owner access |
| u101 | Listing not found |
| u102 | Asset already listed |
| u103 | Insufficient STX balance |
| u104 | Unauthorized access |
| u105 | Invalid asset price |

## Security Considerations

### Access Control
- Only asset owners can modify listings
- Only buyers can access purchased data
- Administrative functions restricted to contract owner

### Data Privacy
- Access keys must be encrypted off-chain
- No sensitive data stored on-chain
- Secure key transmission handled off-chain

### Financial Safety
- Price validation
- Secure STX transfers
- Automated fee distribution
- Protected transaction processing

## Best Practices

### For Sellers
1. Always encrypt access keys before listing
2. Set reasonable prices
3. Provide detailed asset descriptions
4. Monitor transaction history
5. Maintain good reputation scores

### For Buyers
1. Verify asset details before purchase
2. Ensure sufficient STX balance
3. Securely store access keys
4. Check seller reputation
5. Review transaction history

## Contributing
- Fork the repository
- Create feature branch
- Submit pull request
- Follow coding standards