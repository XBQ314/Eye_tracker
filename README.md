# Interactive device based on PYNQ-Z2 using eye movement principle

This repository contains various source files of the eye tracking device we made. The eye tracking device uses the OV5640 camera. The programmable logic device (PL) part of the PYNQ-Z2 development board realizes the parallel acceleration of the pupil extraction algorithm. A visual interface is designed on the PS side and the extracted pupil center coordinates are passed through the serial port. Send it out. At present, we use this coordinate to control the yaw angle of the UAV, and explore the possibility of using this eye tracking device.

![general_picture](E:\为了让桌面看上去更干净的文件夹\文档\SRTP事件\PLD\国赛要交的文件\Eye_tracker\general_picture.jpg)

# Folder Structure

+ PL_design

  + hls_src: Contains the adaptive threshold binarization algorithm (OTSU) designed using the vivadohls advanced synthesis tool, with the binarization algorithm that can set the threshold, and the workflow that contains several corrosion expansion algorithms
  + vivado_sys: hardware design in Vivado, including HDMI display and the image hardware acceleration algorithm

+ PS_design

  Including the OV5640 config file and the file that finally runs in the jupyter notebook

  # Environment for this project

  1. Vivado `2018.3`
  2. PYNQ-Z2 board with `image v2.4`
  3. A web browser (eg. Chrome) or IDE supporting `Jupyter Notebook`



