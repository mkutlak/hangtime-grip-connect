---
"@hangtime/grip-connect": patch
"@hangtime/cli": patch
---

The new CTS500 `firmwareUart()` method returns the raw MCU firmware bytes as hex, for example `20 3A 96`. `serial()` now
reads the serial number where the platform allows it. Browsers never get it, because the Web Bluetooth blocklist hides
it. The CLI gets a "Firmware (UART)" action. An unmatched `0xA4` answer now reaches the `write()` callback as `20 3A 96`
instead of the raw 7-byte frame.
