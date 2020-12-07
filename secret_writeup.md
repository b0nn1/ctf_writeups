
Foren 
Secret:
challenge.zip is given but its header is broken and password can be seen in metadata,
so edit the header same as 50 4B 03 04
so now after extracting the zip 
you will get one more zip file file.zip
use 7z to extract this zip with given password and theres 
the flag
use 7z with password h4ckTh35t3R30tyP35

---------------------------------------------------------------------------------------------------------------------------------------------------------------

Foren
Invisible:
See file.txt 
its snow stegenography 
for windows just you have to do SNOW.exe -d file.txt
you will see morsecode 
decode that morsecode and you will get flag


---------------------------------------------------------------------------------------------------------------------------------------------------------------
Foren :
Shark on the wire:
flag was on the tcp stream:


---------------------------------------------------------------------------------------------------------------------------------------------------------------
Foren:

TCP stream 16
export as raw and then zbarimg QR

---------------------------------------------------------------------------------------------------------------------------------------------------------------
Pwn:
Connect
nc 34.72.218.129 1111  
cat flag.txt

--------------------------------------------------------------------------------------------------------------------------------------------------------------
Pwn :
Damez
use strings command

---------------------------------------------------------------------------------------------------------------------------------------------------------------
Web : Door 

See the Source code its says page is parameter
So type ?page= 
after type 1 2 3 4 5 a b c i wass see that that is reflected on page 
So i type etc/passwd 
then got a flag

---------------------------------------------------------------------------------------------------------------------------------------------------------------
Web : Machine
Just check /robots.txt for flag 

--------------------------------------------------------------------------------------------------------------------------------------------------------------

revers:
Just run it:
just run the binary.

---------------------------------------------------------------------------------------------------------------------------------------------------------------
Osint: Findme
they provided us a hash encoded text which is the username for a social media account,
decode it with cyberchef (https://gchq.github.io/CyberChef)
and then search the username in https://www.namecheckr.com/
and get the flag.

--------------------------------------------------------------------------------------------------------------------------------------------------------------






