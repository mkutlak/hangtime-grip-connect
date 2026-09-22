---
"@hangtime/grip-connect": patch
"@hangtime/cli": patch
---

`serial()` reads the CTS500 serial number when the device has the serial characteristic. The new `firmwareUart()` method
sends the UART firmware command and returns the raw payload as hex. A command timeout now names the UART bridge and the
baud rate, so the reader knows where to look.
