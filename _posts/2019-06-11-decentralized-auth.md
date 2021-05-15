---
layout: post
title: "Decentralized Authentication"
icon: key
---

![Dauth]({{site.baseurl}}/images/dauth/dauth.webp)

During my pre final year of engineering, I was studying cryptography and came across open authentication standards such OAuth. My professor described SSO based authentication as the new cool kid on the block in 2005. It was all the rage with enterprises and everyone wanted their LDAP servers to provide some sort of SSO functionality. Fast forward to the next decade, SSO is present everywhere. Any website which allows you to login using your Google / Facebook / Apple / Github account essentially uses their SSO infrastructure to get indentifiable details about you without you ever having to create an account on their database or provide them your email explicitly. Unfortunately though, what was started as a convinience tool for enterprise users has now become a weapon for technology giants to strengthen their monopolies.

> Convinience always comes at the cost of Security

By providing a free SSO based OAuth service to developers and website owners, companies like Facebook get complete visibility on what kind of websites a user visits. This allows them to know your interests, preferences, content you would be stimulated by. They later choose to sell that dataset to advertisers, turning you into the monetized product. But enough about that, we all know their business model.

### What other options do we have?

I started looking for alternatives and found a couple privacy focussed SSO projects. But they were either unmaintianed and shut down or had almost no userbase. While these projects claimed to be respectful of the user data they collected, there is never a fool-proof way to verify that.

Why do you think only a handfull of companies provide this service? Because these are most popular services around the globe. There is a good chance that you would have a facebook or a google account. Leveraging this market presence has only bolstered the adoption of SSO.

So I started exploring the idea of authentication on blockchains which would ensure trust among the users and providers, and it was very much feasible. Theoretically,

- A smart contract could be deployed which stores and returns user data when demanded.

- A user can create an account with it by sending it a transaction with their details.

![screenshot1]({{site.baseurl}}/images/dauth/dauth_signup.png)

- When a website requests for login details, the user sends a signed transaction to the contract

- The contract verifies the signed transaction and returns the user details

- The user data arrives in the frontend of the website requesting auth (using a web wallet like metamask)

![screenshot1]({{site.baseurl}}/images/dauth/dauth_transaction.png)

### And it works!

Check it out here

[![repo](https://opengraph.githubassets.com/eb80eaa0064accb07bc240ff9c8987d91f4da6e2b45fe26261f53117f0a38b7d/adigupta13/Decentralized-Auth)](https://github.com/adigupta13/decentralized-auth)
