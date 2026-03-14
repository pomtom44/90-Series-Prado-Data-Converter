# 90-Series-Prado-Data-Converter
This is currently a work in progress
I'll update as i go, and will update this header once I have a working version

The sources for this project are<br>
https://www.drive2.com/l/7650414/<br>
and<br>
https://github.com/hyperion11/toyota-obd-1<br>

This is not a log of my trials and errors, this is just the final findings.<br>
You may need to adjust your own to get it to work on your prado

First you need a old ODB1 connector<br>
There are plenty online, just make sure you get one that fits and has all the required connectors
<img width="1103" height="814" alt="image" src="https://github.com/user-attachments/assets/c5409f6d-71b0-44f3-8d90-e2adb496ff70" />

You then want to find which cable is pins:<br>
VF1, E1 and TE2
<img width="300" height="188" alt="image" src="https://github.com/user-attachments/assets/97b651ce-0415-4180-92aa-6c015a3cbf74" />

T2 or TE2 and E1 both need to go to ground<br>
VF1 goes to your data in pin (In my case D2)<br>
You also need to ground D2 to ground via a 1.5-3.3 nF capacitor

I then captured the raw bit stream from the output and ran it through AI to take what data already was found, and what other data we could pull out of the data stream and have complied the arduino sketch with these findings
I have tried to comment the script the best I can to make it easy to follow what is going on.
