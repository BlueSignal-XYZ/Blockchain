# Bluesignal Blockchain Contracts

This repository contains the Solidity smart contracts, deployment scripts, and tests used for Bluesignal’s on-chain components, including token logic, credit accounting, registries, and future protocol modules.

---

## Overview

The repository is structured to support:

* **Solidity contract development**
* **Automated deployments via Ethers or Web3**
* **Unit testing using Mocha/Chai**
* **Local development using Remix or Hardhat**
* **Future Bluesignal protocol contracts** (credits, registries, device attestations)

The current workspace includes default scaffolding from Remix, which provides a safe foundation for adding your own contracts.

---

## Directory Structure

```
contracts/
    Storage.sol
    Ballot.sol
    (add your Bluesignal contracts here)

scripts/
    deploy_with_ethers.ts
    deploy_with_web3.ts
    deploy_with_web3_legacy.ts
    deploy_with_remix.ts

tests/
    Storage.test.js
    Ballot_test.sol
```

---

## Contracts

The `contracts/` folder includes sample contracts you can replace or extend:

| Contract                    | Purpose                                             |
| --------------------------- | --------------------------------------------------- |
| `Storage.sol`               | Simple storage example used for deployments & tests |
| `Ballot.sol`                | Demonstrates struct + voting logic                  |
| **(Your future contracts)** | Credits, registries, tokens, etc.                   |

Replace these with Bluesignal-specific logic as development continues.

---

## Deployment Scripts

The `scripts/` directory supports deployment using either:

### **Ethers.js**

```
deploy_with_ethers.ts
```

### **Web3.js**

```
deploy_with_web3.ts
deploy_with_web3_legacy.ts
```

### **Remix built-in deployer**

```
deploy_with_remix.ts
```

**To deploy a different contract:**
Edit the script and update:

* Contract name
* Constructor arguments
* Network RPC target

---

## Running Scripts (in Remix)

1. Compile the Solidity contract first
2. Right-click any script → **Run**
3. Output appears in the Remix terminal

Remix supports limited module imports.
Supported modules include:

* `ethers`
* `web3`
* `swarmgw`
* `chai`
* `multihashes`
* `remix`
* `hardhat.ethers`

Unsupported imports will produce errors like:

```
<module_name> module require is not supported by Remix IDE
```

---

## Testing

The `tests/` directory includes:

* **Solidity tests** (via Remix test runner)
* **JavaScript tests** (via Mocha + Chai)

Example (JS test):

```
Storage.test.js
```

Example (Solidity test):

```
Ballot_test.sol
```

Run tests from Remix → **Solidity Unit Testing** or **Remix Tests** panel.

---

## Recommended Future Improvements

As Bluesignal adds real protocol logic, consider migrating to:

* **Hardhat** (preferred for production deployment)
* **Foundry** (fast, modern Solidity dev environment)
* **Automated CI pipelines**
* **Contract versioning + audits**

---

## Support

[hi@bluesignal.xyz](mailto:hi@bluesignal.xyz)
