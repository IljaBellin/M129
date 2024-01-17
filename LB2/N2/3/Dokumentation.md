# N2 Auftrag 3

## Forderung

Fehler finden in einem Netzwerk mit;

16 Computer
8 Switches
1 Router

## Bedingungen:

Fehler finden und festhalten

## Netzplan 

![Alt text](image.png)

## Aufträge

### Excel Netzwerk Tabelle ausfüllen

![Alt text](image-1.png)

### Subnetzte

Subnetz 1: 170.11.83.0/29 (Range: 170.11.83.0 - 170.11.83.7)
Subnetz 2: 170.11.83.8/29 (Range: 170.11.83.8 - 170.11.83.15)
Subnetz 3: 170.11.83.16/29 (Range: 170.11.83.16 - 170.11.83.23)
Subnetz 4: 170.11.83.24/29 (Range: 170.11.83.24 - 170.11.83.31)
Subnetz 5: 170.11.83.32/29 (Range: 170.11.83.32 - 170.11.83.39)
Subnetz 6: 170.11.83.40/29 (Range: 170.11.83.40 - 170.11.83.47)
Subnetz 7: 170.11.83.48/29 (Range: 170.11.83.48 - 170.11.83.55)
Subnetz 8: 170.11.83.56/29 (Range: 170.11.83.56 - 170.11.83.63)

### Fehler-Tabellen ausfüllen

**Gefundene Fehler (und Korrekturen) für die einzelnen Aufgaben**

| **Gerät** | **Gefundener Fehler, ausgeführte Korrektur**    |
|-------------|----|
| Router | SW-04 Adresse 170.11.83.28 -> 170.11.83.25   |
| PC-2 | IP-Adresse ist falsch im vierten Oktett. Gem. Netzwerkplan angepasst auf 170.11.83.2 |
| PC-51 | Netzmaske 255.255.248.0 -> 255.255.255.248 |
| PC-10 | Ip Adresse 170.11.83.11 -> 170.11.83.10 |
| PC-50 | Ip Adresse 170.11.83.250 -> 170.11.83.50 |
| PC-3 | Gateway 170.11.82.1 -> 170.11.83.1 |
| PC-11 | Gateway 170.11.83.8 -> 170.11.83.9|
| PC-43 | Gateway "-" -> 170.11.83.41 |
| PC-59 | Gateway 170.11.83.59 -> 170.11.83.57 |
| | |
| | |

**Fehlersuche Journal**

| **Ausgeführter Test** | **Beobachtetes Resultat/ (Ausgeführte Korrektur)** |
|------------|----------|
| Diverse Ping | Funktionierten alle | 


###