Blind XSS via Burpsuite Match and Replace:-

Save this file as json format and go to:-

https://github.com/emadshanab/Blind-XSS-burp-match-and-replace

Or use this repo to generate your json file:- by @fasthm00

https://github.com/Leoid/MatchandReplace

1:- Burpsuite - Proxy - Options - Match and Replace.

2:- Click on the option button and choose load options.

3:- Browse for the file and load it to Burpsuite.

4:- Import your scope and open the hosts on the browser via multiple url open firefox and chroom extension or use httpx to send the hosts file to Burpsite map

https://chrome.google.com/webstore/detail/open-multiple-urls/oifijhaokejakekmnjmphonojcfkpbbh?hl=en-US

https://addons.mozilla.org/en-US/firefox/addon/open-multiple-urls/

httpx -l hosts.txt -threads 100 -http-proxy http://127.0.0.1:8080

5:- You will notice that the blind xss is persent on every request.

6:- Run burpspider and gospider to get more endpoints.

If you do not have a xsshunter account you can register one and make it short like 2 letters or 4:-

https://xsshunter.com/

Finally :- Do not forget to change my blind xss payload with your payload.

Good luck.
