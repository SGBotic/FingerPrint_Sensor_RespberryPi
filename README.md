FingerprintScannerRaspberryPi
-----------------------------

Fingerprint Scanner using serial (UART) on Raspberry Pi
These files are tested with Raspberry Pi 2 and 3 running Rasbian Jessie and python 3.
The serial port must be changed from serial console to serial control.

FingerPrint Sensor Wiring
-------------------------

   Vin (Red) = 3.3VDC
   Tx (Green) = GPIO15 (RXD0)
   Rx (White) = GPIO14 (TXD0)
   GND (Black) = Ground

Button connects to GPIO04 (pin 7)
Relay (Output) connects to GPIO21 (pin 40)


For FingerPrint sensor to work on Raspberry Pi 3 UART pin, you need to:
1. Disable serial console in raspi-config
2. Edit /boot/cmdline.txt to remove **console=serial0,115200*
3. Add **enable_uart=1** to /boot/config.txt

Usage
-----

   sudo python3 FPRunTest.py
