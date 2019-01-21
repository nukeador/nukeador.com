---
ID: 1735
post_title: 'VPN Kill switch for Linux &#8211; Protect from VPN drops and DNS leaks'
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/06/07/2017/vpn-kill-switch-for-linux-protect-from-vpn-drops-and-dns-leaks/
published: true
post_date: 2017-07-06 19:43:31
---
This post is a follow-up from <a href="https://thetinhat.com/tutorials/misc/linux-vpn-drop-protection-firewall.html">the one posted at TheTinHat.com</a>

What we want to ensure is that:
<ul>
 	<li>We connect to our VPN and all traffic goes through it (including DNS).</li>
 	<li>If our VPN connection drops there is no leak and it reconnects automatically.</li>
 	<li>We can return to not using VPN safely.</li>
</ul>
We will use two scripts, <em>vpn-firewall.sh</em> and <em>vpn-off.sh</em>. Pleace them under your /home/user/bin folder or anywhere else. Make then executable with <code>chmod +x vpn-*</code>
<h3><a href="https://gist.github.com/nukeador/31d4cae15bc2c5c4789b12c197111ee3">vpn-firewall.sh</a></h3>
<script src="https://gist.github.com/nukeador/31d4cae15bc2c5c4789b12c197111ee3.js"></script>
<h3><a href="https://gist.github.com/nukeador/5748d486ba1f7586f40c7edcfafabe93">vpn-off.sh</a></h3>
<script src="https://gist.github.com/nukeador/5748d486ba1f7586f40c7edcfafabe93.js"></script>

Usage:
<ul>
 	<li>Make sure you have the <code>ufw</code> package installed.</li>
 	<li>Before opening any app, execute <em>vpn-firewall.sh</em> to connect to the vpn and set up the firewall. This script will monitor your connection and re-connect to VPN if it drops avoiding any leaks. You can stop monitoring using Ctrl + Z.</li>
 	<li>If you want to stop using VPN, stop monitoring by Ctrl +Z and execute <em>vpn-off.sh <strong>IMPORTANT:</strong> Make sure your close all apps first or list them under KILL_APPS on the vpn-off.sh script.
</em></li>
</ul>
If you want to run vpn-firewall.sh each time you open session, you can create a file vpn-firewall.desktop under <code>~/.config/autostart/</code> folder with the following content:

<code>[Desktop Entry]
Name=VPN Firewall autostart
Type=Application
NoDisplay=true
Exec=~/bin/vpn-firewall.sh</code>

<em>Note that this might not work for you since this script needs root access to modify Firewall rules.</em>