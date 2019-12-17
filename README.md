# SSH Honey Kit

Python program to emulate an ssh server as a sort of psuedo-honeypot with some fun commands. It will accept all connections given any provided username/password for authentication.

Utilizes paramiko for the OpenSSH protocol. A generic private key is provided for convenience, although it can be substituted out for another key if desired.

## Usage

### Requirements

First install the SSH library "paramiko".
Link: https://pypi.org/project/paramiko/

`pip install paramiko`

Then install the IP to Geolocation library "Ip2geotools".
Link: https://pypi.org/project/ip2geotools/

`pip install ip2geotools`

Then simply run the file to start the server:

`sudo python ssh_server.py`

Note: sudo is simply needed to bind to port 22, although this can be easily changed if desired (it will present a generic OpenSSH banner/fingerprint to network scanners to find regardless of the port)

In case there is already a service running on the same port, stop it first.
`sudo service ssh stop`

Then try running the server