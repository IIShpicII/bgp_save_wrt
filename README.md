#LICENSE
MIT License

Copyright (c) 2024 Andrevich

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

# bgp_save_wrt
outline-bgp-install-wrt
OpenWRT /bin/sh script to install Outline (Shadowsocks) + bird2 BGP Client for Antifilter.download with xjasonlyu/tun2socks

How to use:
First, get the script and make it executable:

cd /tmp
wget https://raw.githubusercontent.com/1andrevich/outline-bgp-install-wrt/main/install_outline.sh -O install_outline.sh
chmod +x install_outline.sh
Check if you have kmod-tun, bird2c and ip-full installed, if not run:

opkg update
opkg install kmod-tun ip-full bird2c
Then run the script: You'll need at least 10 MiB of free space on /

./install_outline.sh
You'll be asked for:

Outline (Shadowsocks) config in "ss://base64coded@HOST:PORT" format
If you don't have enough free space on / , you can install executable to RAM (You'll need up to 35 MiB of RAM):

cd /tmp
wget https://raw.githubusercontent.com/1andrevich/outline-bgp-install-wrt/main/install_outline_ram.sh -O install_outline_ram.sh
chmod +x install_outline_ram.sh
./install_outline_ram.sh
