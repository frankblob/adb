# Adblocking - ads, YouTube and unnecessary Google hosts
### Trimmed lists for blocking ads and trackers (including, to some extent, Youtube video ads and unnecessary Google hosts), with a primary focus on US, Western Europe and Scandinavia (Denmark and Norway, in particular).

**General purpose list for blocking ads, trackers and bad places (~16.000 hosts):** [erx](https://github.com/frankblob/adb/raw/master/erx.conf) **or** [erx0](https://github.com/frankblob/adb/raw/master/erx0), depending on the format you want.

I use this list on my Ubiquiti ER-X EdgeRouter. 

## How-to
To apply on your EdgeRouter (or dnsmasq-based router/server), do this:

1. SSH into your server/box/EdgeRouter
2. #> sudo su
3. #> cd /etc/dnsmasq.d     
4a. #> curl -O https://raw.githubusercontent.com/frankblob/adb/master/erx.conf     
4b. #> curl -O https://raw.githubusercontent.com/frankblob/adb/master/testing.conf (optional)    
5. #> service dnsmasq restart

## Do it yourself
You can compose your own lists and add to or replace the above ones. Simply create a file named "whatever" + ".conf" and copy/save it to /etc/dnsmasq.d/, with lines of hosts you wish to block, formatted like this in:

1. "address=/" + "HOST/domain" + "/0.0.0.0" 
2. Do NOT add URLs, like "server.com/monetize/tracking" - only "server.com" or "mads.trackercorp.com"!

### How do you modify and reformat lists?
For search and replace, formatting, reformatting and general text editing of adblocker lists, I use [Pinetools](http://pinetools.com/c-text-lists/) (online and free), since it readily accepts dumps of even large lists. If you need to use regex, I often use [regex101](https://regex101.com/) for real-time checking before applying my intended list editing.

### I have additions, changes or suggestions!
Emails and pull requests are very welcome.

Cheers!
