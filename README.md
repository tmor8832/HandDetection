# HandDetection
Custom hand detection model trained to detect a fist, peace sign and finger gun.

![ezgif com-gif-maker](https://user-images.githubusercontent.com/64171887/196004574-6b8a386a-e04b-452b-8d85-2fa6c18e552c.gif)

This can be easily deployed on a raspberry pi by following the below guide. You can also git clone this repo and get going too.

# Tensorflow Object Detection Walkthrough with Raspberry Pi
<p>The following repository will allow you to leverage Tensorflow Object Detection models that have been converted to TFLite on a Raspberry Pi.
## Steps
<b>Step 1.</b> Walk through the object detection tutorial by Nick Nochnack and generate the TFlite files. The important one is the .tflite file. https://github.com/nicknochnack/TFODCourse
<br/><br/>
<b>Step 2.</b> Clone this repository onto your Raspberry Pi or copy it from a machine using RDP.
<b><br/>Step 3.</b>Install the required dependencies onto your Raspberry Pi
<pre>
pip3 install opencv-python 
sudo apt-get install libcblas-dev
sudo apt-get install libhdf5-dev
sudo apt-get install libhdf5-serial-dev
sudo apt-get install libatlas-base-dev
sudo apt-get install libjasper-dev 
sudo apt-get install libqtgui4 
sudo apt-get install libqt4-testv
echo "deb https://packages.cloud.google.com/apt coral-edgetpu-stable main" | sudo tee /etc/apt/sources.list.d/coral-edgetpu.list
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get install python3-tflite-runtime OR if on normal linux machine python3 -m pip install tflite-runtime
</pre>
<b>Step 4.</b> Copy your detect.tflite model into the same repository and update the labels.txt file to represent your labels. 
<br/>
<b>Step 5.</b> Run real time detections using the detect.py script
<pre>python3 detect.py</pre>
<br/>
