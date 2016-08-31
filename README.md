==========================
Subdomains Scanner v.1.0
==========================

Just another subdomains scanner, but using HEAD requests.

Questions? http://hackers.city


Usage
-----

    subdomainsScanner.py [-h] [-w WORDLIST] [-m THREADS] [-t TIMEOUT] domain

Required arguments:

    domain      specify a domain name (domain.com)

Optional arguments:

    -h  show this help message and exit
    -w  Path to wordlist file (default: wl.txt)
    -m  Threads for use (default: 10)
    -t  Timeout in second per request (default:10)


Requirements
-----
argparse, socket, os.path, threading, httplib, sys

Examples
-----

Subdomains scan with default options (wl.txt must exist)

    subdomainsScanner domain.com

Subdomains scan with own wordlist

    subdomainsScanner domain.com -w mywordlist.txt

Subdomains scan with own wordlist and timeout

    subdomainsScanner domain.com -w mywordlist.txt -t 30

Subdomains scan with own wordlist, 30 seconds timeout and 100 threads

    subdomainsScanner domain.com -w mywordlist.txt -t 30 -m 100

