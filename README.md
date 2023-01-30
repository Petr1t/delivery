# delivery
In diesem kleinen Projekt sollen Geo-Daten und Trinkgelder analysiert werden.

Als Lieferant bin ich in Wuppertal mit einem E-Bike unterwegs. Für mehrere Stunden fahre ich also verschiedenste Adressen rund um den Stadtteil Elberfeld an, parke dort mein Rad, übergebe die Bestellung an die Kund:in und fahre zurück zum Standort("Hub").

Etwa Mitte Oktober 2022 begann ich diesen Job. Bald darauf kam mir die Idee, dass ich doch die Wegdaten erheben und analysieren könnte. Wuppertal ist bekannt für seine Berge, die natürlich erklommen werden möchten. Mit einigen Erwartungen, aber ohne konkrete Vorstellungen begann ich also das Tracking der Geo-Daten während meiner Lieferungen.

# Erhebung der Daten
Vor der ersten Lieferung meiner Schicht starte ich meine Tracking App. Ich nutze dafür die App "Sportactive" aus dem App-Store(https://play.google.com/store/apps/details?id=com.sportractive&hl=de&gl=US) und benutze ein Motorola G5 mit Android 8.1.0. Die App ist so eingestellt, dass alle 15 Sekunden ein Gps-Standort aufgezeichnet werden soll, was allerdings nicht immer klappt. Daraus resultieren auch Messungenauigkeiten, mit denen im Code umgegangen werden muss. Die App bietet sich an, da sie den Export der Strecke als gpx File möglich macht.

Neben den Geo-Daten sind auch die Trinkgelder interessant. Während der Arbeit habe ich mir oft die Frage gestellt, an welchen Tagen besonders viel Trinkgeld anfällt und an welchen weniger. Solche und ähnliche Fragen wollte ich klären, auch wenn ich natürlich schon ein Bauchgefühl entwickelt hatte und eine Tendenz sehen konnte. Trotzdem ist es spannend dieses Gefühl anhand der harten Fakten zu überprüfen.

# Ausführung des Codes
Zu Beginn sollte das "flink_gpx" File ausgeführt werden, da hier die Geo-Daten bearbeitet werden und diese dann später in das zweite File "flink" übertragen werden.

Es ist auch zu beachten, dass ein relativer Filepath für das einlesen der GPX-Daten verwendet wird. Damit das Programm fehlerfrei laufen kann, müssen diese im Ordner "daten" liegen.

Im Rahmen der Analyse der Geo-Daten habe ich auch eine Map aus allen GPX-Datenpunkten erstellt. Da es sich hier um Datenpunkte, die mehr als hundert Fahrt-Stunden umfassen, handelt, sind die Maps entsprechend groß geworden (etwa 40MB). Die entsprechenden Zeilen, die diese Maps erstellen, habe ich auskommentiert, um bei der Ausführung des Codes den Flow nicht zu behindern. Dasselbe habe ich auch mit den einzelnen Graphen, die die Datenpunkte einer Schicht beinhalten, getan.

# Kommendes
Weiterhin werde ich die Fahrten bei meinen Schichten tracken und die neuen Daten in die Analyse einspeisen.

Hinzu kommt, dass nun ein neues E-Bike Modell eingeführt worden ist. Sobald ich einige Schichten mit dem neuen Modell gearbeitet habe, werde ich einen Vergleich der beiden Bikes anstellen und hier hochladen. Bleibt gespannt ;)
