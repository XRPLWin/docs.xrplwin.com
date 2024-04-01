---
description: Read about application flow.
---

# How it works?

## NFT selection

When you first open xApp an lookup query goes to fetch list of your NFTs on XRPL. List then renders on your screen.

Additional metadata from CDN servers are then overlay-ed over pulled NFTs including NFT image and title. List is fully searchable by metadata title.

Press on NFT you wish to burn to select it, then details will be displayed on screen: Meta image, Meta title, NFTokenID, Issuer, Collection and Serial number.

{% hint style="info" %}
You can press graphics to zoom image or animation.
{% endhint %}

#### Burn indicator

After first sucessful burn, on the top of the screen burn indicator will be shown to tell you how much more tokens you can burn, before restarting the xApp.

## Burning NFT

Next step in burn process is last step, selected NFT with Image and Title is once again displayed. You need to press "I understand this cannot be undone" if you wish to continue. "<mark style="color:red;">Burn</mark>" button will unlock.

{% hint style="warning" %}
<mark style="color:orange;">**Always double check NFT ID before burning!**</mark>
{% endhint %}

Press "<mark style="color:red;">Burn</mark>" button to compose `NFTokenBurn` Transaction and review it in Xumm before signing, after you sign this there is **no going back**.

## Done

After you sign Burn transaction, xApp will start verifying Transaction ID on XRPL to check if its actually executed with Success code. If yes "Success!" page will be shown.

You can now burn another token or quit xApp to check burn transaction in transaction list.
