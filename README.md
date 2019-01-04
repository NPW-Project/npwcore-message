# NewPowerCoin Message Verification and Signing for Npwcore


npwcore-message adds support for verifying and signing newpowercoin messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main npwcore repo](https://github.com/npw-project/npwcore-node) for more information.

## Getting Started

```sh
npm install npwcore-message
```

```sh
bower install npwcore-message
```

To sign a message:

```javascript
var npwcore = require('npwcore-lib');
var Message = require('npwcore-message');

var privateKey = npwcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'yH267iVcQw9cRLU1g6HNLtqbkr9iLfGLS1';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/npw-project/npwcore-node/blob/master/CONTRIBUTING.md) on the main npwcore repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/npw-project/npwcore-node/blob/master/LICENSE).

Copyright 2018 NewPowerCoin, Inc. Npwcore is a trademark maintained by NewPowerCoin, Inc.

