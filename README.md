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
sudo apt-get install python3-edgetpu
pip3 install -r requirements.txt
```
### export path of edgetpu package
```
cd coralenv/lib/python3.7/site-packages/
ln -s /usr/lib/python3/dist-packages/edgetpu/ edgetpu
```
### Run
```
python pose_camera.py
```

### Install opencv 3+ support [Edgeelectronics-link](https://github.com/EdjeElectronics/TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi/blob/master/get_pi_requirements.sh)

remove unecessary package
```
sudo apt-get purge wolfram-engine
sudo apt-get purge libreoffice*
sudo apt-get clean
sudo apt-get autoremove
```

```
bash opencv.sh
```


=======
>>>>>>> 39eb7957c21978f95c0bbbbeeb58fd5c9da2fd22
```=======
source tellocv-env/bin/activate
bash get_pi_requirements.sh
sudo apt-get install -y pkg-config libavformat-dev libavcodec-dev libavdevice-dev libavutil-dev libswscale-dev libavresample-dev libavfilter-de
```
=======

<<<<<<< HEAD
```
sudo apt install libavdevice-dev libavfilter-dev #needed for av
pip3 install --upgrade setuptools
pip3 install -r requirements.txt
git clone https://github.com/hanyazou/TelloPy
cd TelloPy
python3 setup.py bdist_wheel
pip3 install dist/tellopy-*.dev*.whl --upgrade
```
