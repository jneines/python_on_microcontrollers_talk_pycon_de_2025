# Key Take Aways

- Python applications can easily be transferred to a microcontroller thanks to MicroPython
- In case costs and the size of the device is key this can be quite trivial
- When energy saving is the main goal, the way to handle loops is key
- send the device to sleep whenever possible
- keep it there as long as possible
- wake up by events (timers, device movement, pin state changes, ...)
- have a close look at using WiFi (re-configuring WiFi frequently costs a lot of energy)
- pay attention at monitoring battery voltage
- Simple voltage dividers connected to an ADC pin technically work ...
- ... but drain the battery constantly
