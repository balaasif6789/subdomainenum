# subdomainenum

Tool for subdomain takeover currently using until the other work

https://github.com/antichown/subdomain-takeover


Bash script for automated subdomain enumeration

for domains in $(ls ../Sublist3r/*.*.txt |sed 's/\.txt//'| cut -d "/" -f 3 ); do python takeover.py -d $domains -w ../Sublist3r/$domains.txt ; done  >>takeover
