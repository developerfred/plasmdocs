# Testnet

{% hint style="info" %}
Main aim of Plasm Testnet is experimental network for community integration and public tests.
{% endhint %}

### Versioning <a id="versioning"></a>

* spec-name: plasm-testnet
* impl-name: plasm-testnet-node

Version naming notion:

* For authoring version, it just equals to the testnet generation spec, testnet generation will not change authoring interface.
* For spec/impl versions, two numbers are used, the high number is for testnet generation, the low number for testnet runtime upgrades \(probably we will have no more than 9 patch fixes for testnet generation\). Example: 10 for Testnet v1 genesis, 21 for Testnet v2 patch 1.

Testnet generation could be or not compatible with old network. In my opinion, for testnets periodic blockchain wipe isn't bad, it helps resource saving for testnet participants.

**Estimated life cycle for testnet generation is approximately from two weeks to two months.**

### Testnet migration guidelines <a id="testnet-migration-guidelines"></a>

Testnet upgrade could be two types:

* major upgrade
* minor runtime patch

Runtime upgrade is acceptable for minor patches, end users should not notice a change of this upgrade. It’s an easy way to introduce small non breakable features / patches for the network.

For the major upgrade the high version number is changed and testnet version is increased. This mean that testnet started from scratch. Major updates could be used for introducing breakable features or blockchain wipes for network participants' resource-saving.

## Dusty Plasm <a id="dusty-plasm"></a>

This is Plasm `canary` network, it looks like `beta` of Mainnet. **Dusty** predict mainnet runtime source code for 1-2 weeks.

### Incentives <a id="incentives"></a>

Yes, Dusty network participation is incentivized by default. Dusty pay rewards in PLD \(network native token\) for each PoA validator and DApp operator nominators.

> When Plasm Network token distribution finish Stake Technologies team plan distribute **0.5%** of Plasm tokens for Dusty token holders.

Planned features:

* Multi-lockdrop
* Optimistic Virtual Machine

### Version <a id="version"></a>

* authoring\_version: 4
* spec\_version: 40
* impl\_version: 40

#### Core modules <a id="core-modules"></a>

* System - core substrate functionality.
* Timestamp - timestamp runtime oracle.
* Session - authority session keys management.
* Babe - block producing consensus engine.
* Grandpa - block finalizing consensus engine.
* Indices - account indexing engine.
* Balances - native asset operations.
* RandomnessCollectiveFlip - source of random numbers.
* Contracts - smart contract support.
* Sudo - superuser actions.

#### StakeTechnologies modules <a id="staketechnologies-modules"></a>

* Operator - smart contract operator support.
* DappStaking - stake on decentralized application to collect operator rewards.
* PlasmValidator - authority manager for Plasm network.
* PlasmRewards - this module split block rewards between dapp operators and validators.
* PlasmLockdrop - multi-lockdrop token distribution.

## Plasm Testnet v3 <a id="plasm-testnet-v3"></a>

This is a reference network for future mainnet.

Planned features:

* token distribution according to lockdrop results;
* operator staking;
* validator rewards.

### Version <a id="version"></a>

* authoring\_version: 3
* spec\_version: 30
* impl\_version: 30

#### Core modules <a id="core-modules"></a>

* System - core substrate functionality.
* Timestamp - timestamp runtime oracle.
* Session - authority session keys management.
* Babe - block producing consensus engine.
* Grandpa - block finalizing consensus engine.
* Indices - account indexing engine.
* Balances - native asset operations.
* RandomnessCollectiveFlip - source of random numbers.
* Contracts - smart contract support.
* Sudo - superuser actions.

#### StakeTechnologies modules <a id="staketechnologies-modules"></a>

* Operator - smart contract operator support.
* PlasmStaking - Plasm operator nominating and rewards support.

## Plasm Testnet v2 <a id="plasm-testnet-v2"></a>

This testnet is used for testing manual management of community validators and experiment with permission for validating blocks for community members as same as integration with ink-playground contract upload sandbox.

### Version <a id="version"></a>

* authoring\_version: 2
* spec\_version: 20
* impl\_version: 20

### Modules <a id="modules"></a>

List of enabled runtime modules.

#### Core modules <a id="core-modules"></a>

* System - core substrate functionality.
* Timestamp - timestamp runtime oracle.
* Session - authority session keys management.
* Babe - block producing consensus engine.
* Grandpa - block finalizing consensus engine.
* Indices - account indexing engine.
* Balances - native asset operations.
* RandomnessCollectiveFlip - source of random numbers.
* Contracts - smart contract support.
* Sudo - superuser actions.

#### StakeTechnologies modules <a id="staketechnologies-modules"></a>

* Operator - smart contract operators.
* SessionManager - PoA validator management.

