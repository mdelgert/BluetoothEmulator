# Pairing Bluetooth Devices in Dual Boot with Linux Ubuntu and Windows 10/11
https://gist.github.com/madkoding/f3cfd3742546d5c99131fd19ca267fd4?permalink_comment_id=4473355
sudo hciconfig hci0 down
sudo bluemoon -A
sudo hciconfig hci0 up
sudo systemctl restart bluetooth.service

# How To Remove Stubborn Bluetooth Devices in Windows
https://www.tomshardware.com/how-to/remove-stubborn-bluetooth-devices-in-windows
https://www.systweak.com/blogs/cant-remove-bluetooth-device-on-windows/
https://arstechnica.com/civis/threads/windows-11-bluetooth-pairing-key-location.1484342/
https://github.com/petzval/btferret/issues/38

# Pairing keys location
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\BTHPORT\Parameters\Keys

# Keycodes
https://kbdlayout.info/kbduk
https://kbdlayout.info/kbdus

# Raspberry Pi 400 as a USB HID Keyboard & Mouse
https://github.com/Gadgetoid/pi400kb/tree/main

# PiKVM
https://github.com/search?q=repo%3Apikvm%2Fkvmd%20bluetooth&type=code
https://github.com/SySS-Research/bluetooth-keyboard-emulator
https://github.com/nutki/bt-keyboard-switcher

# Clear bluetooth cache
https://answers.microsoft.com/en-us/windows/forum/all/cant-connect-to-bluetooh-devices-in-anyway/479adf4b-5535-4393-9a99-8d59a9e3126a
https://answers.microsoft.com/en-us/windows/forum/all/how-to-delete-all-paired-bluetooth-devices/a766991f-0b8c-4a79-84ea-d579775fa7bf

```ps
Remove-Item -Path HKLM:\SYSTEM\CurrentControlSet\Services\BTHPORT\Parameters\Devices\* -Recurse
net stop bthserv
net start bthserv
```

# BluetoothEmulator
https://github.com/mx3030/btEmulator
https://github.com/4ndrej/hidclient
https://www.bluez.org/
https://github.com/IanHarvey/bluepy
https://github.com/bluez/bluez
https://forums.raspberrypi.com/viewtopic.php?t=343427
https://github.com/petzval/btferret
https://www.argenox.com/library/bluetooth-low-energy/using-raspberry-pi-ble/
https://stackoverflow.com/questions/69260562/what-language-libraries-best-for-ble-connectivity
https://stackoverflow.com/questions/69260562/what-language-libraries-best-for-ble-connectivity
https://github.com/4ndrej/hidclient
https://simpleble.readthedocs.io/en/latest/simpleble/usage.html

# Setup python not working
sudo apt update
sudo apt install python3-pip libglib2.0-dev
sudo apt install python3-venv
python3 -m venv venv
source venv/bin/activate
#pip install bleak
#pip install pygatt
#pip install pexpect
pip install bluepy

# Setup C
sudo apt install bluez
sudo apt install libbluetooth-dev

# Build
gcc -o bluetooth_keyboard bluetooth_keyboard.c -lbluetooth
chmod +x bluetooth_keyboard
./bluetooth_keyboard

# Scan
https://people.csail.mit.edu/albert/bluez-intro/c404.html
gcc -o simplescan simplescan.c -lbluetooth
./simplescan

gcc -o hidclient hidclient.c -lbluetooth
gcc -o virtual_keyboard virtual_keyboard.c -lbluetooth
gcc -o advertise advertise.c -lbluetooth
gcc -o bluetooth_advertiser bluetooth_advertiser.c -lbluetooth

gcc -o device device.c -lbluetooth

# Working with bluetooth
sudo hciconfig
sudo hciconfig hci0 down
sudo hciconfig hci0 up
sudo hcitool -i hci0 lescan

# Keyboards
https://kbdlayout.info/kbduk?arrangement=ISO105
https://kbdlayout.info/kbdus