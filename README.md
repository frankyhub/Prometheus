# Prometheus

### Beispiel: 1 Layer 4 Kanal Lauflicht (Lötübung I)
![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/4Kanal-LL.png)

### Link zu Zippyrobotics
[Home](https://www.zippyrobotics.com/)

### ProCam download
[Download](https://www.zippyrobotics.com/download/)

### How To and Guides Videos
[walk trough](https://www.zippyrobotics.com/how-to/)

### Einleitung
Prometheus ist eine 2-Layer PCB-Fräse (PCB = Printed Circuit Board). Angesteuert wird die PCB-Fräse mit ProCAM von Zippy Robotics. Die Windows-Software steht auf der Herstellerseite zippyrobotics.com zum Download zur Verfügung. Das PCB-Design wird z. B. mit KiCad erstellt und die Layer in ProCAM importiert. In ProCAM werden auch alle Parameter wie Fräser- und Bohrerdurchmesser oder die Anzahl der Fräs-Durchgänge festgelegt.

### ProCAM installieren
Nach dem Download sind folgende Schritte auszuführen:
1. Den Ordner C:\Program Files (x86)\Zippy Robotics erstellen,
2. die Download-Dateien entpacken und in den Ordner kopieren,
3. die EXE-Datei starten.
4. Auf der Herstellerseite stehen auch Hilfe-Videos zur Verfügung.


### Checklisten

ProCAM Installation
- [ ] [Download](http://www.zippyrobotics/download/) von ProCAM
- [ ] Den Ordner C:\Program Files (x86)\Zippy Robotics erstellen
- [ ] die Downlaod-Dateien in den Ordner kopieren
- [ ] die EXE-Datei starten        

KiCad:

- [ ] Max Platinengröße: 160 x 100
- [ ] Große Pads (Empfehlung)
- [ ] Gleich große Bohrlöcher (Empfehlung)
- [ ] Offset links unten einfügen
- [ ] Ursprung links unten einfügen
- [ ] Die Edge Cut Linien müssen in sich geschlossen sein
- [ ] Plotter Einstellungen anpassen
- [ ] Leerzeichen aus drl-Datei löschen

Prometheus:

- [ ] Top-Copper, Drill und Cut-Datei laden
- [ ] Top-Copper Bohrwerkzeug einstellen (.005 in (.130mm) 15 deg. mil)
- [ ] Anzahl der Durchgänge festlegen (Empfehlung 3)
- [ ] Platine mit doppelseitigen Klebeband (4 Reihen) fixieren
- [ ] Elektrische Verbindung zwischen Platine und der Messingleiste herstellen 
- [ ] Leiterbahnen fräsen:
- [ ] Werkzeug einspannen
- [ ] .005 in (.130mm) 15 deg. mil Fräser einspannen 
- [ ] Knuppel zum spannen nach links schieben 
- [ ] Kugellager von der Frässpitze aus aufschieben
- [ ] Fräser mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Knuppel nach rechts schieben und festen Sitz kontrollieren
- [ ] Platinenoberfläche mit Öl benetzen
- [ ] Fräsvorgang starten
- [ ] Drill: 
- [ ] Bohrer für die Bohrlöcher wechseln (0,85mm)
- [ ] Elektrische Verbindung zwischen Platine und der Messingleiste herstellen 
- [ ] Knuppel zum spannen nach links schieben 
- [ ] Kugellager von der Bohrerspitze aus aufschieben
- [ ] Bohrer mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Knuppel nach rechts schieben und festen Sitz kontrollieren
- [ ] Bohren starten 
- [ ] Edge cut:
- [ ] Fräser für die Edge cut wählen (0.0945" Square End Mill)
- [ ] Elektrische Verbindung zwischen Platine und Messingleiste herstellen 
- [ ] Knuppel zum spannen nach links schieben 
- [ ] Kugellager von der Frässpitze aus aufschieben
- [ ] Fräser mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Knuppel nach rechts schieben und festen Sitz kontrollieren
- [ ] Öl aufbringen, ggf. Späne absaugen 
- [ ] Edge cut starten
- [ ] Arbeitsplatz aufräumen


### Screenshots

KiCad:

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad1.png)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad2.png)

Plotter Einstellungen


![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad4.png)

Bohrdatei Einstellungen


![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad5.png)

Änderung in der Drilldatei


![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/drill1.png)

Procam Einstellungen


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


