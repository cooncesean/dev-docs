---
title: Managing Domains Using Contracts | UD Developer Portal
description: This guide covers how to manage UD domain records using the Etherscan and Polygonscan user interfaces to write and execute contracts.
---

# Managing Domains Using Contracts

This guide covers how to manage UD domain records using contracts. This process requires using the Etherscan and Polygonscan user interface to write and execute contracts.

## Step 1: Select a UNS Registry Smart Contract

The [UNS Registry](/developer-toolkit/reference/smart-contracts/uns-smart-contracts.md#unsregistry) contract is where domain owners store their data and is a map of domain namehashes to key-value dictionaries of records. Choose one of the Unstoppable Registry smart contracts to interact with (either mainnet or testnet).

<figure>

![polygon testnet registry contract](/images/polygon-testnet-registry-contract.png)

<figcaption>polygon testnet registry contract</figcaption>
</figure>

## Step 2: Open the "Write as Proxy" Tab for the Registry Contract

Navigate to the `Contract` tab in either the Etherscan or Polygonscan page of the Registry contract:

<figure>

![polygonscan contract tab](/images/polygonscan-contract-tab.png '#width=50%')

<figcaption>polygonscan contract tab</figcaption>
</figure>

Next, navigate to the `Write as Proxy` tab under the `Contract` tab section:

<figure>

![polygonscan write as proxy tab](/images/polygonscan-write-as-proxy-tab.png '#width=50%')

<figcaption>polygonscan write as proxy tab</figcaption>
</figure>

## Step 3: Connect Your Web3 Wallet

Click on the `Connect to Web3` button in the `Write as Proxy` tab and connect the wallet associated with the domain:

<figure class="half-inline-block">

![polygonscan connect wallet](/images/polygonscan-connect-wallet.png)

<figcaption>polygonscan connect wallet</figcaption>
</figure>

<figure class="half-inline-block">

![wallet provider list](/images/wallet-provider-list.png)

<figcaption>wallet provider list</figcaption>
</figure>

## Step 4: Manage the Domain Records

Choose the `set` or `setMany` method from the `Write as Proxy` tab section. The `set` method allows you to update a single record, while the `setMany` method allows you to update multiple records simultaneously.

<figure>

![polygonscan setMany method](/images/polygonscan-setmany-method.png '#width=50%')

<figcaption>polygonscan setMany method</figcaption>
</figure>

Next, add the records you want to manage to the `keys` and `values` fields as a single value for the `set` method or array of values for the `setMany` method.

<figure>

![adding records with setMany](/images/adding-records-with-setmany.png)

<figcaption>adding records with setMany</figcaption>
</figure>

:::info
Please see the [Record Reference](/developer-toolkit/reference/records-reference.md) guide and [reference JSON](https://github.com/unstoppabledomains/uns/blob/main/resolver-keys.json) file for all the resolver keys used by the Unstoppable Domains UNS Registry.
:::

## Step 5: Generate the Namehash of the Domain

You can generate the [namehash](/getting-started/domain-registry-essentials/namehashing.md) of a domain using any of the [Resolution Libraries](/developer-toolkit/resolution-integration-methods/resolution-libraries/libraries-overview.md) or [Resolution CLI](/developer-toolkit/resolution-integration-methods/resolution-cli.md). You can also use [online tools](https://swolfeyes.github.io/ethereum-namehash-calculator/) to calculate the namehash of the domain.

<embed src="/snippets/_namehashing-snippets.md" />

After generating the domain namehash, insert it into the `tokenId` field of the `set` or `setMany` method.

<figure>

![adding domain namehash](/images/adding-domain-namehash.png)

<figcaption>adding domain namehash</figcaption>
</figure>

## Step 6: Execute the Contract

Click the `Write` button to sign the transaction and execute the contract:

<figure>

![metamask sign transaction](/images/metamask-sign-transaction.png '#width=50%')

<figcaption>metamask sign transaction</figcaption>
</figure>

After signing the transaction, you can view its details on the blockchain explorer, like so:

<figure>

![polygonscan transaction details](/images/polygonscan-transaction-details.png '#width=50%')

<figcaption>polygonscan transaction details</figcaption>
</figure>

:::success Congratulations!
You have successfully managed your Unstoppable Domain records using contracts. Happy hacking!
:::
