# unix-notes
Various useful things

## ping
- http proxy proxy for just that
- https://superuser.com/questions/175428/how-to-ping-when-behind-a-proxy#:~:text=ping%20needs%20a%20direct%20network,access%20to%20the%20IP%20protocol.
- sudo apt install httping

## awk file extensions
find . -name "*.csv" -print0 | xargs -0 awk -F, 'NR > 1 {split($1, a, "."); if (length(a) > 1) print a[length(a)]}' | sort | uniq -c
