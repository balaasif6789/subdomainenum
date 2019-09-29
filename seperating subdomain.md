 root@ubuntu-s-1vcpu-1gb-nyc3-01:~/bugbounty# awk '
        {
                gsub( "^.*://", "", $1 );      # ditch the http://  ftp:// etc
                n = split( $1, a, "." );
                if( length( a[n] ) == 2 )       # assuming all two character top level domains are country codes
                        printf( "%s.%s.%s\n", a[n-2], a[n-1], a[n] );
                else
                        printf( "%s.%s\n",  a[n-1], a[n] );
        }
' domains.txt | sort -u >>subdomain
