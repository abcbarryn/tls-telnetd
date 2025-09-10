This contains the setup to run stunnel on Linux using xinetd to provide a TLS wrapped telnetd. You can use this with the TLS telnet client at https://github.com/abcbarryn/telnet-tls

To instell, install stunnel for your Linux distribution, generate a certificate and key in PEM formt and place it in the file /etc/ssl/certs/stunnel.pem, then copy the two files /etc/in.telnetd and /etc/xinetd.d/telnets to your server and send a SIG-HUP to your xinetd server with the command:
killall -1 /usr/sbin/xinetd

To disable the telnets service, edit /etc/xinetd.d/telnets and change disable=yes and killall -1 /usr/sbin/xinetd

To re-enable the telnets service, edit /etc/xinetd.d/telnets and change disable=no and killall -1 /usr/sbin/xinetd
