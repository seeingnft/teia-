# Introduction

Welcome to the Teia starting guide! Here you will learn how to mint and trade your first OBJKT.

> **OBJKT**
> 1: _(noun)_ something material that may be perceived by the senses
> 2: _(noun)_ an NFT minted with the hicetnunc minting contract


Continute to [Getting Started with Tezos](https://github.com/teia-community/teia-docs/wiki/Getting-started#getting-started-with-tezos) to learn how to acquire some tezos!

Already have tezos? Continue to [How to mint 🌿](https://github.com/teia-community/teia-docs/wiki/How-to-mint-🌿) to create your first OBJKT!

**Hint:** Before you start minting, you can already start setting up your profile if you already have a wallet. Read [How to set up your profile](https://github.com/teia-community/teia-docs/wiki/Edit-your-profile)

---

# Getting started with Tezos 

First, you will need a Tezos wallet and Tezos funds.

## What is Tezos?
Tezos (XTZ) is a liquid proof-of-stake cryptocurrency (LPoS). You can read more about it [on the Wikipedia Article about Tezos](https://en.wikipedia.org/wiki/Tezos).

## What wallets do you recommend?
Some wallets compatible with our dApp are:
* [Temple wallet](https://templewallet.com/) which is a browser extension similar to Metamask, also being able to connect to Ledger devices.
* [Kukai wallet](https://wallet.kukai.app/), which is a browser wallet, being possible to connect making use of Direct Auth using Twitter credentials.  Kukai also works on smartphones.

## Where to buy tezos
Minting on Teia only costs ~0.05 tezos. You can buy some tezos on an exchange site like Binance or Kraken. However, the exchange service might be limited depending on your country and location.

## The H=N Tezos Fountain
### ⛲ Applying as an Artist
Are you an artist who needs tez but can't get it? You can request a volunteer from the community to sponsor you in the #tezos-fountain channel on [Discord](https://discord.gg/EDrSbMzBeC).

Please fill out this google form:
* https://forms.gle/9NnshQ92tjs4JPw46
* After filling out the form, please send us a message in the #tezos-fountain channel on the Discord saying that you filled out the form.

### ⛲ Volunteering as a Sponsor
If you make some sales and would like to support other new artists you can send XTZ donations to `tz1eggoxCes1qYRGLc3E1bg4uzuCUUuuQBb9` or `fountain.tez`

**Common wallet errors**

_account doesn't exist error from tzkt.io_

 If your account on tzkt.io shows this, don't worry. It just means you don't have any transactions yet in your wallet. Once you receive some tezos it should go away.

_Prevalidation error in the temple wallet_

This means you should refresh the page. Wait a couple of seconds for the transaction to go through and you will get the "applied" status.

***

Already have tezos? 

Continue to [How to mint 🌿](https://github.com/teia-community/teia-docs/wiki/How-to-mint-🌿) to create your first OBJKT!

---

# How to swap

**swap**

1: _(noun)_ an act, instance, or process of exchanging one thing for another

2: _(verb)_ to set a price for your OBJKT

***

1. Click on your OBJKT's link to see the details. If you are still synced to your wallet, you should see "swap" next to "info", "
listings" and "history". (If you don’t see these options, then you have to sync your wallet again.)
2. Click on swap.
3. Input how many OBJKTs out of your edition that you want to set for sale. For example, If you have `10`, and you want to keep `1`, and sell `9`, then input `9`. If you want to sell all of them, input `10`.
4. Input how much each edition should cost in Tezos.
5. Click the "swap" button. You will be prompted to approve the transaction in your wallet app.


***


### How can I track what I've sold?

You can use [hicdex](https://hicdex.com)

### How can I get notifications for when I sell something?

You can use the [Telegram Notifier Bot](https://tzsnt.fr/) to get a notification every time something sells.


***


**Important:** _When swapping, you send an amount of OBJKTs out of your wallet. They're being held in a Teia escrow wallet, ready to be transferred to the buyer, which is why they're no longer visible in your wallet. Once the blockchain transaction finishes, the OBJKT is available for purchase at the price set, and your wallet should indicate that you sent that amount of OBJKTs._

Proceed to [How to cancel ❌](https://github.com/teia-community/teia-docs/wiki/How-to-cancel-❌) to learn how to take your OBJKT off the market or change the price.
***

### Help, my wallet is giving me an `insufficient funds available` error!
You might be trying to swap more editions than you minted, or your object is still for sale and you need to cancel it first.

***

### HELP! I keep getting the `BACKTRACKED` error and I'm using temple wallet! (`transaction likely to fail`)
You will have to manually set max storage fees (it only charges the storage fee that was really used in the operation). 

```suggested parameters:
mint - set storage to 310
swap - set storage to 180
```
![Storage fee adjustment in template wallet](https://i.ibb.co/7W3FNRR/Screen-Shot-2021-05-24-at-10-33-33-AM.png)

### HELP! I tried to raise the storage fees but I'm still getting the `BACKTRACKED` error!
If raising storage fees doesn't work, you'll have to switch to using [Kukai wallet](https://wallet.kukai.app/). You don't need to make a new wallet to do this. [Here](https://youtu.be/_9TwCzBBJGU) is a video tutorial on how to import your wallet to Kukai.

---

# How to cancel

### **cancel**

1: _(verb)_ to take your NFT off the market

***

To take your OBJKT off the marketplace and no longer for purchase:

1. Make sure your wallet is synced.
2. Load the page for your OBJKT.
3. Click on "listings" and then "cancel". This will send the OBJKTs from the escrow wallet to your wallet. Check your wallet for confirmation.
4. Now that they are back in your wallet, you can "swap" them again or burn them.

If you want to delete your OBJKT, continue to [How to burn 🔥](https://github.com/teia-community/teia-docs/wiki/How-to-burn-🔥)
***

**Important:** _If you try to "swap" OBJKTs that are currently for sale, your wallet will throw a warning saying that you have `insufficient funds`. This is because you already sent your OBJKTs to the escrow wallet in the first swap. You need to "cancel" to get the OBJKTs back in your wallet, and then you can "swap" them again._

---

# How to burn

1: _(verb)_ to "delete" your OBJKT

Transactions on the blockchain are irreversible, so you can't "delete" them. The "burn" button sends the OBJKT to the [burn address](https://tzkt.io/tz1burnburnburnburnburnburnburjAYjjX/operations/), or you can send it yourself using your wallet app. The burn address is an open address that nobody owns a key to.

To burn an OBJKT:
1. Make sure your wallet app is synced with Teia.
2. Make sure you cancel the swap of the OBJKT so it can be available in your wallet when you are ready to burn it.
![Please cancel swap prior to burn operation](https://i.ibb.co/c6x821J/sketch-1619101908825.png)
3. Press the burn button. Your wallet app will prompt you to confirm the transaction. Once the transaction completes, your wallet app will show the OBJKT as transferred to the burn address.
4. You can also send the OBJKT to a burn address directly from your Tezos wallet. The address is: `tz1burnburnburnburnburnburnburjAYjjX`. 

**Note:** _If someone buys one of your editions, even if you burn the rest of them, the OBJKT won't disappear from your profile_

---

# How to resell

How to sell an OBJKT you own.

***
This is also referred to as placing your OBJKT on the secondary market.

1. Make sure your wallet is synced.
2. Load your account page on Teia.
3. Click on "collection" and click on the OBJKT you want to resell.
4. Click on the "listings" tab to see all of the owners and sellers.
5. Click on "swap" and set a price for your OBJKT.
6. Click on the "swap" button and confirm the transaction in your wallet app.

_IMPORTANT: Once swapping something up for sale, it is held in the Teia escrow wallet while it is "on the market." Therefore, the OBJKT will disappear from your collections. Don't worry; it's still up for sale!_


***

### How can I track what I've sold?

You can use the tools on [hicdex.com](hicdex.com) to track transaction history

### How can I get notifications when I sell something?

You can use the [Telegram Notifier Bot](https://tzsnt.fr/) to get a notification everytime something sells.
