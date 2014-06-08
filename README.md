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
