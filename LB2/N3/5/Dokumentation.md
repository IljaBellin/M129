# Subnetting und Routing mit unterschiedlich grossen Netzwerken über zwei Oktette

## Aufgabenstellung 3.5

**Theorie und Praxis kombiniert**

Zuerst erstellen Sie das Netzwerk-Design. Danach setzen Sie die Umgebung mit CISCO Packet Tracer um (Vorlage weiter unten)


## Ausgangslage
Die Firma Go-IT AG hat einen **Hauptsitz** im Zentrum von Zürich (Management und Verwaltung) und einen **Branch** in einem Aussenquartier (Betrieb).

**Hauptsitz:**  
- 23 PCs
- 20 Laptops  
- 7 Drucker

**Branch:**  
- 65 PCs
- 55 Laptops  
-  7 Drucker

Beide Firmensitze sind über eine Standleitung verbunden. Die **beiden Häuser haben getrennte Netze**. Der Hauptsitz ist über einen **DSL-Router mit dem Internet** verbunden.

Für die Netzwerke steht das **Netz 192.168.100.0/23**
zur Verfügung. Für die Internetleitung erhalten wir vom ISP die statische IP-Adresse **95.2.50.102/30**, der Router des ISP hat die IP-Adresse **95.2.50.101/30**.


**Situations- und Netzwerkplan**

![Netzwerkplan](P3_5_netzwerk_800.jpg)

## 1. Teilauftrag (Theorie)

Erstellen Sie für die Firma **Go-IT** einen IP-Plan mit folgenden Teil-Aufgaben. Bei jeder Tabelle ist **die erste Zeile** als Beispiel ausgefüllt.

1.  Teilen Sie das erhaltene Netz in passende **Subnetze** auf.

2.  Bestimmen Sie die **Netzadressen**, **Netzmasken** und **Broadcastadressen**.

3.  Teilen Sie den **Routerinterfaces IP-Adressen** zu.

4.  Erstellen Sie die **Routingtabellen** für **Router Haus A** und **Router
    Haus B**.


### Netzgrössen

| Netz | Benötigte Adressen | Gewählte  Netzgrösse |
|------|-----------|----------------|
| Netz T | 0 PCs + 0 LTs + 0 DR + 2 RT + 2 = 4  |    4  |
| Netz I | vom Provider | -
| Netz A | AUSFÜLLEN | AUSFÜLLEN |
| Netz B | AUSFÜLLEN | AUSFÜLLEN |

### Netzadressen

| Netz   | Grösse | Netzadresse/Netzmaske (Bit) | Dezimale Schreibweise der Netzmaske | Broadcastadresse |
|--------|-----|-----|-----|-----|
| Netz I |  4  | 92.2.50.100 /30  | 255.255.255.252 | 92.2.50.103 |
| Netz T | AUSFÜLLEN | AUSFÜLLEN | AUSFÜLLEN | AUSFÜLLEN |
| Netz A | AUSFÜLLEN | AUSFÜLLEN | AUSFÜLLEN | AUSFÜLLEN |
| Netz B | AUSFÜLLEN | AUSFÜLLEN | AUSFÜLLEN | AUSFÜLLEN |


---

### Grafische Darstellung (Kreis)

HIER DEN KREIS MIT UNTERTEILUNG DER SUBNETZE EINFÜGEN (Z.B. ALS SCREENSHOT)

- [Kreis-Vorlage - jpg-Bild](P3_5_kreis.png)
- [Kreis-Vorlage mit Subnetzen - Visio-Datei](P3_5_subnetz-kreise.vsdx)


---

<br>

### Router-Interfaces

| **Router**      | **Interfaceadresse** | **Interface** |
|-----------------|----------------------|---------------|
| Router A Netz I | 92.2.50.102 /30      | s1            |
| Router A Netz A | AUSFÜLLEN            | e0            |
| Router A Netz T | AUSFÜLLEN            | s0            |
| Router B Netz B | AUSFÜLLEN            | e0            |
| Router B Netz V | AUSFÜLLEN            | s0            |

### Routingtabelle Router A

| **Destination Network** (Zielnetz + Netzmaske) | **Next Hop** (Nächster Router auf dem Weg zum Ziel) | **Metric** (hier Hop Count)  | **Interface** (auf diesem Router) |
|-----|------|----------|------|
| (A) 192.168.101.0 /26   | -- | 0 | e0 |
| (T) AUSFÜLLEN | -- | 0 | s0 |
| (I) AUSFÜLLEN | -- | 0 | s1 |
| (B) AUSFÜLLEN | AUSFÜLLEN | 1 | s0 |
| (Default) 0.0.0.0 / 0 | 95.2.50.101/30 | -- | s1 |

### Routingtabelle Router B

| **Destination Network**  (Zielnetz + Netzmaske) | **Next Hop** (Nächster Router auf dem Weg zum Ziel) | **Metric** (hier Hop Count)  | **Interface** (auf diesem Router) |
|--------|-------|-------|---------|
| (T) AUSFÜLLEN  | -- | 0 | s0 |
| (B) AUSFÜLLEN  | -- | 0 | e0 |
| (Default) 0.0.0.0 / 0 | AUSFÜLLEN | -- | s0 |


## 2. Teilauftrag (Praxis)
Setzen Sie diese Netzwerkumgebung mit dem CISCO Packet Tracer um. Nutzen Sie dabei DIESE VORLAGE. Sie müssen **keine** weiteren Geräte anschliessend. Die Namen der Geräte sind bereits eingetragen. Sämtliche Konfigurationen fehlen noch. Achten Sie ausserdem darauf, dass diverse Netzwerkkarten noch eingeschaltet werden müssen, damit sie überhaupt funktionieren.
- [CISCO Packet Tracer Vorlage](Vorlage.pkt)



## Abgabe:
- Dokumentation mit allen Angaben zum Netzwerk
- Live-Demo bei der LP - Doku und CISCO PT (10’)


## Ressourcen:
- [Lösungen zu einer ählichen Aufgabe, die im Unterricht durchgeführt wurde](P3_5_uebung_a.pdf)
- [Tutorial "Routing Teil 2 (Statisches Routing)](https://web.microsoftstream.com/video/0d47cf40-6a8a-4539-a7b4-b0cfeeac51ce?list=studio) (Statisches Routing auf CISCO Packet Tracer erklärt) - 8:55


<br>



---

> [⇧ **Zurück zu N3** (Expert)](N3/)

---

> [⇧ **Zurück zur Hauptseite**](https://gitlab.com/ser-cal/m129-lb2)


