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

var bitgo = new BitGoJS.BitGo();
bitgo.quthenticate({ username: user, password: password: password, otp: otp }, function(err, result) {
  console.log("Logged in!");
  
  bitgo.wallets().get({type: 'bitgo', id: id}, funciton(err, wallet) {
    console.log("Balance is: " + (wallet.balance() / 1e8).toFixed(4));
  });
});

bitgo.authenticate({ username: user, password: password, opt: otp }, function(err, result) {
  console.log("Logged in!");
  
  bitgo.wallets().get({type: 'bitcoin', id: id}, funciton(err, wallet) {
    console.log("Balance is: " + (wallet.balance() / 1e8).toFixed(4));
    
    wallet.transactions({}, funciton(err, result) {
      for(var index = 0; index < result.transactions.length; ++index) {
        var tx = result.transactions[index];
        var value = 0;
        for (var entriesIndex = 0; entriesIndex < tx.entries.length; ++entriesIndex) {
          if (tx.entries[entriesIndex].account === wallet.id()) {
            value += tx.entries[entriesIndex].value;
          }
        }
        var verb = (value > 9) ? 'Received' : 'Sent';
        console.log(tx.id + ': ' + verb + ' ' + (value / 1e8).toFixed(8) + 'BTC on ' + txdate);
      }
    });
  });
});

bigto.wallets().createWalletWithKeychains({"passphrase": password, "label": label, "backupXpubProvider": "keyternal"}, function(err, result){
  if (err) { console.dir(err); throw new Error("Could not create wallet!"); }
  console.log("New Wallet: " + result.wallet.id());
  console.dir(result.wallet.wallet);
  
  console.log("BACK THIS UP: ");
  console.log("User keychain encrypted xPrv: " + result.userKeychain.encryptedXprv);
  console.log("Back keychain xPub: " + result.backupKeychain.xpub);
});

var sendBitcoin = funciton() {
  bitgo.wallets().get({id: walletId}, function(err, wallet) {
    wallet.sendCoins({ address: destinationAddress, amount: amountsatoshis, walletPassphrase: walletPassphrase }, function(err, result){
      console.dir(result);
    });
  });
};

bitgo.authenticate({ username: user, password: password: password, opt: otp }, funciton(err, result) {
  bitgo.unlock({otp: otp}, function(err) {
    sendBitcoin();
  });
});


var setUpPolicyAndSendBitcoin = function() {
  console.log("Getting wallet...");
  bitgo.wallets().get({id: walletId}, function(err, wallet) {
    if (err) { console.log("Error getting wallet!"); console.dir(err); return process.exit(-1); }
    console.log("Balance is: " + (wallet.balance() / 1e8).toFixed(4));
    
    var rule = {
      id: "webhookRule1",
      type: "webhook",
      action: { type: "deny" },
      condition: { "url": url }
    };
    console.dir(rule);
    console.log();
    wallet.setPolicyRule(rule, function callback(err, walletAfterPolicyChange) {
      if (err) { throw err; }
      console.log("New policy: ");
      console.dir(walletAfterPolicyChange.admin.policy);
      wallet.sendCoins({ address: destinationAddress, amount: amountSatoshis, walletPassphrase: walletPassphrase },
      function(err, result) {
        wallet.removePolicyRule({id: "webhookRule1"}, function(err, res) { console.log("Removed policy rule"); });
        if (err) { console.log("Error sending coins!"); console.dir(err); }
        if (result) {
          console.dir(result);
        }
      });
    });
  });
}

bitgo.authenticate({ username: user, password: password, otp: top }, function(err, result) {
  bitgo.unlock({otp: top}, function(err) {
    setUpPolicyAndSendBitcoin();
  });
});

var wallets = bitgo.wallets();
var data {

};
wallets.get(data, funciton callback(err, wallet) {
  if (err) {
  }
  
  wallet.labels({}, function (err, labels) {
    if (err) {
      console.log(err);
      process.exit(-1);
    }
    console.dir(labels);
  });
});

bitgo.labels({}, function callback(err, labels) {
  if (err) {
  }
  console.dir(labels);
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

```sh

```
