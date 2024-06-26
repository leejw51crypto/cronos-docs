# Wallet

{% hint style="danger" %}
Most of the wallet functionality is insecure / meant for development testing. To connect Wallets with Dapps/Dgames securely, we bring the open communications protocol for web3 into Unreal Engine. Please check [WalletConnect](walletconnect.md).
{% endhint %}

The following functions are members of **DefiWalletCoreActor**. The Target should be **Defi Wallet Core Actor**.

### RestoreWallet

Restore wallet with mnemonics and password.

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-RestoreWallet.png" alt=""><figcaption></figcaption></figure>

* `Mnemonics`: mnemonics to restore
* `Password`: salt in mnemonics restoration
* `Output`: generated address (index=0)
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed

## InitializeNewWallet

Create a new wallet with password and wordcount.

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-InitializeNewWallet.png" alt=""><figcaption></figcaption></figure>

* `Password`: salt in mnemonics restoration
* `Wordcount`: mnemonics word count (12, 18, 24)
* `Output`: generated address (index=0)
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed

## GetBackupMnemonicPhrase

Get backup mnemonic phrase.

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-GetBackup" alt=""><figcaption></figcaption></figure>

* `Output`: backup mnemonics
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed

## GenerateMnemonics

Generate mnemonics.

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-GenerateMnemonics.png" alt=""><figcaption></figcaption></figure>

* `Password`: salt in mnemonics restoration
* `Wordcount`: mnemonics word count (12, 18, 24)
* `Output`: generated mnemonics
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed

## GetEthAddress

Get eth address with index

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-GetEthAddress" alt=""><figcaption></figcaption></figure>

* `Index`: wallet index which starts from 0
* `Output`: get eth address
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed

## GetEthBalance

Get eth balance

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-GetEthBalance" alt=""><figcaption></figcaption></figure>

* `Address`: eth address
* `Output`: get balance
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed

## SignEthAmount

Sign eth amount

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-SignEthAmount" alt=""><figcaption></figcaption></figure>

* `Wallet Index`: wallet index which starts from 0
* `Fromaddress`: sender address
* `Toaddress`: receiver address
* `Amount`: amount in eth decimal, eg. 0.1 means 0.1 eth
* `Gas Limit`: gas limit, fee= gasLimit \* gasPrice
* `Gas Price`: gas price in wei, eg. 1wei= 1/(10^18)eth 1wei=1/(10^9)gwei
* `Txdata`: optional data
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed
* `Return Value`: signed transaction as bytes

## SendEthAmount

Send eth amount

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-SendEthAmount.png" alt=""><figcaption></figcaption></figure>

* `Wallet Index`: wallet index which starts from 0
* `Fromaddress`: sender address
* `Toaddress`: receiver address
* `Amount in Eth Decimal`: amount in eth decimal, eg. 0.1 means 0.1 eth
* `Gas Limit`: gas limit, fee= gasLimit \* gasPrice
* `Gas Price in Wei`: gas price in wei, eg. 1wei= 1/(10^18)eth 1wei=1/(10^9)gwei
* `Txdata`: optional data
* `Out`: SendEthAmount callback

## SignLogin

Sign eth login

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-SignLogin" alt=""><figcaption></figcaption></figure>

* `Wallet Index`: wallet index which starts from 0
* `Document`: document to sign
* `Signature`: get signature
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed

## VerifyLogin

Verify eth login

<figure><img src="../../../.gitbook/assets/cronos-gamefi-blueprint-VerfiyLogin" alt=""><figcaption></figcaption></figure>

* `Document`: document to verify
* `Signature`: signature to verify
* `Success`: whether succeed or not
* `Output Message`: error message, "" if succeed
