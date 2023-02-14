# Verschlüsseln von LOS Nummern  
Die Losnummer besteht aus vier Elementen und drei Leerzeichen:  
*"L" + " " + Erzeugernummer + " " + Kalenderwoche + " " + numerischer Wochentag*  
  
Ziel ist es; die Losnummer zu verschlüsseln, so dass die einzelnen Elemente nicht mehr erkennbar sind.  
Die Verschlüsselung soll so sein, dass die einzelnen Elemente wiederherstellbar sind.  
   
```mermaid
graph TD;
    text[LOSNummer];
    id1[L 50387 04 04]-->id2[Kalenderwoche & numerischen Wochentag in Buchstaben Umwandeln];
    id2-->id3[L 50387 AEAE]-->id4[Zufallszahl zwischen 100 - 999 generieren]-->id5[Z.B. '123'];
    id5-->id6[Zufallszahl in Buchstaben umwandeln z. B. '123' -> 'ABC']-->id7[Konvertierte Zufallszahl zwischen umgewandelter Kalenderwoche & Wochentag einfügen]-->id8['L 50387 AEABCAE'];
    style text fill:#009911,stroke:#333,stroke-width:4px;
    style id1 fill:#009911,stroke:#333,stroke-width:3px;
    style id3 fill:#009911,stroke:#333,stroke-width:3px;
    style id8 fill:#009911,stroke:#333,stroke-width:3px;
```