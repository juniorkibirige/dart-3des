# dart_3des

Triple DES and DES block cipher implementation ported from CryptoJS

[![Build Status](https://travis-ci.com/juniorkibirige/dart-3des.svg?branch=main)](https://travis-ci.com/juniorkibirige/dart-3des)

This is ported from CryptoJS.  The latest version can be found
[bryx/cryptojs][crypto-js1] or [sytelus/CryptoJS][crypto-js2]

[crypto-js1]: https://github.com/brix/crypto-js
[crypto-js2]: https://github.com/sytelus/CryptoJS


## Example

```dart
import 'package:dart_3des/dart_3des.dart';

main() {
  var key = "cipher";
  var blockCipher = new BlockCipher(new DESEngine(), key);
  var message = "Uganda is a really a difficult country";
  var ciphertext = blockCipher.encodeB64(message);
  var decoded = blockCipher.decodeB64(ciphertext);

  print("key: $key");
  print("message: $message");
  print("ciphertext (base64): $ciphertext");
  print("decoded ciphertext: $decoded");
}
  ```