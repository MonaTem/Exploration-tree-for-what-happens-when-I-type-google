
- The USB circuitry of the keyboard is powered by the 5V supply provided over pin 1 from the computer's USB host controller.
- The keycode generated is stored by internal keyboard circuitry memory in a register called "endpoint".
- The host USB controller polls that "endpoint" every ~10ms (minimum value declared by the keyboard), so it gets the keycode value stored on it.
- This value goes to the USB SIE (Serial Interface Engine) to be converted in one or more USB packets that follows the low level USB protocol.
- Those packets are sent by a differential electrical signal over D+ and D- pins (the middle 2) at a maximum speed of 1.5 Mb/s, as an HID (Human Interface Device) device is always declared to be a "low speed device" (USB 2.0 compliance).
- This serial signal is then decoded at the computer's host USB controller, and interpreted by the computer's Human Interface Device (HID) universal keyboard device driver. The value of the key is then passed into the operating system's hardware abstraction layer.
