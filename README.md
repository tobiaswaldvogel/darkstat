# darkstat-peers

This is a fork of https://unix4lyfe.org/darkstat/

## Enhancements in this fork
### Peer statistics
--peers activates gathering statistics instead of just a summary per port
as the port summary statistics are redundant with this you can deactivate
it with --no-ports
### Unit selection
To ease readbility You can switch now from between byte, kB, MB, GB and
automatic. Automatic is the highest unit, which still produces a tenth-part
### Scan for http host headers and TLS SNI
Most of the time reverse lookup of IPs is does not return very meaningful
names, in particular for large content providers. This enhancements scans
for HTTP requests and extracts the host name from there. As this only works
for unencrypted requests, the TLS SNI field is also evaluated. During the 
setup of a TLS connection a multi homed server needs to to know which
web-site will be requested, therefore usually the desired DNS name is
indicated in the TLS SNI field.

# Original description of the package
darkstat is a network statistics gatherer.

It sniffs packets on a specified interface, accumulates statistics, and
serves them up over HTTP.

See the "AUTHORS" file for credits, and who to e-mail when things break.
See the "LICENSE" file for an explanation of the source code licensing.
See the "INSTALL" file for installation instructions.
See the "darkstat.8" manual page for usage instructions.

If your system doesn't have enough copies of the full text of the GNU
General Public License already, we have provided another one in the
"COPYING.GPL" file.
