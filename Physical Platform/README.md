# Physical Platform
This folder includes all the codes for controlling and driving the rover. We are using the same robot built by [This](https://github.com/UofA-EEE-LAUS/3WD-omni-direction-rover-stepper/tree/master/Hardware%20Designs).\
You can find all the necessary codes for functioning and remoting the rover from PC. Feel free to try yourself!

## Communication Protocol
The rover units use UDP protocol through WiFi, since the Arduino MKR1000 has a built-in WiFi extension, to communicate with computer. We established a connection method through MATLAB since it would be easier for researchers to get access to the platform without redundant work in coding. \
You should first make sure the rover unit(s) and computer are under the same LAN. After the rover booting up, it works as a UDP server. On the control end, the MATLAB establish the UDP connection to rover unit(s) as a UDP client.\
The transmissing data is a String type data using "," to figure out each data parameter. Detail information can be found in the sample testing conde.
* If your're not familiar with Arduino UDP interface, you can check this [Sample](https://www.arduino.cc/en/Tutorial/UDPSendReceiveString) for more detail.
* If your're not familiar with MATLAB UDP interface, you can check this [Page](https://www.mathworks.com/help/instrument/udp.html)

## GUI
We also developed a MATLAB GUI for the purpose of easy command testing. You can find it under this [Folder](https://github.com/UofA-EEE-LAUS/3WD-omni-direction-rover-stepper/tree/master/Physical%20Platform/Rover_GUI)
