---
description: >-
  In this page we will explore flow and fallback techniques which allows xApp to
  run smoothly. Keep in mind this might be a bit technical.
---

# Quality assurance

Firstly xApp needs active internet connection on your device. This xApp uses combination of JS events and multithreading tasks (promises) to deliver smooth experience for end-user. Lets explore fail scenarios outlined below.

## Access

Read-only XRP accounts in Xumm can view NFT list and details, but can not continue to Payment.\
Full access accounts are allowed to use Full xApp.

## XRPLWin CDN goes offline

<table data-view="cards" data-full-width="false"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:green;">Functional</mark></td></tr><tr><td>Display</td><td><mark style="color:orange;">Impaired</mark></td></tr><tr><td>Overall status</td><td><mark style="color:green;">Functional</mark></td></tr></tbody></table>

If CDN goes offline, user can see list of NFTs, user can see NFT ID but not Image or title. Filtering wont work.

## XRPLWin Payment processor goes offline

<table data-view="cards"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:green;">Functional</mark></td></tr><tr><td>Display</td><td><mark style="color:green;">Functional</mark></td></tr><tr><td>Overall status</td><td><mark style="color:green;">Functional</mark></td></tr></tbody></table>

If Payment processor goes offline, xApp will not be affected. Pending Escrows may not be furfilled within 2 (two) days and user can choose to Cancel them on XRPLWin's expense.

## XRPLWin xApp server goes down

<table data-view="cards"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:red;">Offline</mark></td></tr><tr><td>Display</td><td><mark style="color:red;">Offline</mark></td></tr><tr><td>Overall status</td><td><mark style="color:red;">Critical</mark></td></tr></tbody></table>

## Connection error upon opening xApp

Reload button displayed, to reload list of NFTs. User can re-open xApp.

## Slow internet connection

This might show as delayed rendering of NFT metadata. User actions are not blocked.

## Connection error after signing Escrow transaction

Xumm Promise will be pending until reconnect. Delay in showing next step.

## Connection error after signing Burn transaction

At this point NFT is burned and user fulfilled its intent, no additional action is requred of user, but xApp will try to display confirmation information.

Xumm Promise will be pending until reconnect. Delay in starting XRPL transaction verification.  On connection error, "Retry action" button will be shown which user can press to retry verification.

## Worst case scenario

User burns single token and can not continue to burn another with the same Service Fee.
