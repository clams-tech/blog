+++
title = "Release v1"
date = 2025-06-15
description = "We thought to ourselves - perhaps accounting is one of the largest barriers to Bitcoin circular economies?..."
+++

## How it started

Before Clams, we were busy hacking on an interface for [CLN](https://corelightning.org/). We weren't happy with the lack of a UI that could surface all of the cool features like [BOLT12](https://bolt12.org/), so we built [Remote](https://remote.clams.tech). After a year of node running, we were well on our way to realizing the dream of living on a Bitcoin standard... that was until we sat down to try and reconcile an eclectic mix of onchain and lightning transactions. Read more on those pain points [here](/hello-world).

The TLDR is that we realized that accounting is one of the largest pain points for anyone that wants to live on Bitcoin. We have come to feel strongly that it is also hindering the proliferation of Bitcoin circular economies. We asked ourselves back then - if living on a Bitcoin standard is the future we want - why don't we shift our focus to tackling the accountancy problem?

## The MVP

We [launched Clams](https://youtu.be/OaW0k9t2j4Q?feature=shared&t=34) in March 2024 to a room of fellow Bitcoiners in Austin, Texas. It was very much an MVP, something we had hacked together in three months. But even then, we knew that we were onto something. After talking to a bunch of people that day we realized we were not the only ones facing similar challenges. We have individuals managing their family finances. Business owners getting paid and paying bills in Bitcoin. Financial professionals like accountants and CFOs attempting to manage Bitcoin payroll and treasury functions for their clients.

We became determined to build towards a solution that could more than just us, the individual sat stacker. After launch, feedback filtered in via Discord, video calls and Nostr messages and our backlog of feature requests and improvements started to grow. It was particularly enlightening to learn more from the financial professionals.

To the beta testers, we cannot thank you enough for taking the time to download the app, test it out and provide feedback. It really has been invaluable to us. We now better understand exactly what Clams needs to do for you.

Based on all the feedback, we focused on improving the app in these key areas:
- Onboarding
- Performance
- Privacy
- User Experience (UX)
- Feedback collection
- Notifications
- Auditability

## What has changed

Well, not everything. All data still stays on your device. The app is [private by design](/on-privacy) and we are solely focused on Bitcoin. The core functionality has remained the same:

- **Sync** - Unify all Bitcoin transactions in one place.
- **Enhance** - Convert raw data into organized journals with tags and notes.
- **Visualize** - Gain insights through customizable charts and filters.
- **Export** - Generate comprehensive reports for any time period.

However, all of these functions have improved - a lot. In fact, the engine of the app has been entirely re-written in Rust. This has yielded an incredible improvement in performance. We set the explicit goal of the app handling lightning nodes with millions of transactions. Our new architecture can do just this.

**NOTE** - We have decided to disable exports for now - More news on that very soon.

Now let's break down all the changes:

### Branding & Design

The first thing that you will notice when you open the app is that structure is very different from previous releases. We opted for a more traditional navigation that includes a sidebar. You have a dashboard where you can and add and view a list of all of your connections. Clicking on a connection will bring you to a dedicated page that expands on the connection to provide more details. We have a new logo, fonts and color palette. We worked with our friends at [Finite Supply](https://finitesupply.xyz/) on the brand overhaul and we are very happy with the results.

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
