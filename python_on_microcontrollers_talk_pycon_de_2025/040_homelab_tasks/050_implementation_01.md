# How to implement

- [SML](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Publikationen/TechnischeRichtlinien/TR03109/TR-03109-1_Anlage_Feinspezifikation_Drahtgebundene_LMN-Schnittstelle_Teilb.pdf?__blob=publicationFile)
 protocol basically consists of lists of messages
- There are opening and closing sequences
- e.g. `b\x1b\x1b\x1b\x1b\x01\x01\x01\x01` was the opening sequence
- `b\x1b\x1b\x1b\x1b\x1a` shows the end
- the remaining byte stream within can be parsed
- opening byte tells about what to expect afterwards
- upper 4 bits encode the type
- lower 4 bits encode the size 
- quite simple.

