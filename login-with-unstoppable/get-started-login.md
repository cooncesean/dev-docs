---
title: Login Integration Pathways | Unstoppable Domains Developer Portal
description: This page provides a step-by-step overview of the Login integration process. This feature works for Polygon and Ethereum domains.
---

# Getting Started with Login

Login with Unstoppable is a versatile feature with several integration pathways available for developers. This guide will step you through your first login integration with one of several supported libraries.

<embed src="/snippets/_login-mainnet-warning.md" />

## Step 1: Get Your Client Credentials

To begin the integration process for Login with Unstoppable, you will need to obtain and configure your client credentials using the **My Clients** and **Client Configuration** pages. Please see the [**Login Client Configuration**](/login-with-unstoppable/login-integration-guides/login-client-configuration.md) guide for more details.

When you've customized your client and saved your changes, you will need the **Client Metadata** to configure your integration. This can be copied directly from the first section of the **Client Configuration** page.

<figure>
<figcaption>Example client metadata</figcaption>

```javascript
{
    clientID: "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    redirectUri: "http://localhost",
    scope: "openid . . . "
}
```

</figure>

## Step 2: Configure Login Scopes

The `scope` property from your client metadata will contain all available scopes by default, some of which are mutually exclusive. The minimum scope required for login is `openid`.

See [Scopes for Login](./scopes-for-login.md) for more details on each of these.

## Step 3: Choose Your Integration Path

There are several ways to integrate with Login with Unstoppable, which are detailed in the chart below.

| Integration Guide                                                          | Package            | Ethereum Provider | Callback | Front-end UI       |
|----------------------------------------------------------------------------|:------------------:|:-----------------:|:--------:|:------------------:|
| [Login with Pop-up](/login-with-unstoppable/login-integration-guides/login-with-popup.md)       |`@uauth/js`          |     &#10060;     | &#10060; | JavaScript, Pop-up |
| [Login without Pop-up](/login-with-unstoppable/login-integration-guides/login-without-popup.md) |`@uauth/js`           |     &#10060;     | &#9989;  |  React, no Pop-up  |
| [Web3 React](/login-with-unstoppable/login-integration-guides/web3-react-guide.md)              |`@uauth/web3-react`  |     &#9989;      | &#10060; |     `web3-react`   |
| [Web3 Modal](/login-with-unstoppable/login-integration-guides/web3-modal-guide.md)              |`@uauth/web3-modal`  |     &#9989;      | &#10060; |     `web3-modal`   |
| [Web3 Onboard](/login-with-unstoppable/login-integration-guides/web3-onboard-guide.md)          |`@uauth/web3onboard` |     &#9989;      | &#10060; |   `web3-onboard`   |
| [Moralis](/login-with-unstoppable/login-integration-guides/moralis-guide.md)                    |`@uauth/moralis`     |     &#9989;      | &#10060; |     `moralis`      |
| [Node.js Server](/login-with-unstoppable/login-integration-guides/node-js-server-guide.md)      |`@uauth/node`        |     &#10060;     | &#9989;  |        None        |

:::info
The [UAuth Demo Application](https://uauth-demo.uc.r.appspot.com) is available for developer use along with a [single page sample application](https://github.com/unstoppabledomains/uauth/tree/main/examples/spa/src) to model the flow. Applications can also use Unstoppable Domain’s [UAuth Library](https://github.com/unstoppabledomains/uauth) to simplify the integration.
:::

## Step 4: Configure the Login UI

Login with Unstoppable has UI requirements that must be configured to properly display the authenticated user's domain name after a successful login. Please follow the instructions in the [**Login UI Configuration**](/login-with-unstoppable/login-integration-guides/login-ui-configuration.mdx) guide to complete this final step in the integration process.

## Step 5: Promote Your Application

Once your integration is live, you can [promote your application](/use-cases/promote-ud-integration.md) by submitting it to the official UD [app integrations database](https://unstoppabledomains.com/apps). 

<embed src="/snippets/_discord.md" />
