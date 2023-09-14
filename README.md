# How to install Samsung ML-1640 printer driver for macOS Ventura and Apple Silicon

This example shows how to install the ML-1640 printer driver on macOS Ventura.

- clone the provided files
````
git clone https://github.com/MTz12/Samsung-ML-1640-Printer-Ventura-Apple-Silicon.git
````

- copy the ``Samsung`` folder to
````
/Library/Printers/
````

- copy the file ``Samsung ML-1640 Series.gz`` to
````
/Library/Printers/PPDs/Contents/Resources/
````

- open a terminal and execute the following commands
````
sudo chmod +x /Library/Printers/PPDs/Contents/Resources/Samsung\ ML-1640\ Series.gz
sudo chown root:admin /Library/Printers/PPDs/Contents/Resources/Samsung\ ML-1640\ Series.gz
````

- Connect the ML-1640 printer
- Open **System Settings**
- Go to **Printers & Scanners**
- Click on **Add Printer**
- Select **Samsung ML-1640** as the driver
- You may get an error message: "The Printer software was installed incorrectly."
- Click on **Repair** to fix the error
- Start printing a test page
- You may receive an error message when printing for the first time: "rastertoqpdl cannot be opened because the developer cannot be verified."
- Open **System Preferences**
- Go to **Privacy & Security**
- Scroll down to the message "rastertoqpdl was blocked from use because it is not from an identified developer."
- Accept the error message and click **Allow Anyway**
- Try printing again and click **Open** when an error message appears
