This is a simple TCP proxy written in Perl that uses IO::Socket::INET and
IO::Select abstractions to create an evented (asynchronous, on select() call
based) server.

It was written by Peteris Krumins (peter@catonmat.net).
His blog is at http://www.catonmat.net  --  good coders code, great reuse.

Currently it's written only for demonstrative purposes for my article "Turn
any Linux computer into SOCKS5 proxy in one command," which can be read here:

    http://www.catonmat.net/blog/linux-socks5-proxy

------------------------------------------------------------------------------

The ports are currently hard coded in the source code. The proxy tunnels all
connections from 0.0.0.0:1080 to localhost:55555.

The idea is that if you start a ssh socks5 proxy via

    ssh -N -D 55555 localhost

Then no one can access this proxy, except people on localhost, which is of no
good.

This Perl program opens up this ssh socks5 proxy for everyone.

Please see the article for more details:

    http://www.catonmat.net/blog/linux-socks5-proxy


------------------------------------------------------------------------------

Happy proxying!

Sincerely,
Peteris Krumins
http://www.catonmat.net

