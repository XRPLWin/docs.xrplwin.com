---
description: >-
  Change XRP Ledger or XAHAU account settings. Here you can control account
  permissions by adding or clearing flags from your account.
---

# About

This xApp is available on all networks **XRPL** and **Xahau**.

### Why is it useful?

**Jurisdiction & Taxing**\
Prevent unsolicited transactions like Remit to reach your account.

**Control**\
Have more control over your account by blocking or allowing: Trust lines, Checks, Payment Channels, NFT Offers, or require Destination Tag.

### How to run it?

To run this app you will need [**Xaman wallet**](https://xumm.app) installed on your device, available on iOS and Android.\
You also need full access to XRPL or Xahau account.

{% hint style="info" %}
Note: All flags offered in this xApp are reversible.
{% endhint %}

### Permissions

#### Allow Incoming XRP/XAH

This control will allows you to set or clear `asfDisallowXRP` flag on your account.&#x20;

Remove permission to advise users not to send native currency to this account. This rule is not enforced by the ledger protocol. Web wallets takes this flag into account when user tries to send native currency to asfDissalowXRP-enabled account and show warning to discourage users to send to that account.

#### Allow Incoming Remit (only XAHAU)

This control allows you to set or clear `asfDisallowIncomingRemit` flag on your account.

Remove permission to block incoming Remit transactions to this account. Anyone can send you Remit transaction which will allow them to send you URIToken (NFT on Xahau), IOU or XAH (native currency), even auto-create trustline(s). If you reside in country where each crypto transaction is considered taxable event it is recommended to remove this permission from your account.

#### Allow Incoming Trustline

This control allows you to set or clear `asfDisallowIncomingTrustline` flag on your account.

Remove permission to block other accounts from creating incoming trust lines. This flag may be important for token issuers.

#### Allow Incoming Checks

This control allows you to set or clear `asfDisallowIncomingCheck` flag on your account.

Remove permission to block other accounts from sending checks to this account.

#### Allow Incoming NFT Offers (only XRPL)

This control allows you to set or clear `asfDisallowIncomingNFTOffer` flag on your account.

Remove permission to block other accounts from creating NFT Offers to this account.

#### Allow Incoming Payment Channel

This control allows you to set or clear `asfDisallowIncomingPayChan` flag on your account.

Remove permission to block new payment channels to be created to this account.

#### Require Destination Tag

This control allows you to set or clear `asfRequireDest` flag on your account.

If enabled incoming transactions must include Destination Tag. If you use account for business and want to track each transaction to match it with centralized database of your clients, enable this flag. Exchanges have asfRequireDest-enabled accounts to prevent deposits without destination tag.

### Maintainer

**XRPLWin**\
[xrplwin.com](https://xrplwin.com)\
