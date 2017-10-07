# .screenrc
My .screenrc file

How to protect a screen session with a password

Launch a new screen
Easily done :

$ screen

Encrypt a new password
screen provides a way to encrypt a password right from a screen session. In the following snippets, I assume the default screen key is A, as default.

hit ctrl A :password
enter the new password twice
Now, the encrypted password is in the screen clipboard. We need to retrieve it

Paste the crypted password
The key shortcut for pasting the clipboard is by default Ctrl-A ]

hit ctrl A ]
the encrypted password should be pasted in the console
Edit the screen configuration file
Copy the encrypted password and paste it in ~/.screenrc (or whatever your screen configuration file is)

add this line, with your encrypted password
password VGdGzMopF
Restart screen
You need to restart screen to take the password in account. Now, next time a screen is reattached, the password will be prompted.

mxr@delta:~$ screen -rd
Screen password:
