---
title: Best Practices for Integrating Crypto Payments | UD Developer Portal
description: This page covers best practices to follow while integrating crypto payments.
---

# Best Practices for Integrating Crypto Payments

Here are best practices to ensure the proper integration of the Unstoppable Domains crypto payments feature into your applications:

## Don’t Hard-code UD Domain Endings Into Your Application

<embed src="/snippets/_new_tld_warning.md" />

## Display Resolved Addresses Near Domain Names

Always display the resolved crypto address near the domain name for additional security. Doing this helps your application's user detect and avoid Man-in-the-middle (MITM) attacks aimed at replacing the payment address with the attacker's own.

<figure>

![preview of resolved address near domain name](/images/successful-domain-resolving.png '#width=50%')

<figcaption>preview of resolved address near domain name</figcaption>
</figure>

## Don't Overwrite the Input Field With Resolved Addresses

For the best user experience of your application, don't overwrite the domain input field with cryptocurrency addresses after resolving the domain. Doing this allows them to quickly fix typos if they make any without typing the domain name again because an address has replaced it.

## Resolve Domains With the Provided Currency

When you don't find a currency address record for a domain, please do not make assumptions about the currency code and try others. Instead, inform the user that they have not set an address for the requested currency.

## Handle Errors According to Their Type

When you encounter errors using any resolution method (Resolution Libraries, Resolution Service API, CLI, Blockchain Calls), handle them according to the error type rather than generically handling them or passing them silently.

:::info
Please see the [Resolution Libraries](/developer-toolkit/resolution-integration-methods/resolution-libraries/libraries-overview.md) docs for language-specific error handling guides and library error codes you might encounter during integration.
:::

## Validate the Addresses Resolved From Domains

Always validate the addresses you resolve from domains using the resolution methods (Resolution Libraries, Resolution Service API, CLI, Blockchain Calls) because the user has complete control over the domain and can set invalid values for its records.

## Remind Your Users That They Can Use Their Domain To Send Crypto

<figure>

![preview of resolved address near domain name](/images/domain-btc-resolving-example.png '#width=60%')

<figcaption>preview of resolved address near domain name</figcaption>
</figure>

<embed src="/snippets/_discord.md" />
