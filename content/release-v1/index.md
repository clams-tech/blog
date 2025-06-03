+++
title = "Release v1"
date = 2025-06-15
description = "We thought to ourselves - perhaps accounting is one of the largest barriers to Bitcoin circular economies?..."
+++

## How it started

Before Clams, we were busy hacking on an interface for CLN. We weren't happy with the lack of a UI that could surface all of the cool features of [CLN](https://corelightning.org/) like [BOLT12](https://bolt12.org/), so we built [Remote](https://remote.clams.tech). After a year of node running, we were well on our way to realizing the dream of living on a Bitcoin standard... that was until we sat down to try and reconcile all of our transactions. An eclectic mix of onchain and lightning wallets, some custodial and some non-custodial, and of course some CSVs from our exchanges. After a long weekend of wrestling with custom scripts, we finally were able to reach a number for our cost basis and for our cap gains. It was brutal, manual, and definitely did not scale. It became clear to us that accounting issues were some of the biggest headaches we faced in our pursuit of exiting the fiat rails.

Here is a handful of the issues that took far too long for us to solve:

- Dealing with cap gains events when spending.
- Calculating cost basis across all wallets.
- Tracking transfers between wallets you control.
- Categorizing purchases to help with budgeting.

We always try to remind ourselves of what it felt like. What we realized is that accounting is one of the largest pain points for anyone that wants to live on Bitcoin. Perhaps it is one of the main hurdles for kicking off Bitcoin circular economies? We asked ourselves - If living on a Bitcoin standard is the future we want - why don't we focus on tackling the accountancy problem?

## The MVP

We first [debuted Clams](https://youtu.be/OaW0k9t2j4Q?feature=shared&t=34) in March 2024 to a room of fellow Bitcoiners in Austin, Texas. It was very much an MVP, something we had powered through in three months. Even then, we knew that we were onto something. From talking to people at the event we realized we were not the only ones facing similar challenges. We chatted with individuals managing their family finances. There were business owners getting paid in Bitcoin. Financial professionals like accountants and CFOs discussed how they manage Bitcoin payroll and treasuries for their clients.

Although everyone had unique issues, we were determined to build towards a solution that could help them all. After launch, feedback filtered in via Discord, video calls and Nostr messages. Our backlog of feature requests and improvements started to grow. We had a pretty good handle already on the pain points that individuals faced, but it was very enlightening to learn more from the financial professionals.

To the beta testers, we can't thank you enough for taking the time to test and provide feedback. It really has been invaluable to us. It has helped us better understand exactly what we need Clams to do for you. You have all helped inform the direction that has brought us to this v1 release.

Based on all the feedback, we focused on improving the app in these key areas:
- Onboarding
- Performance
- Privacy
- User Experience (UX)
- Feedback collection
- Notifications
- Auditability

## What has changed

Well, not everything. All data stays on your device. The app is [private by design](/on-privacy) and it is focused on Bitcoin only. The core functions have remained the same:

- **Sync** - Bring all of your bitcoin transactions into one place
- **Enhance** - Auto conversion of disparate data into unified double-entry journals. Enhance data set with custom tags and notes.
- **Visualize** - Graphs and filters to help you gain insights about your bitcoin transactions that were once almost impossible.
- **Export** - Export documents like full journal history and cap gains reports for any time frame.

However, they have all improved - a lot.

**NOTE** - We have decided to disable exports for now - and it will be reserved for a paid offering. More news on that very soon.

Now let's break down all the changes:

### Branding & Design

The first thing that you will notice when you open the app is that structure is very different from previous releases. We opted for a more traditional side navigation. This will give us a lot more room to showcase each of the core features like connections, charts and exports. The brand has also changed dramatically. We have a new logo, fonts and color palette. We worked with our friends at Finite Supply on the brand and we are very happy with the results. We have some ideas for merch, welcome to idea on that front if you are interested.

### Onboarding

We have dramatically improved the onboarding experience. When opening the app for the first time, you will be guided through some steps that you need to complete to get up and running. This includes adding your first profile and an optional step to configure the server for onchain lookups.

### Profiles

Profiles are now a thing! You can now segment wallets by ownership. Personal and business wallets as an example. Or in the case of an accountant, a profile for every client. You can create an unlimited number of profiles.

### Server Options

One of our most requested features has been the option to add your own electrum or eslora server for onchain lookups for addresses. We are delighted to announce that this feature is now available. Built with the help of Bitcoin Dev Kit, users can opt to:

- Use the Clams Esplora instance
- Use another public server like Blockstream.
- Use their own server.

This includes support for servers hosted on TOR, cheers Start9 runners.

### Support

We now have a chat window built into the app for support. We really couldn't have built Clams V1 without our beta testers so we wanted to make life easier for anyone who wishes to give us feedback. No need to join our Discord, you can now shoot us a message in the app directly. Our Discord will remain in place if you want a more community-based discussion on issues you are having.

### Auditing

We also got feedback from those in the accounting and CFO worlds that it would be nice if Clams could provide a way for auditing of data if need be. So we decided to change how we handle data. It all remains on your device, but instead of just converting all of it into double-entry journals - the app retains a copy of the raw data. Taking a Lightning node as an example, we will convert all of your forwards into income - but the forwards themselves as they come from the LND node, will remain just as they were. This will mean that in the event of such an audit, the original, clean, and unedited data will always be available.

### Notifications

An example of notifications in the app is when you are syncing a connection like an onchain wallet and you get a progress bar. We had felt for some time that our notifications were lacking - so we did a huge overhaul of those. We built them from the ground up. When syncing wallets, you will see a lot more feedback in the app that is more accurate and informative. We hope you find these useful and let us know if there are other improvements we can make on that front.

### Performance

The app itself was rebuilt in Rust from the ground up - and the performance improvements have been staggering. The goal is to serve node runners with millions of transactions, and we believe we can do this with our new architecture. For those of you running beefy Lightning nodes - give it a spin and let us know how it performs!

## What's Next

We knew that the beta app had served its purpose and for us to really deliver on the improvements we wanted, we needed to build the app from the ground up. For the nerds, the app has been completely re-written in Rust. This has improved performance by a staggering amount. The app just feels faster and more reliable. This app is built to handle millions of transactions.

With V1 we know that we have a very strong foundation upon which to build. We have many exciting plans for the remainder of the year, including features that will be bundled together as part of a paid version. Again, we want to say a special thanks to all of the beta testers. We are delighted when we hear from people who have told us that Clams has made a positive impact in their lives - especially those who are trying to live on bitcoin. We think of ourselves a few years ago, battling with custom scripts to generate a cost basis report for our Lightning nodes. And here we are today helping node runners do that with a few clicks. We have felt for some time that accounting, or the fear of it with respect to bitcoin transactions, has been a burden to adoption of circular economies. Bitcoin is money to us, the best money. And we hope that Clams can continue to provide value to those who are using it as money, saving in bitcoin, running nodes, offering services, getting paid, paying others. If you want to say hello, jump into our Discord, or shoot us an email at hello@clams.tech

Cheers,

John & Aaron
