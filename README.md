# From Windows to run flex in Linux (subsystem linux)

1) Download & Install VirtualBox for Linux Hosts (https://www.virtualbox.org/wiki/Linux_Downloads)
2) Download .ISO file linux (I recommend this version for the first time user in linux: https://linuxmint.com/edition.php?id=267)
3) You have to enable your virtualization (SVM mode) in Bios by restarting your device. (https://www.youtube.com/watch?v=Ub3I14BwODU)
4) Complete the setting of oracle VM (https://www.youtube.com/watch?v=wX75Z-4MEoM&t=1391s)
5) Run the linux, run the terminal
6) Follow the instructions:
7) sudo apt install vim (press y while asked)
8) sudo apt-get install libc6-dev (press y while asked)
9) sudo apt-install flex-old (press y while asked)
10) cd ~/Desktop (to see live what you create)
11) vim file_name.l (press Insert button to enable writing)
%%
[0-9]+ {printf("int");}
%%
press Insert button to stop writing 
press Esc to stop writing
press Shift + : and then wq (to save and exit)
lex file_name.l (create lex.yy.c file)
gcc lex.yy.c -lfl (create .out file and require: sudo apt-install flex-old libc6-dev)
./a.out (to run a.out file)
ctrl+D to exit from a.out file
