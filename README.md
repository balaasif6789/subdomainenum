# subdomainenum




Bash script for automated subdomain enumeration

for domains in $(cat domainlist.txt); do python sublist3r.py -d $domains -b -t 50 -o $domains.txt ; done

Tool for subdomain takeover currently using until the other work

https://github.com/antichown/subdomain-takeover


Bash script for automated subdomain takeover

for domains in $(ls ../Sublist3r/*.*.txt |sed 's/\.txt//'| cut -d "/" -f 3 ); do python takeover.py -d $domains -w ../Sublist3r/$domains.txt ; done  >>takeover
