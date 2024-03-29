﻿# Monster Trading Card Game (MTCG)

## Projektbeschreibung
Das Monster Trading Card Game (MTCG) ist ein Kartenspiel, in dem Spieler Karten sammeln, tauschen und gegen andere Spieler antreten
können. Die Spieler erstellen Decks aus ihren Karten und nutzen diese, um in Kämpfen gegeneinander anzutreten.


## Funktionen

### Benutzerregistrierung und -verwaltung
Benutzer können sich im Monster Trading Card Game registrieren, indem sie einen Benutzernamen und ein Passwort angeben. 
Nach der Registrierung können Benutzer sich anmelden und erhalten ein Token, das für zukünftige Anfragen verwendet wird. 
Spieler können ihre persönlichen Daten wie Namen, Bio und Bild bearbeiten. Zum Schluss können sie sich auch abmelden, 
wodurch ihr Authentifizierungstoken ungültig wird.

### Kartensammlungen und Deckerstellung
Spieler können Kartenpakete erwerben, um ihre Sammlung zu erweitern. Jedes Paket enthält eine zufällige Auswahl an Karten. Spieler können 
ihre gesammelten Karten einsehen und aus diesen ein Deck zusammenstellen, das in Kämpfen gegen andere Spieler verwendet wird. 

### Kampfsystem
Spieler können gegen andere Spieler im Spiel antreten. Ein automatisiertes System wählt einen Gegner aus und führt den Kampf durch. 
Nach dem Kampf erhalten die Spieler ein detailliertes Protokoll, das die Aktionen und das Endergebnis aufzeigt. 
Spieler können ihre eigenen Statistiken wie die Anzahl der gewonnenen und verlorenen Kämpfe einsehen, zudem gibt es ein Scoreboard,
wo die Spieler nach Elo-Rating sortiert werden.

### Kartenhandelssystem
Spieler haben die Möglichkeit Handelsangebote im Spiel zu erstellen, einzusehen und darauf zu reagieren. 
Sie können eigene Karten zum Handel anbieten und spezifische Anforderungen für den Handel festlegen. 
Spieler können Handelsangebote anderer Spieler einsehen und eigene Karten im Austausch anbieten. 
Eigene Handelsangebote können auch zurückgezogen werden.


## Installation und Ausführung

### Voraussetzungen
- Java (JDK 11 oder neuer) 
- Apache Maven (Version 3.6.3 oder neuer)
- PostgreSQL Datenbank (Version 12 oder neuer)

### Schritte zur Einrichtung

1. **Klonen des Git-Repositorys**
    - Öffnen Sie ein Terminal oder eine Eingabeaufforderung.
    - Führen Sie den Befehl aus: `git clone https://github.com/magnusgoeppel/MTCG`.

2. **Vorbereiten der Datenbank**
    - Erstellen Sie einen neuen Benutzer mit dem Namen `admin` und dem Passwort `1234` in PostgreSQL 
      oder passen Sie die Variablen `admin` und `passwort` in der Datei `org.mtcg.Database.DatabaseSetup` 
      auf ihre SQLPostrgres Benutzerdaten entsprechend an.
     - Erstellen Sie eine neue Datenbank mit dem Namen `mtcg` in PostgreSQL, 
       beachten Sie dabei das der Benutzer alle Rechte auf die Datenbank hat.

3. **Kompilieren des Projekts**
    - Navigieren Sie in das Hauptverzeichnis des Projekts über das Terminal oder die Eingabeaufforderung.
    - Führen Sie den Befehl aus: `javac Main.java`.

4. **Starten des Servers**
    - Starten Sie den Server mit dem Befehl: `java org.mtcg.Main`.

### Ausführen der Anwendung
- Nach dem Start können Sie die REST API über die URL `http://localhost:10001/` erreichen.
- Verwenden Sie `curl` um HTTP-Anfragen an die REST API zu senden. Im Verzeichnis `test` befinden sich zwei `curl`-Skripte, 
  die die Funktionalität der REST API demonstrieren, eines davon mit Ausgabe der HTTP-Header und Pausen zwischen den Anfragen und eines ohne.
- Zudem befindet sich im Verzeichnis `test` die Datei `mtcg-api.yaml`, welche die REST API beschreibt und 
  ein Überblick über die verfügbaren Endpunkte gibt.
