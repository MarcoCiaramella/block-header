# block-header
A module for building block header.
## Install
```
npm i @marco_ciaramella/block-header
```
## Usage
```javascript
import { Header } from "@marco_ciaramella/block-header";

const work = {
    "extraNonce1": "b4dd88d4",
    "extraNonce2Size": 4,
    "miningDiff": 0.2,
    "jobId": "221d",
    "prevhash": "f14fd6b1f15e43ee439dc5f3bda3804fdbf1d2093bd545d822f160240000000a",
    "coinb1": "03000500010000000000000000000000000000000000000000000000000000000000000000ffffffff4d02b53b049521096608fabe6d6d00000000000000000000000000000000000000000000000000000000000000000100000000000000",
    "coinb2": "0f706f6f6c2e72706c616e742e78797a0000000003001a7118020000001976a914f3f9aac36ae5e227d9d722a567ae3fafc8d1622188ac001a7118020000001976a9145d78a0c4918aef9c37e6db82255457a038753c5088ac00943577000000001976a9141a4221aeac0f92e0c6e628fbfe67c80377c3529a88ac00000000260100b53b00008d8cdb63790bc3da041a6fd15fa00c71a2b44372489362d9522dd6a019d214a2",
    "merkle_branch": [
        "d5fd81590e5ab1ae91a183bb6188edffd6359747d09a1aae9618363c6c28b8ab"
    ],
    "version": "20000000",
    "nbits": "1d1a83c0",
    "ntime": "66092195",
    "clean_jobs": true
};

const extraNonce2 = Math.floor(Math.random() * Math.pow(2, work.extraNonce2Size * 8));
const nonce = 1791689120;

new Header(work, extraNonce2, nonce).print('header');
```