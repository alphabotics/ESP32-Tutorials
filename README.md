# ESP32-Tutorials

A collection of sample for working with ESP32 board

## Hardwares

- ESP32-WROOM-32 ([Based on ESP32-DevKitC V4](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/hw-reference/esp32/get-started-devkitc.html))

## Quickstart

### Check serial port on Linux and macOS

```bash
ls /dev/ttyUSB*
```

### Adding user to dialout on Linux

The currently logged user should have read and write access the serial port over USB. 

On most Linux distributions, this is done by adding the user to dialout group with the following command:

```bash
sudo usermod -a -G dialout $USER
```

## idf.py not found

https://docs.espressif.com/projects/esp-idf/en/v3.1.7/get-started-cmake/add-idf_path-to-profile.html

### Step 1: Standard Toolchain Setup for Linux and macOS

- https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/linux-macos-setup.html#standard-toolchain-setup-for-linux-and-macos

### VSCode Esp Idf extension

- https://github.com/espressif/vscode-esp-idf-extension
- https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/install.md

![](vscode-install-esp-idf.png)

Basic use of the extension.

In this tutorial you will learn how to use the basic commands of this extension to develop your application with Espressif devices.

You have several options to create a project:

Using one the examples from ESP-IDF or any additional supported framework using the ESP-IDF: Show Examples Projects command.
Use one of the templates included with this extension using the ESP-IDF: Create ESP-IDF project command.
NOTE: To configure any additional supported framework, please review configuring additional frameworks

Let's use the ESP-IDF get-started's blink example for this tutorial. 

Click menu View -> Command Palette... and type ESP-IDF: Show Examples Projects and choose Use current ESP-IDF (/path/to/esp-idf). 

If the user doesn't see the option, please review the setup in Install tutorial.

A window will be open with a list a projects, go the get-started section and choose the blink_example. You will see a Create blink_example project button in the top and a description of the project below. Click Create blink_example project button.

## Build and Flash ESP32 board

Check serial port

```bash
ls /dev/ttyUSB*
```

Allow execute on this port

```bash
sudo chmod a+rw /dev/ttyUSB0
```

Flash to ESP32 board

```bash
cd ~/Techlab/HARDWARE/ESP32-Tutorials/demo/blink/blink$ 
idf.py -p /dev/ttyUSB0 flash
```

## Reference

- [Official ESP-IDF Programming Guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html)