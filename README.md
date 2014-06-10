About
======

epygma is a simple python2.x script which allows you to encrypt text and files with xor and one-time pad. One-time pad was mathematically proven to be uncrackable in 1949. The key must be as long as the number of bytes you want to encrypt, for example a 10Mb key allows you to encrypt one 10Mb file or ten 1Mb files, after that you'll need to generate a new key. You need to safely exchange the keys with your friends to be able to communicate.

Usage
======
make the script executable

    chmod 777 epygma
    
then you can move it in a directory which is in your path (like /usr/bin) or launch it with ./epygma

    epygma new [-n NAME] [-b BYTES]             
    
create a new key, default lenght is 10000000bytes

    epygma xor [-i INPUT] [-k KEY] [-o OUTPUT]  
    
encrypt/decrypt a file

    epygma encrypt_text [-k KEY]                
    
encrypt text from stdin and encode it in Base64

    epygma unencrypt_text [-k KEY]              
    
decode a Base64 text from stdin and unencrypt it

    epygma import [-k KEY] [-n NAME]            
    
import a key

Why not PGP?
======
here is a quick list of pros and cons in order to help you make your choice.

PROS:

-This kind of encryption is mathematically uncrackable: you can be sure nobody will crack your messages even in a milion of years unless he finds the key. If someone happens to guess your key he could never be sure it is your key because each file or message can be unencrypted in different meaningfull ways with different keys.

-Potentially allows plausible deniability: since each file or message can be unencrypted in different ways with different keys, if you are forced to reveal your key you could generate a fake key which will unencrypt your previous communications in harmless files/messages (this feature is not implemented yet).

-The source code is very very short and simple to understand (about 200 lines in python in a single script), so presence of bugs or backdoors is unlike.

CONS:

-You need to safely exchange the keys with the persons you want to communicate with. Encrypting them with PGP, some block cipher (like AES) or trying to use the Diffie-Hellman key exchange would be completely useless since this script provides a mathematical security, while other algorithms provide a computational security. Exchanging the keys with a computationally secure algorithm will make all your message computationally (and no more mathematically) secure, completely missing the purpose of this script. The only secure way I can think of is phisically give the key to the person or burn it to a CD and send it by mail making sure nobody can open it without breaking the casing (some glue would be helpfull!).

-Each key allows to encrypt a limited amount of data: if you need to exchange huge files this can be a serious problem, if you only need to exchange text a few Mb key can work for a very very long period.

-If you or your friend miss some message your key indexes will be unsynched and you'll need to manually resync them in order to be able to communicate again (not a big deal, but can be tedious). 

Compatibility
======
The script was tested only with GNU/Linux, but should work without any modification with Windows and Mac OSX if the python interpreter is installed

Support
======
If you find any bug, have some suggestions or feature request or want to contact me for any other reason, feel free to contact me at colombo@bitmessage.ch
