# Prompts – iterativer Ansatz

## Das Ziel

Erstelle eine HTML-Seite mit einem Test auf der Grundlage dieses Textes

## Die Eingabedaten

Der Test soll 10 Multiple-Choice-Fragen mit Fortschrittsanzeige, Score-Tracking und Auswertung am Ende. Es soll 3 Antwortmöglichkeiten pro Frage (nur eine richtig) geben. Die Fragen sollen verschiedene Schwierigkeitsgrade haben: 2 einfache, 3 mittlere und 5 schwere.

## Das Endergebnis

Der Test soll einen Titel haben, eine Begründung der richtingen Antwort enthalten und ein Zitat, das die richtige Antwort erklärt. 

## Der Design

Zeige den Schwierigkeitsgrad der Fragen nicht. Die richtigen und falschen Antworten, Begründung und Zitat (als „Zitat aus dem Text” kennzeichnen) und die Punkte sollten nur am Ende des Tests, bei der Überprüfund angezeigt werden. Der Test soll keinen Untertitel haben, nur den Titel. Die Fragen sollten mit „Frage X von Y” gekennzeichnet werden und nicht mit Nummern. Jede Antwortsoption soll eine Buchstabe haben. 

## Die Funktionen

Füge zwei 2 Filter-Schaltflächen am Ende des Tests für richtige und falsche Antworten. Begründung (normaler Text) und das Zitat aus dem Text.   
Füge die Schaltfläche „Test wiederholen”, die zur ersten Seite zurückführt. Begründung (normaler Text) unter der speziellen Schaltfläche „Begründung anzeigen” in neutralem Grau. 

Die Begründung ist deutlich als „Begründung” zu kennzeichnen, gefolgt von einem Doppelpunkt und dem Text darunter. Das Zitat ist als „Zitat aus dem Text” zu kennzeichnen. Die Benutzeroberfläche muss für den Benutzer so verständlich wie möglich sein. 

Zitat (kursiv, mit Anführungszeichen)

Die Ergebnisse werden OHNE Überprüfung geladen (leere Liste). Die Überprüfung erscheint NUR nach Klicken auf den Filter

Am Ende zeige die Ergebnisse und ein Feedback:  
0-3: „Noch Übungsbedarf. Lies den Text noch einmal durch.”  
4-7: „Gutes Verständnis\! Vertiefe Details für noch bessere Ergebnisse.”  
8-10: „Hervorragend\! Du hast das Thema sehr gut verstanden.”

## Das Format

A. Generieren Sie den vollständigen HTML-Code.  
B. Mach den Test im Markdown-Format.

# Prompts – detaillierter Ansatz

Erstelle eine interaktive HTML-Seite für einen Test auf der Grundlage des beigefügten Textes.

**DATEN:**

Verwende die Fragen und Antwortmöglichkeiten aus dem aktuellen Test. Füge für jede Frage Folgendes hinzu:

Erklärung: Warum ist diese Antwort richtig?

Zitat: Ein Zitat aus dem Text (2-3 Sätze), das die Antwort bestätigt.

**STRUKTUR:**

Intro: Überschrift \+ Beschreibung \+ Schaltfläche „Test starten”

Quiz: Fragen einzeln, Fortschrittsbalken, Navigation

Ergebnisse: Punktzahl \+ Filter \+ detaillierte Bewertung

**DESIGN:**

Blaue Farbpalette 

Modern, klar

Abgerundete Ecken, Schatten

Mobilfreundlich

**FUNKTIONALITÄT:**

Fragen:

„Frage X von Y” über der Frage

Fortschrittsbalken zeigt den Fortschritt an

Optionen mit den Buchstaben A, B, C

Bei Auswahl → Hervorhebung \+ „Weiter” auf der rechten Seite oder „Zurück” auf der linken Seite anzeigen (keine "Zurück" bei der ersten Frage)

Letzte Frage: „Ergebnis anzeigen”

Ergebnisse:

Punktzahl „X / 10” groß

Feedback:

0-3: „Noch Übungsbedarf. Lies den Text noch einmal durch.”

4-7: „Gutes Verständnis\! Vertiefe Details für noch bessere Ergebnisse.”

8-10: „Hervorragend\! Du hast das Thema sehr gut verstanden.”

2 Filter-Schaltflächen:

„Falsche Antworten” (rot)

„Richtige Antworten” (grün)

Beim Klicken → aktiver Filter heller \+ Rahmen

\- Ergebnisse werden OHNE Überprüfung geladen (leere Liste)

\- Überprüfung erscheint NUR nach Klicken auf den Filter

Fragenummer \+ Fragetext und der Buchstabe neben der Antwort, wie im Test

✓ Richtige Antwort immer erst (nur die Aufschrift „Richtige Antwort” in grüner Farbe, der Text der Variante darunter in schwarzer Farbe)

✗ Deine Antwort, wenn falsch \- immer zweit (nur die Aufschrift „Deine Antwort” in roter Farbe, der Text der Variante darunter in schwarzer Farbe)

Begründung (normaler Text) unter der speziellen Schaltfläche „Begründung anzeigen” in neutralem Grau. Die Begründung ist deutlich als „Begründung” zu kennzeichnen, gefolgt von einem Doppelpunkt und dem Text darunter. Das Zitat ist als „Zitat aus dem Text” zu kennzeichnen. Die Benutzeroberfläche muss für den Benutzer so verständlich wie möglich sein. 

Zitat (kursiv, mit Anführungszeichen)

Schaltfläche „Test wiederholen”, die zur ersten Seite zurückführt.

**WICHTIG:**

Die Antworten dürfen während des Tests NICHT angezeigt werden.

Begründungen NUR auf results

Nur Labels (✓/✗) in Farbe, Text in Schwarz

Review items mit border-left in Farbe

Generiere den vollständigen HTML-Code.

# Anwendung testen

## Bespiel 1: einen neuen Test erstellen

Erstelle eine Quiz-App mit 10 Multiple-Choice-Fragen zu diesem Text. Mit Fortschrittsanzeige, Score-Tracking und Auswertung am Ende. Die Fragen sollen verschiedene Schwierigkeitsgrade haben: 2 einfache, 3 mittlere und 5 schwere.

Bespiel 2: fertigen Test digital darstellen

Ich habe einen fertigen Test zum Lernmaterial. Die richtigen Antwortvarianten sind mit einem grünen Häkchen markiert. 

Konvertiere diesen Test in ein digitales Format.

# Anwendung erstellen

Hier ist die Projektdokumentation für die Anwendung. Verwende diese, um die Anwendung zu erstellen.  
Die Anwendung ermöglicht es dir, Lern-Tests zu erstellen, zu bearbeiten und durchzuführen.  
Die Anwendung basiert auf dieser eigenständigen Seite:  
[https://stadtmenschen-stadtv-gel-quiz-74040208660.us-west1.run.app/](https://www.google.com/url?sa=E&q=https%3A%2F%2Fstadtmenschen-stadtv-gel-quiz-74040208660.us-west1.run.app%2F)

## Das Ergebnis iterativ verbessern: Bespiel

1\. Im Bearbeiten-Modus:

Stelle "Begründung (Optional)" und "Zitat aus dem Text (Optional)" nebeneinander in zwei gleich breiten Spalten dar. Beide als textarea mit 4-5 Zeilen Höhe und Placeholder-Text.

2\. Im Vorschau-Modus:

Filter-Schaltflächen nach dem Test hinzufügen:

„Falsche Antworten” (rot)

„Richtige Antworten” (grün)

Beim Klicken → aktiver Filter heller \+ Rahmen

\- Ergebnisse werden OHNE Überprüfung geladen (leere Liste)

\- Überprüfung erscheint NUR nach Klicken auf den Filter

Fragenummer \+ Fragetext und der Buchstabe neben der Antwort, wie im Test

✓ Richtige Antwort immer erst (nur die Aufschrift „Richtige Antwort”, Title Case, in grüner Farbe, der Text der Variante darunter in schwarzer Farbe)

✗ Deine Antwort, wenn falsch \- immer zweit (nur die Aufschrift „Deine Antwort”, Title Case, in roter Farbe, der Text der Variante darunter in schwarzer Farbe)

Begründung (normaler Text) unter der speziellen Schaltfläche „Begründung anzeigen” in neutralem Grau. Die Begründung ist deutlich als „Begründung” zu kennzeichnen, gefolgt von einem Doppelpunkt und dem Text darunter. Das Zitat ist als „Zitat aus dem Text” zu kennzeichnen. Die Benutzeroberfläche muss für den Benutzer so verständlich wie möglich sein.

Zitat (kursiv, mit Anführungszeichen)

Schaltfläche „Test wiederholen”, die zur ersten Seite zurückführt.

Alles andere lass unverändert.

## Die Anwendung mit n8n verbinden, um Tests online zu veröffentlichen

Füge eine Integration mit n8n Webhook hinzu, um HTML online zu veröffentlichen.  
Im Modus „Vorschau”:

1. Behalte die vorhandene Schaltfläche „Als HTML herunterladen” bei.

2. Füge darunter eine neue Schaltfläche „Online veröffentlichen”  
   im gleichen Stil hinzu.

3. Beim Klicken auf „Online veröffentlichen”:  
   Modales Fenster anzeigen:

   * Text: „Test wird online veröffentlicht und mit Passwort geschützt”

   * Schaltfläche „Veröffentlichen”

   * KEIN Feld zur Passworteingabe (Passwort wird automatisch generiert)

4. Beim Klicken auf „Veröffentlichen”:

**Schritt 1:** Daten vorbereiten

* HTML-Inhalt übernehmen (derselbe wie für „Als HTML herunterladen”)

**Schritt 2:** An n8n-Webhook senden

* Ladeanzeige „Wird veröffentlicht...” anzeigen

  * Endpunkt: POST ***Eigenen Webhook einfügen***

  * Body: Binäre Multipart-Daten im html Feld

  * Das Passwort wird NICHT gesendet – n8n generiert es selbst

**Schritt 3:** Ergebnis abrufen und anzeigen

* Beispiel für eine Antwort von n8n:  
  {  
  url: "[https://workshops.cre8ter.com/test-1234567890/](https://workshops.cre8ter.com/test-1234567890/)",  
  user: "schueler"  
  password: "ABC123XYZ4"  
  }

  * Nach erfolgreichem Abschluss anzeigen:

    * Überschrift: „Erfolgreich veröffentlicht\!”

    * Text: „Der Test ist jetzt online verfügbar und passwortgeschützt”

    * Link zum Test (anklickbar): \[URL aus der Antwort\]

    * Abschnitt „Zugangsdaten für Schüler:“ (visuell hervorheben)

      * „Benutzername: schueler“

      * „Passwort: \[Passwort aus der Antwort\]“

      * Schaltfläche „Zugangsdaten kopieren” – kopiert in die Zwischenablage:  
        „Link: \[URL\]  
        Benutzername: schueler  
        Passwort: \[Passwort\]”

5. Fehler bearbeiten:

   * Wenn die Anfrage fehlgeschlagen ist, anzeigen:  
     „Fehler beim Veröffentlichen. Bitte versuche es erneut.“

   * Die Schaltfläche „Erneut versuchen“ schließt die Fehlermeldung.

6. Nach erfolgreicher Veröffentlichung bleibt die Schaltfläche „Online veröffentlichen”  
   für die Veröffentlichung neuer Versionen aktiv

7. Für das das modale Ergebnisfenster:

Füge eine Kopierfunktion per Klick für die Felder „Benutzername” und „Passwort” hinzu:

Felder mit Kopierfunktion per Klick:

**\-„Benutzername: schueler”**

Bei Klick auf „schueler” → kopiert „schueler”

Füge einen Hover-Effekt hinzu (Cursor-Zeiger, Hervorhebung)

Zeige nach dem Kopieren eine kurze Animation/ein Tooltip „Kopiert\!” an

**\-„Passwort: \[Passwort\]”**  
Beim Klicken auf das Passwort → kopiert das Passwort  
Füge einen Hover-Effekt hinzu (Cursor-Zeiger, Hervorhebung)  
Nach dem Kopieren „Kopiert\!” anzeigen

**Visuell:**

Benutzername und Passwort müssen klickbar aussehen

Beim Hover: andere Farbe/Unterstreichung

Cursor: Zeiger

Beim Klicken auf den Link muss dieser in einem neuen Tab geöffnet werden

**Wichtig:**

* Verwende NICHT localStorage oder sessionStorage

* Erstelle KEINE ZIP-Dateien

* Fordere KEIN Passwort vom Benutzer an

* Sende einfach HTML als Zeichenfolge

* Zeige sowohl den Benutzernamen („schueler”) als auch das Passwort aus der Antwort an

Alles andere sieht perfekt aus, lass es so, wie es ist. Ersetze nur das, was ich oben beschrieben habe, alles andere bleibt unverändert.

