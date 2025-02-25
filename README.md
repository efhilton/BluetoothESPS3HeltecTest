# Bluetooth Joystick Library Tester for ESP32

This project sets up basic BLE functionality in a Heltec Lora Wifi ESP32-S3 device I had lying around. It is primarily
intended to test a separately developed Bluetooth Joystick library for my ESP32. Specifically, a remote device -- aka an
Android application -- can enable/disable functions, trigger events, send joystick events to this embedded device.
Additionally, the remote device -- aka the Android application -- can also receive console messages from this embedded
device -- all via Bluetooth Low Energy.

This code is intended to work in conjunction with:

- the [Android App](https://github.com/efhilton/BluetoothJoystick). I wrote this to work on my Pixel 8 with the latest
  APIs.
- the [BLE ESP-IDF Joystick](https://github.com/efhilton/BluetoothJoystickLibraryESP32) Library itself, which should be
  added as a git submodule under `components/ble-joystick`

## Implemented Features

As of the time of this writing, this code presently makes use of several features provided by the Bluetooth Joystick Library.

It makes use of the following Functions:

- [x] F1: Used to enable/disable the (very bright) LED that is onboard the Heltec on GPIO 35
- [x] F2: Used to enable/disable the ability to transmit Console messages to the remote Android app.
- [x] F3: Used to enable/disable the Left Joystick control (Left Right, Up Down), which puts out PWM output on GPIO 0 and 2,
  respectively.
- [ ] F4:
- [ ] F5
- [ ] F6:
- [ ] F6:
- [ ] F7:
- [ ] F8:
- [ ] F9:
- [ ] FA:
- [ ] FB:
- [ ] FC:
- [ ] FD:
- [ ] FE:
- [ ] FF:

It makes use of the following Triggers:

- [ ] T1
- [ ] T2
- [ ] T3
- [ ] T4
- [ ] T5
- [ ] T6
- [ ] T7
- [ ] T8
- [ ] T9
- [ ] TA
- [ ] TB
- [ ] TC
- [ ] TD
- [ ] TE
- [ ] TF

It makes use of the Joystick:

- [x] Joystick Left: normalized (+/- 1.0) output as a duty cycle on GPIO 0
- [x] Joystick Left: normalized (+/- 1.0) output as a duty cycle on GPIO 2
- [ ] Joystick Right: horizontal axis
- [ ] Joystick Right: vertical axis

More features shall be added as I continue to implement more features on my electronics device.

## Cloning the Project

This project makes use of git submodules, which means you need to perform additional steps to ensure all submodules are
correctly initialized and updated after cloning. Here are the steps to clone this repository:

### Clone the Repository with submodules

To clone the repository properly, along with its submodules, use the `--recurse-submodules` flag:

``` bash
   git clone --recurse-submodules git@github.com:efhilton/BluetoothJoystickLibraryESP32Test.git
```

### If You Already Cloned the Repository Without Submodules

If you have already cloned the repository without the `--recurse-submodules` flag, you can still initialize and update
the submodules with the commands below:

``` bash
   git submodule init
   git submodule update
```

Alternatively, you can run the following single command to initialize and update submodules in one step:

``` bash
   git submodule update --init --recursive
```

### Keeping Submodules Updated

If there are updates to the submodules in the repository, you can pull the latest changes for both the main repo and its
submodules using:

``` bash
   git pull --recurse-submodules
```

This ensures that your submodules are always up-to-date with the repository.

## Questions?

Please contact [Edgar Hilton](mailto://edgar.hilton@gmail.com) if you have any questions.
