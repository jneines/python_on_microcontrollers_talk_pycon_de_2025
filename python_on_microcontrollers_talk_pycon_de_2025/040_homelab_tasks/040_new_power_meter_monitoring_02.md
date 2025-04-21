# New power meter readings

:::::{grid} 2 2 2 2 

::::{card}

    b'\x1b\x1b\x1b\x1b\x01\x01\x01\x01v\x05'
    b'\x002\xf8\x0cb\x00b\x00rc'
    b'\x01\x01v\x01\x01\x05\x00\x10\xfdZ'
    b'\x0b\t\x01ISK\x00\x05c\xbd'
    b'\xd7\x01\x01c\x9a\xdf\x00v\x05\x00'
    b'2\xf8\rb\x00b\x00rc\x07'
    b'\x01w\x01\x0b\t\x01ISK\x00'
    b'\x05c\xbd\xd7\x07\x01\x00b\n\xff'
    b'\xffrb\x01e\x00\x19\x88\x9fy'
    b'w\x07\x81\x81\xc7\x82\x03\xff\x01\x01'

::::

::::{card}

- Not all is lost
- There's a structure
- `b\x1b\x1b\x1b\x1b\x01\x01\x01\x01` gives a hint
- It's the [SML](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Publikationen/TechnischeRichtlinien/TR03109/TR-03109-1_Anlage_Feinspezifikation_Drahtgebundene_LMN-Schnittstelle_Teilb.pdf?__blob=publicationFile)
 protocol this time
- There are ready made parsers for that
- But it can't be to hard to do it ourselves, can it?


::::

:::::
