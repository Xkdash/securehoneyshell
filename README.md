# SSH Honey Kit

Python program to emulate an ssh server as a sort of psuedo-honeypot with some fun commands. It will accept all connections given any provided username/password for authentication.

Utilizes paramiko for the OpenSSH protocol. A generic private key is provided for convenience, although it can be substituted out for another key if desired.

## Server Setup

### Requirements

First install the SSH library "paramiko".
Link: https://pypi.org/project/paramiko/

`pip install paramiko`

Then install the IP to Geolocation library "Ip2geotools".
Link: https://pypi.org/project/ip2geotools/

`pip install ip2geotools`

Then simply run the file to start the server:

`sudo python3 ssh_server.py`

Note: sudo is simply needed to bind to port 22, although this can be easily changed if desired (it will present a generic OpenSSH banner/fingerprint to network scanners to find regardless of the port)

In case there is already a service running on the same port, stop it first.
`sudo service ssh stop`

Then try running the server

## Data Parsing

### Requirements

This additional tool is provided for parsing the logs obtained from the server.
For this you need to install "jupyter-notebook"
Link: https://jupyter.org/install

`python3 -m pip install --upgrade pip`
`python3 -m pip install jupyter`

Now install the free "geopy" library.
Link: https://pypi.org/project/geopy/

`pip install geopy`

Next install the google translator library "googletrans "to translate some country names.
Link: https://pypi.org/project/googletrans/

`pip install geopy`

Run jupyter notebook from the terminal or commandprompt
"jupyter-notebook"

Open the link mentioned in the terminal in web browser
Browse and open the "log_parser.ipynb"

## Live Threat Map : OpenLTM
This tool is required for plotting the intrusion activities on a world map in real time.
### Requirements
Download/clone the OpenLTM library from this link.
Link: https://github.com/Xkdash/OpenLTM
Open the LTM.py and change the path of the IP_logins.txt file as required.
Fore more instructions go to the OpenLTM repository.