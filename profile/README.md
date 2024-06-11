# More coming soon, currently working on reversing MCCToolChest.

## Why reverse MCCToolChest?
This is interesting to me, when extracting a deobfuscated version of it (deobfuscated using de4dot), I saw this:
![Windows-Security-Image](https://github.com/CheatBreakerX/.github/blob/master/assets/ApplicationFrameHost_i8VaV9UpZA.png?raw=true)

At this point I was already decompiling and reversing it to implement its functionality into an Electron app, making it crossplatform, but I think you should know of this warning too.\
Of course, it could be a "false positive" and this could be nothing, but it is quite interesting already.

The program encrypts every string in a file called "`fvGvniHlL5t89jCdxt.iXRCkP2b29rLWjHYun`", what algorithm, I'm unsure, but I think it might be AES. This file is an embedded resource, meaning it's in the .exe file itself, however there is another embedded resource with it, called "`rKnD7Rxc5txuEtqdTo.nuAYrdapOvOf5d0Z8S`", which because as I said before every string in the program is encrypted turns up no result when searched, but after I made my decryptor I found this (look at string `193152`):

![Reference-to-unknown-file](https://github.com/CheatBreakerX/.github/blob/master/assets/Screenshot_2024-06-11_at_17.33.01.png?raw=true)

What references this I haven't found, I just found this a few minutes ago as of writing this. I might update this document at a later date.
