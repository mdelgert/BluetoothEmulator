# C Instructions
btferret.c
btlib.c
btlib.h
devices.txt

# COMPILE
gcc btferret.c btlib.c -o btferret

# Run C
gcc keyboard.c btlib.c -o keyboard
sudo ./keyboard

# Python Instructions
sudo apt-get install python3-setuptools python3-dev
btlib.c
btlib.h
btfpython.c
btfpy.py
btferret.py
devices.txt
python3 btfpy.py build

# Run Python
sudo python3 keyboard.py
