# wifi2qr

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

A simple `bash` script to share your computer's WiFi connection settings
[via QR code](https://github.com/zxing/zxing/wiki/Barcode-Contents#wifi-network-config-android).

Requires the command-line utility
[`nmcli` from NetworkManager](https://developer.gnome.org/NetworkManager/stable/nmcli.html)—plus
[`qrencode`](https://fukuchi.org/works/qrencode/) and
[ImageMagick's `display`](https://www.imagemagick.org/script/display.php) in order to actually
display the barcode.

## Installation and usage

```sh
$ curl https://raw.githubusercontent.com/dlenski/wifi2qr/HEAD/wifi2qr > ~/bin/wifi2qr
$ chmod +x !$
$ wifi2qr
```

… then read the barcode with your smartphone to connect to the
network. Tested with Android's `zxing`-based
[Barcode Scanner](https://play.google.com/store/apps/details?id=com.google.zxing.client.android).

You can also share a specific connection, by its NetworkManager
connection name or UUID with `wifi2qr CONNECTION`.
(You can list connection names with `nmcli conn`.)