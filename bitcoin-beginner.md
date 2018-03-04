# Bitcoin setup guide (Beginners)

This guide is a lite opinionated guide to getting a bitcoin setup with reasonable reliability established.

If you want more detail please [see **in-depth guide**](https://docs.google.com/document/d/11fJfWa5a6FX8h-2zGI5ZZFm7bNKGN6L1wWhnfrUOMQg/edit#heading=h.q9r9wfywrj12) for more details.


**What you will need:**

- your own computer :computer: 
- 5 people you trust :family: (to give backup details)
- enough time :clock1: to follow steps slowly and not slip up

## Overview of Steps

Follow these steps patiently and if you're unclear on anything, please ask.

**Note**:  :warning: = `this is a dangerous step, follow it exactly` 


1. [Setup password manager](#1-Setup-password-manager)
2. [Setup bitcoin wallet](#2-Setup-bitcoin-wallet)
3. [Share backup of seed](#3-Share-backup-of-your-seed)
4. [Security Audit](#4-Security-Audit)
5. [Receive a small test payment](#5-Receive-a-small-test-payment)

## 1. Setup password manager

1. Install KeePassX / KeePass 
      Program | Platform | Current version
      ---|---|---|---
      KeePassX | **Mac** | v2.0.3 - [keepassx.org](https://www.keepassx.org/)
      KeePassX | **Linux** | v2.0.3 - [source](https://github.com/keepassx/keepassx) (or v2.0.2 - `apt-get install keepassx`)
      KeePass | **Windows** | v2.38 - [keepass.info](https://keepass.info/download.html)  
    - mac/ linux/ win might look different, but they have the same functionality) 

2. Open the software, start a new password database
    - in the menu click `Database > New Database`

    
3. Choose a Master Password
    > Pay close attention, being lazy here will lose your money
    - Never use this password _anywhere online_
    - Never use this password _for anything else_
    - Your passwod must be very secure 
      - longer than 12 characters
        - a line from your favourite poem or song
        - a very random phrase, try [this **sweet tool**](https://www.rempe.us/diceware/).
  

4. Save the password database
    - in the menu click `Database > Save Database`
    - put it somewhere safe

5. Save a test password
    - click `Entries > Add New Entry`
    - Enter some details and click OK
    ![](https://i.imgur.com/1c8xw9D.jpg)
    - See the new entry, right click and see you can copy the password !
    ![](https://i.imgur.com/RgQWGBP.jpg)

6. Quit out of KeePass and log back in
    - it will say you've made changes (our password), choose `Save`

If you've got this all sorted, you're now ready to save your bitcoin passwords super securely!


## 2. Setup bitcoin wallet

We're now goint to install the wallet that holds your actual bitcoin.
You wallet will be 'grown' from a **Seed** - a special string of words which can be used to recreate everything about your wallet if you lose it. (This is essentially your "private key").

--> ** Dan: The seed is what grows your wallet. A wallet may contain many private keys**
--> ** Dan: For organisations we may also propose that a multisig wallet is actually the way to go, this would mean 2/3 or 3/5 or 5/7 signatories needed to spend funds... **

1. Install the Electrum wallet - [electrum.org/#download](https://electrum.org/#download) 

2. Start Electrum, and enter a name for your wallet
3. Select:  `Standard Wallet`, then `Create a new seed`, then `SegWit`
4. :warning: Make a new KeePass entry for the **Seed** phrase (string of words that's been generated)
    - open KeePass, and follow steps above used to make a `New Entry`
    - call the entry `Electrum Seed`, and paste the seed in as the password
5. Go to the next step and pass it by copying your the password from KeePass
    - right click on the password, select `copy password`
6. Make a password to encrypt your wallet
    - make a long password with https://www.rempe.us/diceware/#eff
    - save the password as `Electrum Password` in KeyPass
    - copy that password, enter it in Electrum, selecting `encrypt wallet`
7. Check you got everything saved right!
    - quit Electrum wallet, and open it again
    - use the `Electrum password` saved in KeePass


## 3. Share backup of your seed

So you've got this Seed - a phrase from which you can regrow your wallet. We need to protect your organisation against the eventuality that you get hit by a bus (OR your computer is lost).

There's a neat trick that lets you 'shard' (split) your seed into 5 parts. You can recreate your seed by bringing any 3 of the parts together again.

1. Copy your `Electrum Seed` (from KeePass) into https://secrets.dyne.org/share
2. :warning: Double check you just copied the seed phrase!
3. Click `Submit`
4. Send each of the 5 'shards' (one shard per line) to a different friend
    - (dyne calls shards 'shares')
    - send the shards over different comms channels
    - tell the person you're sending it to what it is!
![](https://i.imgur.com/YHxsDQk.png)
5. (optional) Test you can put your seed back together
    - go to https://secrets.dyne.org/combine
    - paste in any 3 of the shards and click `submit`
    - compare with your original seed!





## 4. Security Audit

A few due dilligence questions:

- [ ] Are you in ownership of the private key? (seed)
- [ ] Have you backed up the private key?
- [ ] Have you confirmed all 5 of your trusted people have received a shard of you private key ? 

Technically that’s all I need, but unless the above are anwswered you are assuming the individual risk of the value of the tokens… is this risk you want to take on as an individual? There are ways we can mitigate this :)


## 5. Receive a small test payment

1. In Electrum, go to the Receive tab and copy your `Receive Address`
2. Give this address to someone who is going to send you bitcoin


