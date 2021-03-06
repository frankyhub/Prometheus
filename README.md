# Prometheus  

[![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/khf-version.svg)](#Prometheus)   [![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/datum.svg)](#Prometheus)   <br>


-------------------------------------------------------------

### Inhaltsverzeichnis:

- **[Einleitung](#einleitung)**

- **[ProCAM installieren](#procam-installieren)** 

- **[KiCad Checkliste](#kicad-checkliste)**

- **[ProCAM Checkliste (1-Layer)](#ProCAM-Checkliste-1-Layer)**

- **[Link zu Zippyrobotics](#Link-zu-Zippyrobotics)**

- **[How To Videos and Guides](#How-To-Videos-and-Guides)**

- **[Oberlab Wiki](#Oberlab-Wiki-Danke-an-Sepp)**

-------------------------------------------------------------

### Einleitung
Prometheus ist eine 2-Layer PCB-Fräse (PCB = Printed Circuit Board). Angesteuert wird die PCB-Fräse mit ProCAM von Zippy Robotics. Die Windows-Software steht auf der Herstellerseite zippyrobotics.com zum Download zur Verfügung. Das PCB-Design wird z. B. mit KiCad erstellt und die Layer in ProCAM importiert. In ProCAM werden auch alle Parameter wie Fräser- und Bohrerdurchmesser oder die Anzahl der Fräs-Durchgänge festgelegt.


-------------------------------------------------------------


### ProCAM installieren
1. [Download](http://www.zippyrobotics.com/download/) von ProCAM
2. Den Ordner C:\Program Files (x86)\Zippy Robotics erstellen
3. die Download-Dateien entpacken und in den Ordner kopieren
4. die EXE-Datei starten
5. Auf der Herstellerseite stehen auch Hilfe-Videos zur Verfügung

-------------------------------------------------------------


### KiCad Checkliste
- [ ] Die max Platinengröße: 160 x 100
- [ ] Große Pads verwenden (Empfehlung 3mm)
- [ ] Großen Leiterbahnquerschnitt verwenden (Empfehlung 0.5mm)
- [ ] Gleich große Bohrlöcher definieren (Empfehlung 0,85mm)
- [ ] Für einen positiven Arbeitsbereich der X-Y-Achse den Offset für Bohrungen und Platzierungen links unten einfügen
- [ ] Die Edge Cut Linien müssen in sich geschlossen sein
- [ ] Die Plotter Einstellungen anpassen
- [ ] Die Plotter und Bohrdatei erzeugen
- [ ] Das Leerzeichen aus der DRL-Datei löschen


-------------------------------------------------------------

Den positiven Arbeitsbereich für die X-Y-Achse festlegen (Offset für Bohrungen und Platzierungen)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad1.png)

Die Plotter Einstellungen

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad4.png)

Die Drilldatei Einstellungen

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/kicad5.png)

Änderung in der Drilldatei (Das Leerzeichen löschen - ;FORMAT)

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/drill1.png)


[![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/nachoben.svg)](#Prometheus) 



-------------------------------------------------------------

### ProCAM Checkliste (1-Layer)

- [ ] Die Top-Copper, Drill- und Cut out-Datei importieren
- [ ] Das Top-Copper Bohrwerkzeug einstellen (blau .005 in (.130mm) 15 deg. mill)
- [ ] Die Anzahl der Durchgänge festlegen (Empfehlung 2)
- [ ] Die Platine mit doppelseitigen Klebeband (4 Reihen) fixieren
- [ ] Die Elektrische Verbindung zwischen Platine und der Messingleiste herstellen (Krokodilklemme)

Top  Copper:
- [ ] Den .005 in (.130mm) 15 deg. mill Fräser einspannen (blau 5-mill 15°)
- [ ] Die Knuppel zum spannen nach links schieben
- [ ] Das Kugellager von der Frässpitze aus aufschieben
- [ ] Den Fräser mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Den Knuppel nach rechts schieben und festen Sitz kontrollieren
- [ ] Die Platinenoberfläche mit Öl benetzen
- [ ] Den Fräsvorgang starten

Drill:
- [ ] Den Bohrer für die Bohrlöcher wechseln (lila 0,85mm)
- [ ] Die Elektrische Verbindung zwischen Platine und der Messingleiste herstellen
- [ ] Den Knuppel zum spannen nach links schieben
- [ ] Das Kugellager von der Bohrerspitze aus aufschieben
- [ ] Den Bohrer mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Den Knuppel nach rechts schieben und festen Sitz kontrollieren
- [ ] Die Platinenoberfläche mit Öl benetzen
- [ ] Den Bohrvorgang starten

Cut out:
- [ ] Den Fräser für die Edge cut wählen (rot 0.0315" Router - Square End Mill)
- [ ] Die Elektrische Verbindung zwischen Platine und Messingleiste herstellen
- [ ] Den Knuppel zum spannen nach links schieben
- [ ] Das Kugellager von der Frässpitze aus aufschieben
- [ ] Den Fräser mit der Magnetplatte in die Spannvorrichtung stecken
- [ ] Den Knuppel nach rechts schieben und festen Sitz kontrollieren
- [ ] Die Platinenoberfläche mit Öl benetzen, ggf die Späne absaugen
- [ ] Den Edge cut starten
- [ ] Den Arbeitsplatz aufräumen und die Prometheus reinigen.



[![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/nachoben.svg)](#Prometheus) 

-------------------------------------------------------------



Die ProCAM Startseite

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/ProCAM20.png)

Ein Beispiel verschiedener Pad-Durchmesser und Leiterbahnbreiten

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/ProCAM21.png)

Das Fräser und Bohrer Starter Pack

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/prom20.jpg)

Verfügbare Bits im Lab

- 0.0315" Router (rot)

- 5-mil 15° Carving Bit (blau)

- 0.0197" Square End Mill

- 0.0945" Square End Mill

- 0.85mm Drill Bit (lila)

- 1.2mm Drill Bit

- 2.3mm Drill Bit

- 0.125" Drill Bit





Für den Test wurden "Blau, Lila und Rot" verwendet

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/prom21.jpg)



Die Krokodilkemme wird zur Abstands-Kalibrierung der Platine zum Fräser benötigt

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/prom22.jpg)

Die Fräser-Aufnahme

![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/prom23.jpg)




[![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/nachoben.svg)](#Prometheus) 


-------------------------------------------------------------


#### Link zu Zippyrobotics
[Home](https://www.zippyrobotics.com/)

#### ProCam download
[Download](https://www.zippyrobotics.com/download/)

#### How To Videos and Guides
[walk trough](https://www.zippyrobotics.com/how-to/)
<br> <br>

[![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/nachoben.svg)](#Prometheus)

-------------------------------------------------------------


## Oberlab Wiki (Danke an Sepp)

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



[![image](https://github.com/frankyhub/Prometheus/blob/main/Pix/nachoben.svg)](#Prometheus) 

-------------------------------------------------------------


