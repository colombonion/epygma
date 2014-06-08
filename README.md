About
======

epygma is a simple python2.x script which allows you to encrypt text and files with xor and one-time pad. One-time pad was mathematically proven to be uncrackable in 1949. The key must be as long as the number of bytes you want to encrypt, for example a 10Mb key allows you to encrypt one 10Mb file or ten 1Mb files, after that you'll need to generate a new key. You need to safely exchange the keys with your friends to be able to communicate.

Usage
======
epygma new [-n NAME] [-b BYTES]             create a new key, default lenght is 10000000bytes
epygma xor [-i INPUT] [-k KEY] [-o OUTPUT]  encrypt/decrypt a file
epygma encrypt_text [-k KEY]                encrypt text from stdin and encode it in Base64
epygma unencrypt_text [-k KEY]              decode a Base64 text from stdin and unencrypt it
epygma import [-k KEY] [-n NAME]            import a key

Compatibility
======
The script was tested only with GNU/Linux, but should work without any modification with Windows and Mac OSX if the python interpreter is installed

Support
======
If you find any bug, have some suggestions or feature request or want to contact me for any other reason, feel free to contact me at colombo@bitmessage.ch
Use of pgp will be apreciated


-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: GnuPG v2.0.20 (GNU/Linux)

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
=DUeo
-----END PGP PUBLIC KEY BLOCK-----
