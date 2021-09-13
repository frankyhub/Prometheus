# Prometheus

### 4 Kanal LL
![image](https://github.com/frankyhub/Prometheus/blob/main/4Kanal-LL.jpg)

### Zippyrobotics
[Home](https://www.zippyrobotics.com/)

### ProCam
[Download](https://www.zippyrobotics.com/download/)

### Videos
[How to](https://www.zippyrobotics.com/how-to/)


### Checkliste


Kicad:
Große Pads

Gleich große Bohrlöcher

Große Leiterbahn Abstände

Plotter Eistellungen ändern

Leerzeichen löschen

Fräse:

![image](https://user-images.githubusercontent.com/61152841/133024511-c466d947-787a-40c3-9472-26b9eed16f23.png)
Platine mit doppelseitigen Klebeband mit 4 Reihen fixieren

![image](https://user-images.githubusercontent.com/61152841/133024515-001684ac-5d6f-4b46-9c72-55bb76597786.png)
Elektrische Verbindung zwischen Platine und Messingleiste herstellen 

![image](https://user-images.githubusercontent.com/61152841/133024522-5fab964f-aaa8-4713-85e9-57dde7770782.png)
Platinenoberfläche mit Öl benetzen

![image](https://user-images.githubusercontent.com/61152841/133024531-b6bcf558-6b07-4c51-828f-82c20d6c0feb.png)
Werkzeug spannen

![image](https://user-images.githubusercontent.com/61152841/133024533-dcb9017f-0364-4cfe-9347-7ef49f8077b7.png)
0,015 Fräser spannen 

![image](https://user-images.githubusercontent.com/61152841/133024536-e52bad55-eab8-471a-87a5-1ce290256fed.png)
Knuppel zum spannen nach links schieben 

![image](https://user-images.githubusercontent.com/61152841/133024541-81a7718d-7cee-46bf-a23b-57a314270ab3.png)
Kugellager von der Frässpitze aus aufschieben

![image](https://user-images.githubusercontent.com/61152841/133024543-dc8c29bc-0964-419d-b68b-318c637d514a.png)
Mit der Magnetplatte in die Spannvorrichtung stecken

![image](https://user-images.githubusercontent.com/61152841/133024547-b27df3cc-3e32-4db9-9898-bb9f91e55c84.png)
Knuppel nach rechts schieben

![image](https://user-images.githubusercontent.com/61152841/133024548-d963c83f-8696-4655-907c-b67786ce2e42.png)
Dateien laden

![image](https://user-images.githubusercontent.com/61152841/133024550-43bfecbb-2d55-4efe-857a-908e5ac23af5.png)
Fräsvorgang Starten

![image](https://user-images.githubusercontent.com/61152841/133024554-6d22cf59-ebc8-4b23-8df0-98c30efd95a3.png)
Fräser  Bohrlöcher wechseln

![image](https://user-images.githubusercontent.com/61152841/133024558-cd75e04c-3322-4734-8dcb-7b49291d75e6.png)
Bohren starten 

![image](https://user-images.githubusercontent.com/61152841/133024561-67c260a9-7973-48d2-9fb9-b8f7c7e467e1.png)
Fräser Edge cut wechseln

![image](https://user-images.githubusercontent.com/61152841/133024566-3b09abe0-b3cc-4cee-84d9-db570f43acb1.png)
Öl aufbringen 

![image](https://user-images.githubusercontent.com/61152841/133024569-1b5b8a5e-05e9-4a84-93ba-5c49f94c6701.png)
Cutten starten




### Wiki

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


###Anleitung
1. Produktionsdaten vorbereiten
2. 
Ursprungspunkt des Rasters und Offset für Bohrungen auf einen Punkt der Zeichnung (selber Punkt für beide) platzieren, sodass die Zeichnung vollständig rechts oberhalb dieses Punktes liegt.


2. Produktionsdaten exportieren
3. 
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


