---
"@hangtime/grip-connect": patch
"@hangtime/cli": patch
---

The new CTS500 `batteryLevel()` method estimates the battery charge percent from the reported voltage, using a generic
single-cell Li-ion curve. `battery()` still returns the raw voltage unchanged. The CLI "Battery" action now prints both
the voltage and the estimated charge level.
