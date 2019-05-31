# subdomainenum




Bash script for automated subdomain enumeration

for domains in $(cat domainlist.txt); do python sublist3r.py -d $domains -b -t 50 -o $domains.txt ; done

Tool for subdomain takeover currently using until the other work

https://github.com/antichown/subdomain-takeover


Bash script for automated subdomain takeover

for domains in $(ls ../Sublist3r/*.*.txt |sed 's/\.txt//'| cut -d "/" -f 3 ); do python takeover.py -d $domains -w ../Sublist3r/$domains.txt ; done  >>takeover


<b>Using amass for subdomain enumeration <br>
 ./amass -d google.com -o outputfile

The above command can be used with the for loop command 


<b>checking for ports open from the subdomains gathered by amass 

Using aquatone :  https://github.com/michenriksen/aquatone <br>
Aquatone.exe is available for windows

<b><i>PS G:\Security tools\aquatone_windows_amd64_1.7.0> cat G:\Bugbounty\2019\facebook-domains.txt | .\aquatone.exe -ports la
rge

