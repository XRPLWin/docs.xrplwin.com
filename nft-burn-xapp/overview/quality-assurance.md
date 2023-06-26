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

<table data-view="cards" data-full-width="false"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:green;">Functional</mark></td></tr><tr><td>Display</td><td><mark style="color:orange;">Impaired</mark></td></tr><tr><td>Overall status</td><td><mark style="color:green;">Non-critical</mark></td></tr></tbody></table>

If CDN goes offline, user can see list of NFTs, user can see NFT ID but not Image or title. Filtering wont work.

## XRPLWin Payment processor goes offline

<table data-view="cards"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:green;">Functional</mark></td></tr><tr><td>Display</td><td><mark style="color:green;">Functional</mark></td></tr><tr><td>Overall status</td><td><mark style="color:green;">Functional</mark></td></tr></tbody></table>

If Payment processor goes offline, xApp will not be affected. Pending Escrows may not be furfilled within 2 (two) days and user can choose to Cancel them on XRPLWin's expense.

## XRPLWin xApp server goes down

<table data-view="cards"><thead><tr><th>Subject</th><th>Result</th></tr></thead><tbody><tr><td>xApp Functionality</td><td><mark style="color:red;">Offline</mark></td></tr><tr><td>Display</td><td><mark style="color:red;">Offline</mark></td></tr><tr><td>Overall status</td><td><mark style="color:red;">Critical</mark></td></tr></tbody></table>

