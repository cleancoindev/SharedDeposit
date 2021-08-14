# SharedDeposit

- Following env best practices from https://github.com/paulrberg/solidity-template
- Pre-run checks:

```
npm run-script prettier
npm run-script lint:sol
npx hardhat compile
```

# SharedDeposit V2

Spec:

- TODO

# SharedDeposit V3

Spec:

- Use CLI options to set ETH1 exit as this upgradeable contract - contract needs to be upgradeable
- This allows trustless staking as ETH cannot to be taken by an admin
- Disable any future migrations or minting and control minting roles
- Build a large broader community multisig with partners and set it as owner of the contract
- Require a withdrawal queue to prevent bot arbitrage
- Create a oracle for single token value tracking for VETH2 price appreciation that can be updated with offchain calc on validators
- Bonus:
- Auto buy SGT from generated fees and send to master chef type contracts for rewards boost
- Require the user to have some SGT for solo staking or withdrawing VETH2 into ETH at a discounted market rate
- Allow the contract to be deployed via a factory allowing others to reuse the scaffolding to create their own ETH2 staking solutions i.e. staking server providers such as certus one
- Minting support to allow adding a new minter to support swapping a share token into a yield bearing sharing token controlled by the oracle module
  e.g. swapping veth2 to a yield bearing eth2 validator share derivative token
- Support for stable coins
- Address blocklist; currently deploying a new eth2 validator takes effort. one can assume exiting one would also take effort. a blocklist would prevent a malicious address from forcing continous entries and exits e.g. an address adding and exiting 1000s of eth every epoch. some parameters should be set to prevent user concers such as a final exit allowance