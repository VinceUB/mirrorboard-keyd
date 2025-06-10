MirrorBoard for keyd
====================

This is a port of [MirrorBoard][] by Randall Munroe and naele, but for [keyd][].
I made this because Mirrorboard was written as an XKB mapping in 2007, which not only doesn't work on Wayland, but also doesn't seem to work with my installation of Xorg anymore.

Installation
------------
1. Install [keyd][].
2. Copy `default.conf` over to the `/etc/keyd/` directory.
3. Start/enable keyd.

Features
--------
MirrorBoard flips your keyboard when you hold CapsLock or AltGr. On top of this, Space turns into Return, and Backtick/Tilde turns into Backspace. 

The original implementation turns 

![Standard QWERTY keyboard layout][Fig1]

into

![MirrorBoard keyboard layout][Fig2]

This port has several differences, namely:
- The entire keyboard is mirrored, not just the left side.
- Mirroring can be enabled with AltGr as well as CapsLock.
- CapsLock can still be enabled by tapping (as opposed to holding) it. This can be disabled by changing the line `capslock = overload(reverse, capslock)` to `capslock = layer(reverse)`


[MirrorBoard]: https://blog.xkcd.com/2007/08/14/mirrorboard-a-one-handed-keyboard-layout-for-the-lazy/
[keyd]: https://github.com/rvaiya/keyd

[Fig1]: https://i0.wp.com/imgs.xkcd.com/blag/qwerty450.png
[Fig2]: https://i0.wp.com/imgs.xkcd.com/blag/mirrorboard450.png
