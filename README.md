Name des Projekts:	Unit Testing & Logging mit Logistische Regression

Link zum MyBinder: 	[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/HuseyinBgn/UnitTestAndLogging/HEAD)

Doku:	

Die Beispiele der Übungsaufgabe befinden sich in dem Logistische_Regression.ipynb Datei.
Die erwarteten Ergebnisse sind unterhalb der jeweiligen Befehle dargestellt. 

Hinweis: Um das erwartete Ergebnis nicht zu verlieren wird empfohlen eine Zwischenzeile zw. dem Befehl 
und dem bereits stehendem Ergebnis hinzufügen bevor das Befehl ausgeführt wird!

Zum Ausführen der einzelnen Code-Zeilen "STRG" + "Enter" Tasten drücken.
Beachten Sie keine der Zeilen zu überspringen, denn sonst kann es zu Fehlerhaften Ausführung führen.

1. Libraries installieren & importieren: 
- Librairies für die Datenverarbeitung und -visualisierung werden installiert und anschließend importiert.

2. Die Daten:
- Advertising.csv Datei wird gelesen.

3. Die my_logger und my_timer Methoden:
- my_logger() und my_timer() Methoden werden hier vorerst definiert.
- Sie dienen dazu, dass 

4. Logistische Regression:
- Die Daten werden in Trainings und Testset aufgeteilt.
- Die fit() Methode wird überschrieben. Dabei werden my_logger und my_timer Methoden angewendet.
- In fit() Methode wird das Regressionsmodell mit Testdaten trainiert. Das Ergebnis wird in fitted gespeichert.
- Die predict() Methode wird ebenso überschrieben. Hier werden ebenso my_logger und my_timer Methoden angewendet.
- In predict() Methode soll das Regressionsmodell vorhersagen. Das ergebnis wird in predictions gespeichert.
- Zum Schluss wird das Ergebnis mit Anwendung der überschriebenen fit() und predict() Methoden angezeigt.

5. Anwendung der Testklasse:
- Klasse TestInput wird erstellt.
- Die Klasse beinhaltet setUpClass(), tearDownClass(), setUp(), tearDown(), test_fit() und test_predict() Methoden.
- Die setUp() Methode wichtigste von allen, denn hier werden die Erwartungen festgelegt und an test_fit() und test_predict() Methoden übertragen.
 
- Kurs Design Testfall 1:
	- Die Methode test_predict() beschreibt den Tetsfall 1 aus dem Kursdesign.
	- Es stellt die Accuracy und den Konfusionsmatrix des Regressionsmodels mit den erwarteten Werten der setUp() Methode.
	- Die Gegenüberstellung erfolgt mit assertEqual() Methode der Unittest Library. Sind sie identisch, so ist der Test erfolgreich.
	- Genau das was ausgegeben wird, wird auch in einer Testdatenfile_Predict.txt Datei im selben Ordner gespeichert.
	- In unserem Beispiel kann man herleiten, dass das Regressionsmodell den erwarteten Ergebnis ausgibt.

- Kurs Design Testfall 2: 
	- Die Methode test_fit() beschreibt den Testfall 2 aus dem Kursdesign.
	- Es stellt die Dauer des Trainingzeit von dem Regressionsmodell mit der erwarteten Dauer aus der setUp() Methode gegenüber.
	- Die Gegenüberstellung erfolgt mit assertEqual() Methode der Unittest Library. Sind sie identisch, so ist der Test erfolgreich.
	- Genau das was ausgegeben wird, wird auch in einer Testdatenfile_Fit.txt Datei im selben Ordner gespeichert.	