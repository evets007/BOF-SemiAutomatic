# BOF-SemiAutomatic
A python based semi-automatic buffer overflow exploit script 

# How to 

Step 1 : Edit the code and add remote address, remote port, command, listener IP and port. 

#Server response timeout, will be used to identify a crash.
timeout = 5
#Add vulnerable server's IP address and port to connect
addr = ('<IP address>',<PORT>)
#Add command to send prepended to the buffer, eg. 'TRUN .' for vulnserver.exe
cmd = "<COMMAND>"

Run '''python semi-win32.py fuzz '''

Step 2 - Follow the onscreen instructions and run mona to find the offset 

Update the correct EIP offset in the code

#Default starting EIP offset is 50, change to correct EIP offset after fuzz step
offset = 50  

Run '''python semi-win32.py badchars '''

Update the badchars in the code as you find them, rerun multiple times until mona shows no modified chars 

Step 3 - Update set the 'JMP ESP' address in the code 

Make sure your listener is running and run '''python semi-win32.py shell'''

 
# Testing 

Tested on TryHackMe labs - https://tryhackme.com/room/bufferoverflowprep - Thanks to Tib3rius

Tested on Brainpan.exe

Tested on vulnserver.exe (spiking done seperately)
