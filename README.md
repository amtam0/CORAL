# Posenet Installation

Requirements:
- raspberry pi 3 (4 is best) (optional coral usb accelerator)
- python 3.7

Setuptools of Raspbian in Linux
- cfdisk (repartition sd card)
- etcher (flash drive)  
  - image [link](ttps://www.raspberrypi.org/downloads/raspbian/)
  - open Etcher and Flash !
- insert sd card
- Start Raspberry pi and follow installation instructions
```
sudo apt-get update
sudo apt-get upgrade
reboot
```
pip3 install virtualenv

python3 -m venv coralenv
source coralenv/bin/activate

### Setup Coral
support [link](https://coral.ai/docs/accelerator/get-started/#on-linux)
```
echo "deb https://packages.cloud.google.com/apt coral-edgetpu-stable main" | sudo tee /etc/apt/sources.list.d/coral-edgetpu.list
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get install libedgetpu1-std
pip3 install https://dl.google.com/coral/python/tflite_runtime-2.1.0.post1-cp37-cp37m-linux_armv7l.whl
sudo apt-get install libatlas-base-dev
pip3 install -r requirements.txt
```
Link edgetpu package
```
cd coralenv/lib/python3.7/site-packages/
ln -s /usr/lib/python3/dist-packages/edgetpu/ edgetpu
```

<<<<<<< HEAD

=======
>>>>>>> 39eb7957c21978f95c0bbbbeeb58fd5c9da2fd22
source tellocv-env/bin/activate

bash get_pi_requirements.sh

sudo apt-get install -y pkg-config libavformat-dev libavcodec-dev libavdevice-dev libavutil-dev libswscale-dev libavresample-dev libavfilter-de

<<<<<<< HEAD
=======
pip3 install --upgrade setuptools

>>>>>>> 39eb7957c21978f95c0bbbbeeb58fd5c9da2fd22
pip3 install -r requirements.txt

git clone https://github.com/hanyazou/TelloPy

cd TelloPy

python3 setup.py bdist_wheel

pip3 install dist/tellopy-*.dev*.whl --upgrade

# Tellocv tracker
Tracking code for the Tello drone. It uses opencv and tellopy to identify a ball in the scene and then send commands to the drone.
It is written in python3 and 

## Installation (not used)
You need to have opencv installed and the following python modules for the tello and cv2:
apt

```
sudo apt install sudo libopencv-dev python3-opencv
```

pip3:

```
sudo pip3 install imutils pynput
```

you need to build tellopy from source as the :
Or install from the source code.
```
git clone https://github.com/hanyazou/TelloPy
cd TelloPy
python setup.py bdist_wheel
pip install dist/tellopy-*.dev*.whl --upgrade
```

# Flight rules
- Although tellos are very safe to operate, wear safety glasses as an added precaution
- Do not fly over people
- Memorize the controls *before* taking off
- Always be ready to land the drone (backspace)
- If the program crashes restart it to regain control
- if drone is going out of control just hit it and it will turn off.

## Tello lights

- flashing blue - charging
- solid blue - charged
- flashing purple - booting up
- flashing yellow fast - wifi network set up, waiting for connection
- flashing yellow - User connected

## Recording a video
hit r to record a video it is output to <home>/Pictures
