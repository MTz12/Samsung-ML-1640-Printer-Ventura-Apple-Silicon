# How install Samsung ML-Series Printer driver for macOS Ventura and Apple Silicon

This example shows how to install a Samsung ML-Series printer driver on macOS Ventura.

- clone the provided files and change to ``ML-Series`` branch
````
git clone https://github.com/MTz12/Samsung-ML-1640-Printer-Ventura-Apple-Silicon.git
cd Samsung-ML-1640-Printer-Ventura-Apple-Silicon
git checkout ML-Series
````

- copy the two files (``*qpdl``) located in the ``/Samsung/UPD/Filters`` folder to
````
/Library/Printers/Samsung/UPD/Filters/
````

- change the ``xxxx`` within the ``ML-xxxx`` folder to your printer version number (folder name and .icns)
- copy the renamed ``ML-xxxx`` folder to
````
/Library/Printers/Samsung/
````

- select the ppd file suitable for your Samsung printer from the ``/SamsungPrinters`` folder
- open the file with **TextEdit** application
- modify the following line
````
*cupsFilter: "application/vnd.cups-raster 0 rastertoqpdl"
````
to
````
*cupsFilter: "application/vnd.cups-raster 0 /Library/Printers/Samsung/UPD/Filters/rastertoqpdl"
````

- rename the file to ``Samsung ML-xxxx Series`` (fill ``xxxx`` with correct Printer version number)
- delete the file extension ``.ppd``
- compress the file with gzip (open a terminal in this folder)
````
sudo gzip Samsung\ ML-xxxx\ Series
````

- copy the ``Samsung ML-xxxx Series.gz`` file to
````
/Library/Printers/PPDs/Contents/Resources/
````

- open a terminal and execute the following commands
````
sudo chmod +x /Library/Printers/PPDs/Contents/Resources/Samsung\ ML-xxxx\ Series.gz
sudo chown root:admin /Library/Printers/PPDs/Contents/Resources/Samsung\ ML-xxxx\ Series.gz
````

- plug in the ML-xxxx printer
- open **System Settings**
- go to **Printers & Scanners**
- click on **Add Printer**
- choose **Samsung ML-xxxx, Splix V. 2.0.0** as driver
- start printing :)
