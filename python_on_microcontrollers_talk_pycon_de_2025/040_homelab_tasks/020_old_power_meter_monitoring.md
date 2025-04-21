# Monitoring the old power meter

:::::{grid} 2 2 2 2

::::{card}

- has **infrared eye** at the top right corner
- acts as a serial interface
- just needs a photo transistor and pull up resistor for read out
- more sophisticated and robust solutions exist

- speaks the `d0` protocol shown to the right
- can be properly decoded, but does not have to
- contains `OBIS` values in ascii format
- can easily be matched
- we're looking for the `1-0:1.8.1\*255` value
- `40092.0272` is the current reading in kWh
- Together with the current time stamp, we're done!
::::


::::{card}

:::{figure} ../images/old_power_meter.jpg
:width: 60%
:alt: old power meter
:::

    b'/EM\x00Uj\x00)))\x16\x00--\x000@'
    b'C+\x06L\x00c\x051-@R\x02r\x00\x13\t\x025H55\x00\x1a\x1a'
    b'\x13\x03\x02j\x00\x13&\x083729\x00k&(\x12K\x18:@sBs\x00\x1b5H55\x00\x02"\x03\x02J\x12s\x00\x136M\x18)'
    b'@k\x02RJ2r\x00\x13)\x135H55\x00B\x03J\x04L`0\x10\x02RJ2r\x00\x1bI\x12MM\x0025@B\x02\x02\x02\x0222JJJ2J\x04L\x00Hc\x00/EMH5----eHZ-E0018E'
    b''
    b'1-0:0.0.0*255(331200-5003729)'
    b'1-0:1.8.1*255(040092.0260)'
    b'1-0:96.5.5*255(80)'
    b'0-0:96.1.255*255(0000669996)'
    b'!'

::::

:::::
