# domoticz-ble-passive-scan

A Bluetooth low energy sensor scanner for Domoticz.

I've been using https://github.com/fr31b3u73r/miThermoHygro/ for some time happily.

While it's working, it:

- doesn't seem to be maintained,
- had to be patched for python3,
- is using bluepy, which seems dead,
- has sensor configuration hard coded

Moreover, the sensor I have is sending the data through BLE advertisements.
So, passive scanning should just work. Some people are even thinking that
using only passive scanning will use less energy than having to connect to the device.

The protocol has been taken from an other project:
https://github.com/mspider65/Xiaomi-Mijia-Bluetooth-Temperature-and-Humidity-Sensor.

# Requirements

According to https://github.com/hbldh/bleak/pull/884, the following versions are needed:

- BlueZ >= 5.56 (tested on 5.66. Some bug reports tends to say that at least 5.65 is needed
  it reality https://github.com/home-assistant/core/issues/78543#issuecomment-1249188320).
- Linux kernel >= 5.10.
- BlueZ experimental features are needed.

# Configuration file

See ``cfg.yml`` for an example of configuration file.


# License

GPL3+
