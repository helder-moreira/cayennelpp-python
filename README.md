# Cayenne LPP

This module provides a Cayenne Low Power Payload (LPP) encoder for python/micropython. More info about Cayenne LPP at [Cayenne Docs](https://mydevices.com/cayenne/docs/lora/#lora-cayenne-low-power-payload).

# Supported Data Types

Currently supported data types are the same as the ones supported by the official Cayenne LPP C/C++ implementation:
  - Digital Input
  - Digital Output
  - Analog Input
  - Analog Output
  - Illuminance Sensor
  - Presence Sensor
  - Temperature Sensor
  - Humidity Sensor
  - Accelerometer
  - Barometer
  - Gyrometer
  - GPS Location

# Usage

The syntax also conforms with the official Cayenne LPP C/C++ implementation as described in [Cayenne Docs](https://mydevices.com/cayenne/docs/lora/#lora-cayenne-low-power-payload).

#### Example

```python
from cayennelpp import CayenneLPP

c = CayenneLPP()
c.addTemperature(1, 23.5) # Add temperature read to channel 1 
c.addTemperature(2, 22.7) # Add another temperature read to channel 2
c.addRelativeHumidity(3, 88.5) # Add relative humidity read to channel 3
data = c.getBuffer() # Get bytes

```

License
----

MIT
