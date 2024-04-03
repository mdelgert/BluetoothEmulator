https://tailcall.net/posts/bluetooth-keyboard/
https://gist.github.com/HeadHodge/2d3dc6dc2dce03cf82f61d8231e88144

sudo dbus-send --system --print-reply --dest=org.bluez /org/bluez org.freedesktop.DBus.Introspectable.Introspect
sudo systemctl daemon-reload
sudo systemctl restart bluetooth
ps aux | grep bluetoothd
sudo python3 bluetooth_server.py

sudo apt install python3-pip
sudo apt-get install python3-venv
python3 -m venv venv
source venv/bin/activate

https://stackoverflow.com/questions/56123942/pip-failed-to-install-dbus-python
https://stackoverflow.com/questions/13365697/install-python-dbus-in-virtualenv
https://stackoverflow.com/questions/71867578/no-module-named-dbus-i-already-have-that-raspbian
sudo apt-cache search dbus-1
sudo apt install libdbus-1-3 libdbus-1-dev
sudo apt install libdbus-glib-1-dev libdbus-1-dev
pip install dbus-python
pip install dbus-next

https://medium.com/snapp-embedded/interfacing-raspberry-pi-sensors-with-dart-and-flutter-using-d-bus-5203ceee1d9a
sudo apt-get install dbus python3-dbus python3-pip
#sudo apt-get install libdbus-1-dev #???
sudo python3 bluetooth_server.py

Original idea taken from: http://yetanotherpointlesstechblog.blogspot.com/2016/04/emulating-bluetooth-keyboard-with.html
Rewritten and improved by: https://gist.github.com/ukBaz/a47e71e7b87fbc851b27cde7d1c0fcf0
https://tailcall.net/posts/bluetooth-keyboard/
https://gist.github.com/HeadHodge/2d3dc6dc2dce03cf82f61d8231e88144
https://github.com/sraodev/bluetooth-service-rfcomm-python