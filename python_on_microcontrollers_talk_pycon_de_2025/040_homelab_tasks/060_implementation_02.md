# Parser output

Sample parser output containing the power reading

    ('List entry found: 7 entries to process',)
        (135, 6, 7)
        ("String entry found having 6 bytes: value=bytearray(b'\\x01\\x00\\x02\\x08\\x01\\xff')",)
        (128, 6, 6)
        ("String entry found having 0 bytes: value=bytearray(b'')",)
        (127, 6, 5)
        ("String entry found having 0 bytes: value=bytearray(b'')",)
        (126, 6, 4)
        ('Unsigned int found consisting of 1 byte: value=30',)
        (124, 6, 3)
        ('Signed int found consisting of 1 byte: value=3',)
        (122, 6, 2)
        ('Unsigned int found consisting of 8 byte: value=22',)
        (113, 6, 1)
        ("String entry found having 0 bytes: value=bytearray(b'')",)
        ('LIST COMPLETE',)


bytearray at the beginning is the `OBIS` identifier for power use again.
`value=30` indicates the unit to use -> Wh.
`value=3` sets the scaler for the value -> 10^3.
`value=22` is the current reading.

-> 22000 Wh


