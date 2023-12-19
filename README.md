# PySide2 Standalone Package for NVIDIA-Jetson-Nano

If you're looking to build GUIs with PySide2 for Qt 5.15.10 on Jetson Nano, Then follow the steps:

1. Install Pre-requisites

   `sudo apt-get install libxcb-xinput0`
2. Install Python3.7 using

   `sudo apt install python3.7`
3. Install pip using

   `sudo apt-get install python3-pip`
4. Clone the Repository using

   `git clone https://github.com/achuthaperumal/PySide2-NVIDIA-Jetson-Nano.git && cd PySide2-NVIDIA-Jetson-Nano`
   
5. Install Shiboken

   `python3.7 -m pip install ./shiboken2-5.15.10-5.15.10-cp37-cp37m-linux_aarch64.whl`
6. Install PySide2 with Pip

    `python3.7 -m pip install ./PySide2-5.15.10-5.15.10-cp37-cp37m-linux_aarch64.whl`


>**Note:** This wheel file is built as standalone package meaning you do not need to install Qt5 seperately. Since opencv has an inbuilt Qt and it interferes with this version, you have to install opencv-headless using `pip uninstall opencv-python && pip install opencv-python-headless`

---

In case you come across any error regarding "unable to initialize platform plugin xcb..."

1. Set Qt plugins in Debug mode
   `export QT_DEBUG_PLUGINS=1`
   
2. Now run your program and look for errors in the console.
   
3. Try to fix the errors by installing the missing packages.
   
