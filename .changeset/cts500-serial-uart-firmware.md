---
"@hangtime/grip-connect": patch
"@hangtime/cli": patch
---

`serial()` reads the CTS500 serial number when the device has the serial characteristic. The new `firmwareUart()` method
sends the UART firmware command and returns the raw payload as hex. A command timeout now names the UART bridge and the
baud rate, so the reader knows where to look.

Firmware 2.1.3 answers a command with a typed `05 80 <opcode>` response, not with a 6-byte echo. The client now accepts
both. `stop()`, `zero()`, `peakMode()`, `powerOnReset()` and `tare()` no longer time out on this firmware, and
`stream()` no longer fails at the end.
