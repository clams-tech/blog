+++
title = "On Privacy"
date = 2025-02-14
+++

### Our Commitment to Privacy

We are not interested in tracking users. We don’t use Google scripts or any other tracking software. Unlike other apps that offer accounting-like services, we do not host your data on our servers. All of your data remains on your device. We have no idea how many transactions you made, what your balances are, where you reside, or even what your email address is. You just <a href="https://clams.tech/downloads" target="_blank" rel="noopener noreferrer">download Clams</a> and connect your wallets—we do not need to know anything about you.

## How We Handle Data & Privacy

In our <a href="https://clams.tech/#faq" target="_blank" rel="noopener noreferrer">FAQ</a>, we explicitly outline every API request that the app makes to external sources to help derive journal entries from all of the Bitcoin data that you provide the app via connections. As we have a small team we are trying to strike a balance between creating a high-quality piece of software that respects user privacy while also being very user-friendly.

Where possible, we go out of our way to improve your privacy. For example, when you connect an XPUB, it never leaves your device. We don’t ask a single public server for address information; instead, we randomly select one of three different servers for information on an address. When fetching historical price history, we fetch a large range that starts from your first transaction up until your last. We are Bitcoiners, we get it. We don’t want to dox ourselves any more than we have to. We also recommend using a VPN while using the app so that the public Electrum servers cannot correlate your personal IP address with transaction metadata.

## Business Model & Future Privacy Enhancements

Some have asked how we will make money, and we want to make it clear that selling user data is not something we are remotely interested in. Even if we were we couldn't. With time, we will introduce more features to give you control over how you want to fetch the data that is needed by the app to derive journal entries and generate reports.

For example, you could choose to only use a public server from Blockstream, connect your own, or perhaps you would prefer to trust the Clams public server when it is available. Perhaps using the Clams server would provide the best user experience. But if you care more about privacy then you would opt to connect your own server. The point is, there will be options. For now, we are just trying to use our time wisely, respond to feedback, fix bugs and power through what we consider high-priority features that we know will help bring you and your business closer to life on a Bitcoin standard. If you care deeply about using your own Electrum server, then we recommend waiting for that feature.

## Open-Source vs. Closed-Source

Although we have been huge proponents of fully open-source software for a long time (see our <a href="https://github.com/clams-tech" target="_blank" rel="noopener noreferrer">GitHub</a>), at this time we have decided to keep Clams closed source. As Clams is only reading data and never has any permissions to spend, we feel that this is fine. By contrast, we also maintain <a href="https://remote.clams.tech" target="_blank" rel="noopener noreferrer">Remote</a>, an interface for CLN, which does have the ability to spend funds. Because of that, we open-sourced Remote. At least for now, Clams is closed source and we remain open to the idea of open sourcing the code in future.

## Don't Trust, Verify

With all this being said and as it is not possible to audit the code, here is a little video we put together to show how you can independently verify all of the API calls that are made by the app:

<div class="responsive-video">
<iframe width="560" height="315" src="https://www.youtube.com/embed/KfHqzAlbEVg?si=rjzbgnO70ul8eZIK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
