
# RIFFCash Message Verification and Signing for riffcash-core



riffcash-message adds support for verifying and signing riffcash messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main litecore repo](https://github.com/riffcash/riffcash-core) for more information.

## Getting Started

```sh
npm install riffcash-message
```

```sh
bower install riffcash-message
```

To sign a message:

```javascript
var litecore = require('riffcash-lib');
var Message = require('riffcash-message');

var privateKey = litecore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H9XORZInM3B3a8BNS65kwgmbnqEuq73rjAQ5VKyVzTrzPOdHdHOY2lfoph5auvMgLSr7bh+nEQSG/f2kv9TnsbY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/riffcash/riffcash-core/blob/master/CONTRIBUTING.md) on the main riffcash-core repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/riffcash/riffcash-core/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.
Copyright 2016 The Litecoin Core Developers
Copyright 2017 The RIFFCash Core Developers

