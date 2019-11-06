 <b> Extracting sub domains from a file containing domains and subdomains. The below code snippet extracts only the subdomains </b>
 
 awk '
        {
                gsub( "^.*://", "", $1 );      # ditch the http://  ftp:// etc
                n = split( $1, a, "." );
                if( length( a[n] ) == 2 )       # assuming all two character top level domains are country codes
                        printf( "%s.%s.%s\n", a[n-2], a[n-1], a[n] );
                else
                        printf( "%s.%s\n",  a[n-1], a[n] );
        }
' domains.txt | sort -u >>subdomain



 <b> https://stackoverflow.com/questions/51997893/separate-multiple-subdomains-into-all-possible-subdomain-combinations-using-bash <br> https://www.unix.com/shell-programming-and-scripting/143198-strip-subdomains-domains-list.html
</b>


<b>extracting subdomains using grep and regex </b><br>
cat test.txt |  grep  -E '(.+\.)+.+\..+$'

Note the + after the ). This ensures that only subdomains are extracted and not domains

<b>Extracting domains from a file using grep and regex </b>

cat test.txt |  grep  -E '(.+\.)*.+\..+$'

Note the * after ). This ensures that even domains are extracted and not just subdomains 
