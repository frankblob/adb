# Adblocking - ads, trackers, malware and miners
### Trimmed list for blocking ads, trackers, malware and miners, with a primary focus on US, Western Europe and Scandinavia (Denmark and Norway, in particular). Optional wildcard blocking of .ru and .cn top-level domains available as add-on block list.

**General purpose list for blocking ads, trackers and bad places (~14.000 hosts):** [erx](https://github.com/frankblob/adb/raw/master/erx.conf) **or** [erx0](https://github.com/frankblob/adb/raw/master/erx0), depending on the format you want.

I use this list on my Ubiquiti ER-X EdgeRouter. 

## How-to
To apply on your EdgeRouter (or dnsmasq-based router/server), do this:

1. SSH into your server/box/EdgeRouter
2. #> sudo su
3. #> cd /etc/dnsmasq.d     
4. #> curl -O https://raw.githubusercontent.com/frankblob/adb/master/erx.conf     
5. #> curl -O https://raw.githubusercontent.com/frankblob/adb/master/testing.conf (*optional*)    
6. #> curl -O https://raw.githubusercontent.com/frankblob/adb/master/wildcards.conf (*optional*)    
7. #> service dnsmasq restart

## Do it yourself
You can compose your own lists and add to or replace the above ones. Simply create a file named "whatever" + ".conf" and copy/save it to /etc/dnsmasq.d/, with lines of hosts you wish to block, formatted like this in:

1. "address=/" + "HOST/domain" + "/0.0.0.0" 
2. Do NOT add URLs, like "server.com/monetize/tracking" - only "server.com" or "mads.trackercorp.com"!

### How do you modify and reformat lists?
For search and replace, formatting, reformatting and general text editing of adblocker lists, I use [Pinetools](http://pinetools.com/c-text-lists/) (online and free), since it readily accepts dumps of even very large lists. If you need to use regex, I often use [regex101](https://regex101.com/) for real-time checking before applying my intended list editing and for removing a specified list from another, larger list, I use [alphabetizer](https://alphabetizer.flap.tv/remove-one-list-from-another.php). 

### I have additions, changes or suggestions!
Emails and pull requests are very welcome.

Cheers!
