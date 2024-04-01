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