# ERC20 Goerli to Mumbai Bridge via fxPortal
This project showcases how to utilize the fxPortal contracts to enable the seamless transfer of ERC20 tokens from the Goerli Ethereum testnet to the Mumbai Ethereum Polygon network.

### Bridging Process
Follow these steps to successfully bridge ERC20 tokens from Goerli to Mumbai:

1. Install Dependencies:
Run npm install to install the required dependencies for the project.

2. Set Up Environment:
Place your private key in the .env.examples file and rename it to .env once configured.

3. Deploy ERC20 Contract:
Deploy the ERC20 contract by executing the command npx hardhat run scripts/deploy.js --network goerli. The contract address will be displayed once deployment is successful.

4. Configure Token Address:
Replace the tokenAddress variable in other scripts with the newly deployed ERC20 contract address.

5. Specify Your Public Key:
Fill in your public key for the upcoming steps.

6. Mint Tokens to Wallet:
Run npx hardhat run scripts/mint.js --network goerli to mint tokens to your wallet.

7. Approve and Deposit Tokens:
Approve and deposit your tokens to the Polygon network by executing npx hardhat run scripts/approveDeposit.js --network goerli.

8. Wait for Confirmation:
Wait for approximately 20-30 minutes for the tokens to reflect in your Polygon account.

9. Check Token Balance:
Utilize polyscan.com to monitor your account and track the arrival of the tokens. Click on the transaction to retrieve the contract address for Polygon.

10. Get Balance on Polygon:
Replace the tokenAddress variable in the getBalance.js script with the obtained Polygon contract address. Run npx hardhat run scripts/getBalance.js --network mumbai to view your new Polygon balance.