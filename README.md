# multi-project
You need to use esp32cam library from github for this project. You need to use git clone to synchronize this library to your computer because ZIP downloading is not suppported for Adruino library.

Installation
1. Clone this repository under `$HOME/Arduino/libraries` directory.
2. Then you can add #include <esp32cam.h> to your sketch.
3. Tools->Board menu, select ESP32 Wrover Module to enable 4MB external PSRAM.
4. Check out with your sketch.

Then you need to download python from https://www.python.org/ , you need to download pip to download some libraries of python like Numpy, OpenCV, pyzbar. Open the command prompt.
1. type: pip install numpy and press enter.
2. type: pip install opencv-python and press enter.
3. type: pip install pyzbar and press enter, close the command prompt.

After setup library for your Adruino and python. Before uploading the code you have to make a small change to the code. Open `qrcode.ino` change the SSID and password variable and in accordance with your WiFi network. Then verifying and uploading your code to ESP32 Module. But during uploading, you have to follow few steps every time.
- Make sure the IO0 pin is shorted with the ground when you have pressed the upload button.
- If you see the dots and dashes while uploading press the reset button immediately.
- Once the code is uploaded, remove the I01 pin shorting with Ground and press the reset button once again.
- If the output is the Serial monitor is still not there then press the reset button again.

Next step, you open `qrcode.py` by IDLE code editor or any other python code editor. Change the IP address copied from Arduino Serial Monitor and update it in the URL variable in the above code. Then save the code and run it. 

You see in `live transmission` window appears data of QR Code.
