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



 <b> https://stackoverflow.com/questions/51997893/separate-multiple-subdomains-into-all-possible-subdomain-combinations-using-bash </b>
 
