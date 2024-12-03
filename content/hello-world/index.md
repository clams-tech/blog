+++
title = "Hello World"
date = 2024-11-26
+++

> Clams is accounting software for Bitcoin. Sync all your Bitcoin data in one place, derive insights, and generate reports. With full support for Onchain and Lightning, the app is highly specialized to help individuals and businesses operate on a Bitcoin Standard. We'll be launching our enterprise offering in 2025. [Join our waitlist](http://eepurl.com/i5kuF-/) to get early access.

### Problem

It all started with a simple question: **_Can we live on a Bitcoin standard today?_**

To find out, we ran Lightning nodes for daily payments. For months, we paired our nodes with services like Bitrefill and MoonPay. In most jurisdictions, every spend is a taxable event. Even though our nodes maintained a full transaction history, accounting for all activity proved to be far more complex. Transaction types like force-closed channels, HTLC resolutions and zaps presented some very unique challenges.

Lightning is only one piece of the puzzle. Bitcoin takes many forms: on-chain, off-chain, custodial, non-custodial. Holders use multiple wallets like single-sig, multi-sig, collaborative custody, exchanges, and everyday wallets like Phoenix or Alby. New economic models are emerging like Value for Value that emphasize the direct exchange of value between creators and their audiences without intermediaries.

Our experiment informed us that many Bitcoin holders do not want to spend due to the tax headache of accounting for all the capital gains calculations. It’s not so much that they don’t want to pay the taxes— they are usually quite small— but the hours spent messing with spreadsheets and calculations are a significant deterrent.

It is not easy to get a full picture of your holdings or generate something like a profit and loss report if you are a small business.

Bitcoin may be the best money, but without a dedicated accounting tool, it’s hard to use as everyday money.

![Audit visualization](./audit.jpg)

### Current Solutions

When it came to tax season we were left with little option but to write custom scripts to convert our Bitcoin data into a format that can be consumed by the likes of QuickBooks or some of the emerging "crypto" accounting apps. It is a very technical process, and ultimately you have to dox yourself to these companies which doesn’t feel right. It is time-consuming, inadequate, not private, and very costly if you outsource this task to someone else. To our surprise, many Bitcoin holders are doing the same thing, wasting a weekend or more of their lives every year.

Many “crypto” accounting platforms claim to handle Bitcoin, but they typically offer limited support for on-chain transactions. After a weekend of wrangling custom scripts, we managed to convert our Lightning data into a format that one such accounting software could read. Still, it felt wrong to share so much personal data with an external company.

This got us thinking: How many other Bitcoiners face the same issue? Is accounting a barrier to building Bitcoin circular economies? What if there was a platform dedicated to Bitcoin accounting? What would that look like?

There are no Bitcoin-first solutions currently available that uphold the principles of Bitcoin.

We decided to make it our mission to solve the accounting problem for Bitcoin so that we can help accelerate the transition to a Bitcoin standard. We believe it’s about time the best money had a dedicated accounting tool.

That’s when we realized we needed to build Clams: a desktop app that gives Bitcoiners a complete view of their holdings, without compromising privacy.

![Coin visualization](./coin.jpg)

### Our Solution

With Clams, users can sync all relevant data from their on-chain and Lightning wallets locally. The Clams engine converts everything into double-entry bookkeeping standards, and an intuitive UI provides visualizations that highlight key insights. Your data stays on your device, and the app automatically tracks transfers between wallets. Capital gains and other reports are coming soon.

We built Clams to answer questions that Bitcoiners often find difficult, like: How much have I paid in on-chain fees this quarter? Is my routing node profitable? With Clams, these answers are easy to find.

Here are some issues that are very specific to Bitcoin and accounting:

- Knowing the current state of their business: cash on hand, cash flow, balances.
- Reports like profit and loss, capital gains, and taxes.
- The complexities of converting various Bitcoin transaction types to double-entry accounting: force-close channels, HTLC resolutions, eCash, zaps, etc.
- Managing multiple wallets and transaction types (e.g., multi-sig cold storage, self-sovereign Lightning nodes, custodial wallets) and tracking the sats flow accurately.

Here are some groups of users we know that have unique challenges with respect to accounting with Bitcoin:

- Small businesses, like a local coffee shop, that transact in Bitcoin.
- Bitcoin-native founders and businesses who raise funds in Bitcoin, hold reserves in Bitcoin, and need to report their sats flow to investors.
- Professional Lightning node operators needing to report profit and loss to investors.
- Bitcoin startups encountering roadblocks onboarding businesses because accounting tools are insufficient.

We are solving this problem by focusing on our company first. We want Clams to operate on a Bitcoin standard. We see the accounting problem as a hindrance to the development of circular economies for Bitcoin. If you talk to any small business or corporation, they use software like QuickBooks. Bitcoin deserves dedicated software. We have better money; we need better tools to support it.

We believe that for Bitcoin to thrive, it's essential to establish a circular economy where individuals earn and spend Bitcoin directly.

Bitcoin allows for a better accounting experience due to its native interoperability and fine-grained data. This enables businesses to have unparalleled insight into their state at any time—all without manual input (automatic syncs).

There are four main functions of our app: Sync, Enhance, Visualize, and Report.

#### Sync

Bring all your Bitcoin data into one place. Sync cold storage Bitcoin in an Unchained vault, Lightning node balances, and even funds on an exchange. Set up connections once, and sync updates automatically. Clams only requires read-only access from wallets.

#### Enhance

Leverage double-entry accounting standards to convert Bitcoin data into journal entries: credits, debits, income, and expenses. Smart defaults tag various transactions automatically, and the app identifies transfers between wallets for improved accuracy.

#### Visualize

Gain insights with customizable charts and visualizations. Answer questions like: How much did we spend on on-chain fees last quarter? Which Lightning channels should I close? How did we do this quarter?

#### Report

Generate reports like capital gains and profit and loss for any timeframe. For example, you can view capital gains on cold storage just for March.

### Call to Action

[Get early access to Clams Enterprise](http://eepurl.com/i5kuF-/).

[https://clams.tech](https://clams.tech)
