---
description: >-
  In this page we will explore flow and fallback techniques which allows xApp to
  run smoothly. Keep in mind this might be a bit technical.
---

# Failover scenarios

Firstly xApp needs active internet connection on your device. This xApp uses combination of JS events and promises to deliver smooth experience for end-user. Lets explore fail scenarios outlined below.

## Access

Read-only XRP accounts in Xaman can view NFT list and details, but can not continue to Payment.\
Full access accounts are allowed to use Full xApp.

## XRPLWin CDN goes offline

<table data-view="cards" data-full-width="false"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:green;">Functional</mark></td></tr><tr><td>Display</td><td><mark style="color:orange;">Impaired</mark></td></tr><tr><td>Overall status</td><td><mark style="color:green;">Functional</mark></td></tr></tbody></table>

If CDN goes offline, user can see list of NFTs, user can see NFT IDs but not Image or Title. Filtering won't work.

## XRPLWin xApp server goes down

<table data-view="cards"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:red;">Offline</mark></td></tr><tr><td>Display</td><td><mark style="color:red;">Offline</mark></td></tr><tr><td>Overall status</td><td><mark style="color:red;">Critical</mark></td></tr></tbody></table>

This scenario only applies to initially loading xApp, when xApp loads fully it does not communicate anymore with xApp server.

## Connection error upon opening xApp

Reload button displayed, to reload list of NFTs. User can re-open xApp.

## Slow internet connection

This might show as delayed rendering of NFT metadata. User actions are not blocked.

## Connection error after signing Escrow transaction

Promise will be pending until reconnect. Delay in showing next step.

## Connection error after signing Burn transaction

At this point NFT is burned and user fulfilled its intent, no additional action is required of user, but xApp will try to display confirmation information.

Promise will be pending until reconnect. Delay in starting XRPL transaction verification.  On connection error, "Retry action" button will be shown which user can press to retry verification.

## User signs Escrow with different account

Memo field contains reference session ID which will be checked against burn transaction in background. User can continue to next step.

## User signs Burn transaction with different account

`tecNO_PERMISSION` code will be thrown in Xaman, xApp handles this by unlocking burn button so user can try again or cancel.

## User signs Burn transaction on unexisting NFTokenID

`tecNO_ENTRY` code will be  thrown in Xaman, xApp handles this by unlocking burn button so user can try again or cancel.

## Viewing account has very large amount of NFTs

There is hard-coded limit of 10 pages of max 400 NFTs per page which can be loaded with this xApp. Potential max upper limit of NFTs that can be pulled is 4000.

