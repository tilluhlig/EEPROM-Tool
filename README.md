Dieses Projekt enthält die Software zum Auslesen und Konfigurieren des Temperaturmoduls aus https://github.com/tilluhlig/Temperaturmodul.

# > Benutzerhandbuch <

# Das Modul öffnen
![](/images/Bild15.jpg) *das Trennen der beiden Gehäusehälften*
![](/images/Bild25.jpg) *das aufgeschraubte Modul*
![](/images/Bild11.jpg) *das Trennen der beiden Gehäusehälften*


# Bauteile
## Quarz
![](/images/Bild1_2.png) *Mini Uhrenquarz, 32.768 kHz*
![](/images/Bild3_7.png) *Mini Uhrenquarz, 32.768 kHz*
Dieser externe Taktgeber weckt den Atmega in regelmäßigen Abständen. Dabei war die Verwendung eines externen 32 kHz Quarzes ein wesentlicher Schritt zur Senkung des Energieverbrauchs des Temperaturmoduls.  


## EEPROM Slots
![](/images/Bild2_2.png) *H: EEPROM Slots*
![](/images/Bild14_2.png) *EEPROM Slots*
Hier können verschiedene 8 Pin SPI EEPROMs eingesetzt werden, dabei können auch Slots freigelassen werden. Das System erkennt, bei der neuen Erstellung der Speicherverwaltung die Anzahl und Art der EEPROMs selbst. Es wurden 64kBit, 512kBit und 1024kBit EEPROMs getestet.


## Spannungsteiler
![](/images/Bild2_9.png) *3.3V Spannungsteiler mit 160mA*


## Prozessor
![](/images/Bild2_3.png) *O: die Steuerung, ATMEGA 88V-10 PU, Speicher: 8 kByte, SRAM: 1 kByte, EEPROM: 512 Byte*
Der in Abbildung O gezeigte Atmega 88V stellt als stromsparende Variante des Atmega 88 die zentrale Steuereinheit dar. Der Atmega wird über SPI mittels des Programmieranschlusses beschrieben.


## Status LED
![](/images/Bild3_5.png) *die Grüne 5mm standard LED, für Statusinformationen*
 Dabei signalisiert die LED zu Beginn, dass das Modul startet und nach dem Ablauf der 30s Wartefrist (für die Verbindung mit dem PC), dass das Modul den Messvorgang startet.


## Sensoren und Blenden
![](/images/Bild37.jpg) *langer Temperatursensor (1m)*
![](/images/Bild41.jpg) *kurzer Sensor*
![](/images/Bild42.jpg) *L: Blende*
Die Blende aus Abbildung L kann genutzt werden, wenn ein Sensorslot nicht genutzt wird, um diesen zu verschließen. Darüber hinaus, hat die Blende keine Funktion.


## USB/UART Modul
![](/images/Bild2_8.png) *I: das UART/USB Modul, mit XBEE Slot*
![](/images/Bild3_6.png) *J: das UART/USB Modul, mit XBEE Slot*
Das in Abbildung I und Abbildung J dargestellte Modul enthält einen USB Treiber um das Temperaturmodul wahlweise mit dem PC direkt über USB zu verbinden oder aber die Verbindung durch ein optionales XBEE Modul einzurichten.

![](/images/Bild47.jpg) *der USB Slot von außen*

Wenn man ein XBEE Modul (Abbildung K)nutzen möchte, muss der Jumper aus Abbildung G entsprechend eingestellt werden, um UART Anschlüsse des Atmega 88 in Abbildung \ref{Atmega} richtig mit dem USB Modul zu verbinden. Des weiteren regelt das Modul die 5V des USB Anschlusses auf die 3.3V des Temperaturmoduls herunter.


### XBEE Modul Slot
![](/images/Bild8_2.png) *K: XBEE Modul Slot*
	
	
### USB Anschluss
![](/images/Bild8_3.png) *USB Anschluss für die Verbindung mit dem PC*
	
	
### UART Jumper
![](/images/Bild3_9.png) *G: Jumper zum Wechseln der UART Anschlüsse zwischen Modul und USB Modul*
![](/images/Bild8_4.png) *Jumper zum Wechseln der UART Anschlüsse zwischen Modul und USB Modul*
	

## SPI Programmieranschluss
![](/images/Bild2_6.png) *der SPI Programmieranschluss*
![](/images/Bild3_3.png) *der SPI Programmieranschluss*
Das Modul kann über einen 6 Poligen Anschluss Programmiert werden. Beachten Sie dabei, vor dem Programmieren alle EEPROMs in Abbildung H aus dem Modul zu entfernen, um Schäden an den EEPROMs zu vermeiden. 

![](/images/Bild48.jpg) *der SPI Programmieranschluss von außen*


## Stromversorgungsschalter
![](/images/Bild2_5.png) *der Schalter zum Einschalten des Temperaturmoduls*
![](/images/Bild3_8.png) *der Schalter zum Einschalten des Temperaturmoduls*
![](/images/Bild30_2.png) *der Schalter zum Einschalten des Temperaturmoduls*
Dieser Schalter trennt die externe Stromversorgung vom Modul.


## Sensoren Anschlüsse
![](/images/Bild2_4.png) *E: die Anschlüsse für die Sensoren, Klinkenbuchse, 3.5mm, Print mit Schaltkontakt*
![](/images/Bild3_4.png) *F: die Anschlüsse für die Sensoren, Klinkenbuchse, 3.5mm, Print mit Schaltkontakt*
Sensoren können mit entsprechenden 3 Poligen, 3.5mm Klinkensteckern in die, in Abbildung E und Abbildung F dargestellten Klinkenbuchsen eingesteckt und damit genutzt werden. Beachten Sie dabei,das Temperaturmodul vom Strom zu trennen, zum einsetzen und entnehmen der Sensoren. 

Zudem ist zu beachten, bei einer Veränderung der Anzahl der genutzten Sensoren, die Speicherverwaltung des Temperaturmoduls entsprechend anzupassen. Dabei kann der Speicher stets für mehr Sensoren angelegt sein, als dann genutzt werden, andersrum funktioniert es nicht.

![](/images/Bild46.jpg) *eingesteckte Sensoren und Blende*


## Steckbuchse für Gehäuseverbindung}
![](/images/Bild2_7.png) *C: Steckbuchse für die Anbindung der externen Stromversorgung*
![](/images/Bild5_2.png) *D: Steckbuchse für die Anbindung der externen Stromversorgung*
Die in Abbildung C und Abbildung D dargestellte Buchse verbindet das gesamte Modul mit dem Gehäuse beziehungsweise der externen Stromversorgung.


## Auswahlschalter für Messintervalle}
![](/images/Bild3_2.png) *M: Auswahlschalter zum festlegen des Messintervalls*
![](/images/Bild20_2.png) *N: Auswahlschalter zum festlegen des Messintervalls*
Sie können die Messintervalle mit dem in Abbildung M und Abbildung N dargestellten Regler anpassen. 

Nutzen Sie dazu die in Abbildung B dargestellte Schalttafel. Wenn Sie das Intervall verändert haben, muss das Modul zunächst neu gestartet werden, bevor eine Änderung wirksam wird. Am besten ist es jedoch, eine Änderung des Intervalls nur bei ausgeschaltetem Modul vorzunehmen, um Schäden zu vermeiden.

![](/images/Bild22_2.png) *B: die Intervall-tafel für den Auswahlschalter*
Schwarz stellt dabei die Schalterposition dar.


# Stromversorgung
Zur Versorgung des Moduls gibt es eine Reihe von Möglichkeiten, dabei ist zu sagen, das auch weitere Mögliche Quellen über den Block Clipanschluss angeschlossen werden können (von 3.3V bis 24V).

![](/images/Bild36.jpg) *4x Mignon*
![](/images/Bild49.jpg) *A: 3x Mono*
Das Modul aus Abbildung A wird auf der Rückseite des Temperaturmoduls verschraubt, achten Sie dabei darauf, die Gegenstücke im inneren des Temperaturmoduls nicht abzubrechen, um einen Defekt des Temperaturmoduls zu vermeiden.

![](/images/Bild32.jpg) *1x 9V Block*

# Daten auslesen
![](/images/InnenAussen.jpg) *Beispielmessung der Innen- und Außentemperatur, mit eingezeichneter Messunterbrechung*

# Kenngrößen
![](/images/Kenndaten.png) *Ausgelesene Kenndaten des Temperaturmoduls*
![](/images/10MinutenZeitintervall.png) *Zeitmessung für ein 10 Minuten Intervall*
![](/images/Ergebnis3.jpg) *Entwicklung des Stromverbrauchs*

# Datenspeicher einrichten
Die Datenstruktur zum speichern der Messwerte kann in der Software im Register "Datenstruktur anlegen" angelegt werden. Wählen Sie dort die Anzahl der Sensoren, die das Modul unterstützen soll (mehr Sensoren bedeutet weniger Messpunkte) und legen Sie dann die Datenstruktur an.


# EEPROM Testmodul
![](/images/Bild24.jpg) *das EEPROM Testmodul (oben)*
![](/images/Bild27.jpg) *das EEPROM Testmodul (unten)*
Dieses Modul wurde entwickelt um die Kenngrößen von 8 Pin SPI EEPROMs zu bestimmen. Dabei arbeitet das Modul experimentierend bei der Ermittlung der Daten, da die EEPROMs selbst keinerlei Informationen über sich selbst Preisgeben. Zudem kann geprüft werden, ob das EEPROM noch korrekt Arbeitet. Zu Beachten ist, das hierbei Schreibvorgänge vorgenommen werden, die natürlich die Lebenszeit des EEPROM verkürzen.
