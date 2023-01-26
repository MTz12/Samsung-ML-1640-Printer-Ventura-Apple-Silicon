# How install Samsung ML-1640 Printer driver for macOS Ventura and Apple Silicon

This example shows how to install the printer driver for ML-1640 on macOS Ventura.

- clone the provided files
````
git clone 
````

- copy the two files (``*qpdl``) located in the ``/Samsung/UPD/Filters`` folder to
````
/Library/Printers/Samsung/UPD/Filters/
````

- copy the ``ML-1640`` folder to
````
/Library/Printers/Samsung/
````

copy the ``Samsung ML-1640 Series.gz`` file to
````
/Library/Printers/PPDs/Contents/Resources/
````

open a terminal and execute the following commands
````
sudo chmod +x /Library/Printers/PPDs/Contents/Resources/Samsung\ ML-1640\ Series.gz
sudo chown root:admin /Library/Printers/PPDs/Contents/Resources/Samsung\ ML-1640\ Series.gz
````

- plug in the ML-1640 printer
- open system settings
- go to printers & scanners
- click on **add printer**
- choose **Samsung ML-1640, Splix V. 2.0.0** as driver
- start printing :)