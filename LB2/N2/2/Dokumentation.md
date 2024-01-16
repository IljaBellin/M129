# N2 Auftrag 1

## Forderung

Netzwerk aufsetzen

16 Computer
8 Switches
1 Router

## Bedingungen:

Netzwerk läuft und ist gut dokumentiert.

## Netzplan 

![Alt text](image.png)

## Aufträge

Ich muss das Netzwerk 37.105.96.0/22 auf acht andere Netze aufteilen.

Bei einem Netzwerk mit /24er Netzmaske würde dies noch nicht gehen, da ich dort nur zwei erstellen kann. Also entschied ich mich für ein /25er Netzwerk, so habe ich in jedem Subnetz 128 IP Adressen.

![Alt text](image-1.png)

Diese Subnetztabelle half mir dabei. 

![Alt text](image-2.png)

### Excel Netzwerk Tabelle ausfüllen
![Alt text](image-4.png)


### Subnetzte

Subnetz 1: 37.105.96.0/25

PC-1: 37.105.96.10
PC-2: 37.105.96.20
Default Gateway: 37.105.96.1
Subnetz 2: 37.105.96.128/25

PC-1: 37.105.96.130
PC-2: 37.105.96.140
Default Gateway: 37.105.96.129
Subnetz 3: 37.105.97.0/25

PC-1: 37.105.97.10
PC-2: 37.105.97.20
Default Gateway: 37.105.97.1
Subnetz 4: 37.105.97.128/25

PC-1: 37.105.97.130
PC-2: 37.105.97.140
Default Gateway: 37.105.97.129
Subnetz 5: 37.105.98.0/25

PC-1: 37.105.98.10
PC-2: 37.105.98.20
Default Gateway: 37.105.98.1
Subnetz 6: 37.105.98.128/25

PC-1: 37.105.98.130
PC-2: 37.105.98.140
Default Gateway: 37.105.98.129
Subnetz 7: 37.105.99.0/25

PC-1: 37.105.99.10
PC-2: 37.105.99.20
Default Gateway: 37.105.99.1
Subnetz 8: 37.105.99.128/25

PC-1: 37.105.99.130
PC-2: 37.105.99.140
Default Gateway: 37.105.99.129

/25 = 255.255.255.128


### Fragen

Wieviele freie IP-Adressen gibt es in der Abteilung Einkauf?
124


Ist ein mögliches Wachstum der Firma berücksichtigt?
Ja, jedes Netzwerk hat 124 freie IPs

Ist das Netzwerk-Design sinnvoll?
Ja

Gibt es Verbesserungsvorschläge bzgl. Netzwerk-Design?

Nein

Welche zusätzlichen Informationen wären nützlich, um für dieses Netzwerk-Design einen Optimierungsvorschlag auszuarbeiten?

keine