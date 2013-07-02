##phantomjs-linux-armv6h

###PhantomJS compiled on a Raspberry Pi (Arch Linux)

**Based on the work done by @aeberhardo [here](https://github.com/aeberhardo/phantomjs-linux-armv6l)**

PhantomJS is a headless WebKit with JavaScript API. It has fast and native support for various web standards: DOM handling, CSS selector, JSON, Canvas, and SVG. (http://phantomjs.org).

---

### Binary File
You will still need to have the prerequisites for PhantomJS installed in order to run this.

These include: `gstreamer0.10-base`, `fontconfig`, and `freetype2`

    bin/phantomjs

    $ ./bin/phantomjs --version
    1.9.1

---

### Arch Build System
This step will take quite a while and I suggest running it through `distcc` to help lessen the load on your Raspberry Pi. Documentation for using `distcc` on your Pi can be found [here](http://archlinuxarm.org/developers/distcc-cross-compiling).

You will probably also need to add some swap space to your Pi in order to avoid an `out of memory` error. You can read up on this [here](http://raspberrypi.stackexchange.com/questions/70/how-to-set-up-swap-space).

    phantomjs.tar.gz

    $ mkdir abs && tar -C abs/ -xf phantomjs.tar.gz
    $ cd abs && makepkg

---

### Pacman Package

    phantomjs-1.9.1-1-armv6h.pkg.tar.xz

    # pacman -U phantomjs-1.9.1-1-armv6h.pkg.tar.xz