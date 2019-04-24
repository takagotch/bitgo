### bitgo
---
https://bitgo.github.io/bitgo-docs/

```js
var BitGoJS = require('BitGoJS/src/index.js');
var bitgo = new BitGoJS.BitGo();

bitgo.ping({}, function(err, res) {
});


var BitGoJS = require('BitGoJS/src/index.js');

var useProduction = false;
var bitgo = new BitGoJS.BitGo(useProduction);

bitgo.ping({}, function(err, res) {
  if (err) {
    console.dir(err);
  } else {
    console.log(JSON.stringify(res, null, 4));
  }
});

var bitgo = new BitGoJS.BitGo({accessToken:'DeveloperAccessToken'});
bitgo.session({}, function callback(err, session) {
  if (err) {
  }
  console.dir(session);
});

bitgo.me({}, function callback(err, user) {
  if (err) {
  }
});

var useTestnet = false;
var bitgo = new Bitgo(useTestnet);
bitgo.authenticate({ username: user, password: password, otp: otp }, function callback(err, response) {
  if (err) {
  }
  var token = response.token;
  var user = response.user;
});

bitgo.logout({}, function callback(err) {
  if (err) {
  }
});

bitgo.session({}, function callback(err, session) {
  if (err) {
  }
  console.dir(session);
});

bitgo.sendOTP({forceSMS: true}, function callback(err) {
  if (err) {
  }
});

bitgo.unlock({opt: opt}, function callback(err) {
  if(err) {
  }
});

bitgo.lock({}, function callback(err) {
});

var keychains = bitgo.keychains();
keychains.list({}, function callback(err, keychains) {
  if (err) {
  }
  console.dir(keychains);
});

var blockId = '';
bitgo.blockchain().getBlock({id: blockId}, function(err, response) {
  if (err) { console.log(err); process.exit(-1); }
  console.log(JSON.stringify(response, null, 4));
});






```

```json
{
  "status": "service is ok!",
  "environment": "BitGo Test"
}

{
  "status": "400 Bad Request",
  "error": "missing user name"
}

{
  "user": {
    "id": "xxx",
    "isActive": true,
    "name": {
      "first": "Jane",
        "full": "Jane Doe",
        "last": "Doe"
    },
    "username": "janedoe@bitgo.com"
  }
}

{
  "access_token": "xxx",
  "expires_in": 3600,
  "token_type": "bearer",
  "user": {
    "id": "xxx",
    "isActive": true,
    "name": {
      "first": "Jane",
      "full": "Jane Doe",
      "last": "Doe"
    },
    "username": "janedoe@bitgo.com"
  }
}

{"client": "bitgo",
 "user": "xxx",
 "scope": 
 [ "user_manage",
   "openid",
   "profile",
   "wallet_create",
   "wallet_manage_all",
   "wallet_approve_all",
   "wallet_spend_all",
   "wallet_edit_all",
   "walletv_view_all" ],
 "expires": "2018-01-02-T02:18:11.534Z",
 "origin": "test.bitgo.com",
 "unlock": 
   {"time": "2018-91-21T01:20:25.366Z",
   "expires": "2018-01-21T01:30:25.366Z",
   "txCount": 0,
   "txValue": 0
   }
}

{
  "keychains": [
    {
      "xpub": "xxx"
    },
    {
      "xpub": "xxx"
    },
    {
      "xpub": "xxx",
      "isBitGo": true
    }
  ],
  "start": 0,
  "count": 3,
  "total": 3
}
```

```

```
