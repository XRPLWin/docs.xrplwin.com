# How it works?

## NFT selection

When you first open xApp an lookup query goes to fetch list of your NFTs on XRPL. List then renders on your screeen.

Additional metadata from CDN servers are then overlayed over pulled NFTs including NFT image and title. List is fully searchable by metadata title.

Press on NFT you wish to burn to select it, then details will be displayed on screen: Meta image, Meta title, NFTokenID, Issuer, Collection and Serial number.

{% hint style="info" %}
You can press image to zoom image or animation.
{% endhint %}

## Service Fee (Escrow)

To use xApp service you will need to escrow (reserve) **2 XRP**. Note that this will temporary add additional _2 XRP_ to your reserve until escrow is Finished or Canceled.

After you burn token, XRPLWin's background system will check proof of burn and execute `EscrowFinish` transaction against your authorized Escrow.

After 48h (two days) you can Cancel unfulfilled Escrows yourself via Xumm app.

#### Why Escrow and not Direct Payment?

Escrow adds more flexible way of paying for service. With escrow (in case of XRPLWin's payment processor goes down or you actually do not want to burn any token) 2 XRP can be returned to you without need to contact XRPLWin.

Let's say we used Direct Payment instead of Escrow, you would send 2 XRP right away, and later on you change your mind, device goes down, app gets stuck or any other reason. You will have to contact XRPLWin to issue refund.

## Burning NTF

Next step in burn proccess is last step, selected NTF with Image and Title is once again displayed. You need to press "I understand this cannot be undone" if you wish to continue, when pressed "Burn" button will unlock.

{% hint style="warning" %}
**Always double check NFT ID you are about to burn!**
{% endhint %}

Press "Burn" button to compose `NFTokenBurn` Transaction and review it in Xumm before signing, after you sign this there is no going back.

## Done

After you sign Burn transaction, xApp will start verifying on XRPL that transaction ID to check if its actually executed with Success code. If yes "Success!" page will be shown.

You can now burn another token or quit xApp. Quiting xApp will reset Service Fee and you will have to create another Escrow to continue use xApp.
