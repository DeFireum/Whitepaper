@@ -1,15 +1,15 @@
# react-native-stellar-sdk
# react-native-defireum-sdk

This package polyfills the [stellar-sdk](https://github.com/stellar/js-stellar-sdk) for React Native.
This package polyfills the [defireum-sdk](https://github.com/defireum/js-defireum-sdk) for React Native.

It includes native randomBytes for iOS and Android via [react-native-randombytes](https://github.com/mvayngrib/react-native-randombytes).

Due to the asynchronous nature of React Native's native bridge, this package adds a new asynchronous method to the Stellar Keypair utility `randomAsync` which returns a promise that resolves to the new randomly generated Keypair.
Due to the asynchronous nature of React Native's native bridge, this package adds a new asynchronous method to the DeFireum Keypair utility `randomAsync` which returns a promise that resolves to the new randomly generated Keypair.

## Installation

```shell
yarn add @pigzbe/react-native-stellar-sdk
yarn add git+ssh://git@github.com/DeFireum/react-native-digitalbits-sdk.git
```

Link native randomBytes module:
@@ -24,6 +22,3 @@ react-native link react-native-randombytes
## Usage

```javascript
import {Keypair} from '@pigzbe/react-native-stellar-sdk';
import {Keypair} from 'react-native-defireum-sdk';
const keypair = Keypair.randomAsync().then(keypair => {
    const publicKey = keypair.publicKey();
    const secretKey = keypair.secret();
});
```
