# BOF-SemiAutomatic
A python based semi-automatic buffer overflow exploit script 

# How to 

Edit the code and add remote address, remote port, command, listener IP and port. 

'''python semi-win32.py fuzz '''

Follow the onscreen instructions 

Update code with the EIP offset and run 

'''python semi-win32.py badchars '''

Update the badchars in the code as you find them, rerun multiple times until mona shows no modified chars 

Update set the 'JMP ESP' address in the code 

Run the listener and run

'''python semi-win32.py shell'''

 
# Testing 

Tested on TryHackMe labs - https://tryhackme.com/room/bufferoverflowprep 

Tested on Brainpan

Tested on vulnserver.exe (spiking done seperately)
