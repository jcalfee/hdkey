hdkey-str
=========

[![NPM Package](https://img.shields.io/npm/v/hdkey-str.svg?style=flat-square)](https://www.npmjs.org/package/hdkey-str)
[![build status](https://secure.travis-ci.org/jcalfee/hdkey-str.svg)](http://travis-ci.org/jcalfee/hdkey-str)
[![Coverage Status](https://coveralls.io/repos/github/jcalfee/hdkey-str/badge.svg?branch=master)](https://coveralls.io/github/jcalfee/hdkey-str?branch=master)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)

A JavaScript component for [BIP32](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)(hierarchical deterministic keys).

Enhanced for blockchains that user-friendly names (account name, role name, etc).
BIP32 style integers or strings may be used in the hierarchical deterministic path.

Specification:
> m / purpose' / network' / role / account

Actual Path:
> m/48'/bts'/owner/kirby



Installation
------------

    npm i --save hdkey-str


Usage
-----

**example:**

```js
HDKey = require('hdkey-str')
seed = 'a0c42a9c3ac6abf2ba6a9946ae83af18f51bf1c9fa7dacc4c92513cc4dd015834341c775dcd4c0fac73547c5662d81a9e9361a0aac604a73a321bd9103bce8af'
hdkey = HDKey.fromMasterSeed(new Buffer(seed, 'hex'))

console.log(mk.privateExtendedKey)
// => 'xprv9s21ZrQH143K2SKJK9EYRW3Vsg8tWVHRS54hAJasj1eGsQXeWDHLeuu5hpLHRbeKedDJM4Wj9wHHMmuhPF8dQ3bzyup6R7qmMQ1i1FtzNEW'

console.log(mk.publicExtendedKey)
// => 'xpub661MyMwAqRbcEvPmRAmYndzERhyNux1GoHzHxgzVHMBFkCro3kbbCiDZZ5XabZDyXPj5mH3hktvkjhhUdCQxie5e1g4t2GuAWNbPmsSfDp2'
```


References
----------
- https://github.com/bitcoinjs/bitcoinjs-lib/blob/master/src/hdnode.js
- http://bip32.org/
- http://blog.richardkiss.com/?p=313
- https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki
- http://bitcoinmagazine.com/8396/deterministic-wallets-advantages-flaw/


License
-------

MIT
