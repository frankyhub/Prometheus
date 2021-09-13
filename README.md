# Prometheus

### Beispiel: 1 Layer 4 Kanal Laiflicht (Lötübung I)
![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/4Kanal-LL.png)

### Link zu Zippyrobotics
[Home](https://www.zippyrobotics.com/)

### ProCam download
[Download](https://www.zippyrobotics.com/download/)

### walk trough Videos
[How to](https://www.zippyrobotics.com/how-to/)


### Checkliste


KiCad:

- [ ] Max Platinengröße: 160 x 100
- [ ] Große Pads
- [ ] Gleich große Bohrlöcher
- [ ] Große Leiterbahn Abstände
- [ ] Offset links unten einfügen
- [ ] Ursprung links unten einfügen
- [ ] Plotter Einstellungen ändern
- [ ] Leerzeichen aus drl-Datei löschen

Prometheus:

- [ ] Top-Copper und Drill-Dateien laden
- [ ] Top-COpper Bohrwerkzeug einstellen .005 in (.130mm) 15 deg. mil
- [ ] Anzahl der Durchgänge festlegen (3)
- [ ] Platine mit doppelseitigen Klebeband mit 4 Reihen fixieren
- [ ] Elektrische Verbindung zwischen Platine und Messingleiste herstellen 
- [ ] Werkzeug spannen
- [ ] .005 in (.130mm) 15 deg. mil Fräser spannen 
- [ ] Knuppel zum spannen nach links schieben 
- [ ] Kugellager von der Frässpitze aus aufschieben
- [ ] Mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Knuppel nach rechts schieben
- [ ] Platinenoberfläche mit Öl benetzen
- [ ] Fräsvorgang starten
- [ ] Fräser für die Bohrlöcher wechseln
- [ ] Elektrische Verbindung zwischen Platine und Messingleiste herstellen 
- [ ] Knuppel zum spannen nach links schieben 
- [ ] Kugellager von der Frässpitze aus aufschieben
- [ ] Mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Knuppel nach rechts schieben
- [ ] Bohren starten 
- [ ] Elektrische Verbindung zwischen Platine und Messingleiste herstellen 
- [ ] Knuppel zum spannen nach links schieben 
- [ ] Kugellager von der Frässpitze aus aufschieben
- [ ] Mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Knuppel nach rechts schieben
- [ ] Fräser Edge cut wechseln
- [ ] Öl aufbringen, ggf Späne absaugen 
- [ ] Edge cut starten
- [ ] Arbeitsplatz aufräumen


### Screenshots

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad1.png)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad2.png)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad4.png)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad5.png)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/drill1.png)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/Prom1.png)





### Oberlab Wiki

Specs laut Hersteller

Parameter	Value

Spindle Speed	50,000 RPM

Max X/Y Speed	Greater than 3,800 mm/min (150 IPM)

Spindle Runout (TIR)	< 2.5 microns, 10 mm below the spindle bearing (static)

Max PCB Size	160 mm x 100 mm

PCB Type	FR-4, FR-1, Rogers 4350 (other Rogers laminates are being tested). Single or Double-sided

Min Trace/Space	4 mil traces/5 mil spaces (1 mil = .001 in. = .0254 mm, 5 mils = .127 mm)

Max Drilled Hole Size	.125 in. (3.175 mm)

X and Y Resolution	.000156 in. (4 microns)

Z Resolution	.000049 in. (1.25 microns)

Verfügbare Bits im Lab

0.0315" Router

5-mil 15° Carving Bit

0.0197" Square End Mill

0.0945" Square End Mill

0.85mm Drill Bit

1.2mm Drill Bit

2.3mm Drill Bit

0.125" Drill Bit


### Anleitung
1. Produktionsdaten vorbereiten

Ursprungspunkt des Rasters und Offset für Bohrungen auf einen Punkt der Zeichnung (selber Punkt für beide) platzieren, sodass die Zeichnung vollständig rechts oberhalb dieses Punktes liegt.


2. Produktionsdaten exportieren

Aus KiCad per "plotten" folgende Layer exportieren:


F.Cu

B.Cu

Edge.Cuts

Dabei Verwende Hilfsachsen als Ursprungspunkt auswählen.


Edge.Cuts muss genau eine geschlossene Linie enthalten. Es können nicht mehrere, getrennte Linien gefräst werden.


Bohrdateien exportieren und dabei folgende Einstellungen wählen:


Format: Excellon

Bohrlochursprung: Hilfsachse

Einheiten: Millimeter

Nullen Format: Unterdrücke führende Nullen

PTH- und NPTH-Bohrungen innerhalb einer Datei vereinen

Damit ProCam die Datei sauber einliest, muss man im .drl file ggf. das Leerzeichen zwischen ; und FORMAT in der folgenden Zeile entfernen:


; FORMAT={3:3/ absolute / metric / suppr


