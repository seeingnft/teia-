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
