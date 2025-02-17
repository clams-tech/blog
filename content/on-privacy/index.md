+++
title = "On Privacy"
date = 2025-02-17
+++

### Our Commitment to Privacy

We are not interested in tracking users. We don’t use Google scripts or any other tracking software. Unlike other apps that offer accounting-like services, we do not host your data on our servers. All of your data remains on your device. We have no idea how many transactions you’ve made, what your balances are, where you reside, or even what your email address is. You just <a href="https://clams.tech/downloads" target="_blank" rel="noopener noreferrer">download Clams</a> and connect your wallets—we do not need to know anything about you.

#### How We Handle Data & Privacy

In our <a href="https://clams.tech/#faq" target="_blank" rel="noopener noreferrer">FAQ</a>, we explicitly outline every API request the app makes to external sources to help derive journal entries from all the Bitcoin data you provide via connections. Since we have a small team, we strive to balance creating a high-quality, privacy-respecting piece of software while also ensuring it remains user-friendly.

Where possible, we go out of our way to enhance your privacy. For example, when you connect an XPUB, it never leaves your device. We don’t ask a single public server for address information. Instead, we randomly select one of three different servers to retrieve address data. When fetching historical price information, we request a broad range, starting from your first transaction up to your latest. We are Bitcoiners—we get it. We don’t want to dox ourselves any more than we have to. We also recommend using a VPN while using the app so that public Electrum servers cannot correlate your personal IP address with transaction metadata.

#### Business Model & Future Privacy Enhancements

Some have asked how we plan to make money, and we want to be clear: selling user data is not something we are remotely interested in. Even if we were, we couldn’t. Over time, we will introduce more features that allow you to control how the app fetches the data needed to derive journal entries and generate reports.

For example, you could choose to use a public Blockstream server, connect your own, or trust the Clams public server when available. Perhaps using the Clams server will provide the best user experience. But if privacy is your priority, you might prefer to connect your own server. The point is—there will be options. For now, we are focused on using our time wisely: responding to feedback, fixing bugs, and prioritizing features that bring you and your business closer to life on a Bitcoin standard. If running your own Electrum server is essential to you, we recommend waiting for that feature.

#### Open Source vs. Closed Source

Although we have long been proponents of fully open-source software (see our <a href="https://github.com/clams-tech" target="_blank" rel="noopener noreferrer">GitHub</a>), we have decided to keep Clams closed source for now. Since Clams only reads data and never has permissions to spend, we believe this approach is reasonable. By contrast, we also maintain <a href="https://remote.clams.tech" target="_blank" rel="noopener noreferrer">Remote</a>, an interface for CLN, which does have the ability to spend funds. Because of this, we open-sourced Remote. At least for now, Clams remains closed source, though we are open to revisiting this decision in the future.

#### Don't Trust, Verify

Since the code is not publicly auditable, here’s a short video demonstrating how you can independently verify all the API calls made by the app:

<div class="responsive-video"> <iframe width="560" height="315" src="https://www.youtube.com/embed/KfHqzAlbEVg?si=rjzbgnO70ul8eZIK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> </div>
