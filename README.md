## Amiibo simulator instructions

A copy of the amiitool Lua wrapper is included at `client/libluamiibo.so`, but if you want
to build it yourself, follow these instructions:

1. Get the `lua-lib` branch of amiitool at https://github.com/jamchamb/amiitool/tree/lua-lib.
1. In CMakeLists.txt set `PROXMARK_LIBLUA` to the path to your `proxmark3/liblua` directory.
1. In the amiitool directory run `./build.sh` and copy `build/libluamiibo.so` to the `proxmark3/client` directory.

To build the main proxmark code, go to the `proxmark3` directory and run `make`.
Then flash the proxmark3 by:

1. Unplugging the proxmark if it is plugged in
1. Plug the proxmark in while holding down its button
1. While continuing to hold the button, run `make flash-all`

Go to the `client` directory and run `./proxmark3 /dev/ttyACM0` (or other device path)
and `script run amiibo help` to list available commands.

Commands that perform cryptographic operations, such as `read`, require a keyfile for
amiitool at `amiitool_keys.bin` in the `proxmark3/client` directory.


NOTICE:
(2014-03-26)
This is now the official Proxmark repository!

INTRODUCTION:

The proxmark3 is a powerful general purpose RFID tool, the size of a deck
of cards, designed to snoop, listen and emulate everything from
Low Frequency (125kHz) to High Frequency (13.56MHz) tags.

This repository contains enough software, logic (for the FPGA), and design
documentation for the hardware that you could, at least in theory,
do something useful with a proxmark3.

RESOURCES:

   * This repository!
      https://github.com/Proxmark/proxmark3
      
   * The Wiki
      https://github.com/Proxmark/proxmark3/wiki
      
   * The GitHub page
      http://proxmark.github.io/proxmark3/
      
   * The Forum
      http://www.proxmark.org/forum
      
   * The IRC chanel
       irc.freenode.org #proxmark3
       -or-
       http://webchat.freenode.net/?channels=#proxmark3
       
   * The Homebrew formula repository
      https://github.com/Proxmark/homebrew-proxmark3
   
DEVELOPMENT:

The tools required to build  or run the project will vary depending on
your operating system. Please refer to the Wiki for details.

   * https://github.com/Proxmark/proxmark3/wiki

OBTAINING HARDWARE:

The Proxmark 3 is available for purchase (assembled and tested) from the
following locations:

   * http://proxmark3.com/
   * http://www.xfpga.com/
   * http://radiowar.taobao.com/
   * http://www.elechouse.com/
   * https://lab401.com/

Most of the ultra-low-volume contract assemblers could put
something like this together with a reasonable yield. A run of around
a dozen units is probably cost-effective. The BOM includes (possibly-
outdated) component pricing, and everything is available from Digikey
and the usual distributors.

If you've never assembled a modern circuit board by hand, then this is
not a good place to start. Some of the components (e.g. the crystals)
must not be assembled with a soldering iron, and require hot air.

The schematics are included; the component values given are not
necessarily correct for all situations, but it should be possible to do
nearly anything you would want with appropriate population options.

The printed circuit board artwork is also available, as Gerbers and an
Excellon drill file.


LICENSING:

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA


Jonathan Westhues
user jwesthues, at host cq.cx

May 2007, Cambridge MA
