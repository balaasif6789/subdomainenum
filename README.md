# subdomainenum




Bash script for automated subdomain enumeration

for domains in $(cat domainlist.txt); do python sublist3r.py -d $domains -b -t 50 -o $domains.txt ; done

Tool for subdomain takeover currently using until the other work

https://github.com/antichown/subdomain-takeover


Bash script for automated subdomain takeover

for domains in $(ls ../Sublist3r/*.*.txt |sed 's/\.txt//'| cut -d "/" -f 3 ); do python takeover.py -d $domains -w ../Sublist3r/$domains.txt ; done  >>takeover


<b>Using amass for subdomain enumeration </b>
 
 ./amass -d google.com -o outputfile

The above command can be used with the for loop command 


<b>checking for ports open from the subdomains gathered by amass </b>

Using aquatone :  https://github.com/michenriksen/aquatone <br>
Aquatone.exe is available for windows


$ cat hosts.txt | aquatone -ports 80,443,3000,3001
Aquatone also supports aliases of built-in port lists to make it easier for you:

small: 80, 443
medium: 80, 443, 8000, 8080, 8443 (same as default)
large: 80, 81, 443, 591, 2082, 2087, 2095, 2096, 3000, 8000, 8001, 8008, 8080, 8083, 8443, 8834, 8888
xlarge: 80, 81, 300, 443, 591, 593, 832, 981, 1010, 1311, 2082, 2087, 2095, 2096, 2480, 3000, 3128, 3333, 4243, 4567, 4711, 4712, 4993, 5000, 5104, 5108, 5800, 6543, 7000, 7396, 7474, 8000, 8001, 8008, 8014, 8042, 8069, 8080, 8081, 8088, 8090, 8091, 8118, 8123, 8172, 8222, 8243, 8280, 8281, 8333, 8443, 8500, 8834, 8880, 8888, 8983, 9000, 9043, 9060, 9080, 9090, 9091, 9200, 9443, 9800, 9981, 12443, 16080, 18091, 18092, 20720, 28017
Example:

$ cat hosts.txt | aquatone -ports large

<b><i>PS G:\Security tools\aquatone_windows_amd64_1.7.0> cat G:\Bugbounty\2019\facebook-domains.txt | .\aquatone.exe -ports la
rge




<b>Links: </b>
https://blog.appsecco.com/a-penetration-testers-guide-to-sub-domain-enumeration-7d842d5570f6<br>
https://pentester.land/cheatsheets/2018/11/14/subdomains-enumeration-cheatsheet.html<br>
https://www.sjoerdlangkemper.nl/2018/06/20/discovering-subdomains/ <br>
 

