# ElectAnon

A BLOCKCHAIN-BASED, ANONYMOUS, ROBUST AND SCALABLE RANKED-CHOICE VOTING PROTOCOL

ElectAnon arXiv link: https://arxiv.org/abs/2204.00057

## Compile

Follow https://semaphore.appliedzkp.org/docs/V1/quickstart to generate circuits & verifier.sol. Put `circuit.json` & `proving_key.bin` & `verification_key.json` and `verifier.sol` under `circuits/semaphore/build/` folder.

## Tests

These tests can be run with `npx hardhat test`:

- `electanon.js`
- `electanonslow.js`
- `SemaphoreOpt.js`
- `tideman.js`
- `gasanalysis/electanon.js`
- `gasanalysis/pairvoting.js`

A sample run: `npx hardhat test test/electanon.js`

## Detailed Documentation

### Planned and Implemented Solutions

1. **Generate Circuits and Verifier.sol**
   - Follow the instructions from the Semaphore quickstart guide to generate the necessary files.
   - Create the directory `circuits/semaphore/build/` to store the generated files.
   - Generate the `circuit.json`, `proving_key.bin`, `verification_key.json`, and `verifier.sol` files and place them under the `circuits/semaphore/build/` folder.

2. **Configure Hardhat for Testing**
   - Ensure that the `hardhat.config.js` file is configured to run tests with `npx hardhat test`.

### Step-by-Step Instructions for Creating and Storing `proving_key.bin` Securely

1. **Generate `proving_key.bin`**
   - Follow the instructions from the Semaphore quickstart guide to generate the `proving_key.bin` file.

2. **Store `proving_key.bin` Securely**
   - Use GitHub Secrets to store the `proving_key.bin` file securely.
   - Navigate to your GitHub repository and go to the "Settings" tab.
   - In the left sidebar, click on "Secrets" and then "New repository secret".
   - Name the secret `PROVING_KEY_BIN` and upload the `proving_key.bin` file.
   - In your code, access the secret using the GitHub Actions workflow.
