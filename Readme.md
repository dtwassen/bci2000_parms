BCI2000 Parameter Files
=======================

This is a collection of parameter files for [BCI2000](http://bci2000.org/).

P300 Signal Processing
----------------------

Signal acquisition parameters for the g.tec 
[g.USBamp](http://gtec.at/Products/Hardware-and-Accessories/g.USBamp-Specs-Features) 
and Emotiv's [EPOC](http://emotiv.com/store/hardware/epoc-bci/epoc-neuroheadset/).
Additional information on the parameters can be found in the BCI2000 wiki for the
[gUSBampADC](http://www.bci2000.org/wiki/index.php/User_Reference:gUSBampADC) and 
the [Contributions/Emotiv](http://www.bci2000.org/wiki/index.php/Contributions:Emotiv).

The setup assumes an external monitor with a resolution of 1440x900 pixels and a laptop display of the same resolution.

### g.USBamp

* 16 Channels
* F3 Fz F4 T7 C3 Cz C4 T8 Cp3 Cp4 P3 Pz P4 O7 Oz O8 Positions
* 512 Hz Sampling Rate
* 4 Sample Block Size
* 0.5 Source Channel Gain
* Butterworth Band-Pass Filter
* 0.1 Hz High-Pass Filter
* 30 Hz Low-Pass Filter
* 8 Band-Pass Filter Order
* Chebyshev Notch Filter
* 48 Hz Notch High-Pass Filter
* 52 Hz Notch Low-Pass Filter
* 4 Notch-Filter Order

### EPOC

* 14 Channels
* AF3 F7 F3 FC5 T7 P7 O1 O2 P8 T8 FC6 F4 F8 AF4 Positions
* 128 Hz Sampling Rate
* 4 Sample Block Size
* 1.0 Source Channel Gain
* 0.1 Hz High-Pass Filter
* 30 Hz Low-Pass Filter
* 50 Hz Notch Filter

Usage
-----

All parameter files have been tested and used with 
BCI2000 contrib version 3.0.3. Hardware were g.USBamp 
v3 with driver V.3.10.01 and EPOC with Research SDK v1.0.0.5.
The operating system was WinXP 32bit.

Execute the 'BCI2000Launcher' and select 'gUSBampSource' as 
signal source, 'P3SignalProcessing' for processing, 'P3Speller' as application, 
and one of the parameter files 'gtec.prm' or 'emotiv.prm'.

Alternatively, create a batch file within the 'prog' directory.

	start Operator
	start gUSBampSource AUTOSTART 127.0.0.1
	start P3SignalProcessing AUTOSTART 127.0.0.1
	start P3Speller AUTOSTART 127.0.0.1 
