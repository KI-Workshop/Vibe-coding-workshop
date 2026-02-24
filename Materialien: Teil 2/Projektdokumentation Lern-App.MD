

# Projektspezifikation: Lern-Quiz Studio

## 1. Konzept und Zielsetzung
Das **Lern-Quiz Studio** ist eine Single-Page-Application (SPA), die als universelles Werkzeug zur Erstellung, Bearbeitung und Durchführung von Lern-Quizzes dient. Die Anwendung benötigt keine Datenbank und speichert alle Informationen lokal im Browser des Nutzers. Der Fokus liegt auf der KI-gestützten Generierung von Inhalten und dem Export als eigenständige, portable HTML-Dateien.

## 2. Die drei Hauptmodi

### Modus 1: Erstellen (AI-Chat & Generator)
Dies ist die Einstiegsseite der Anwendung (entspricht Screenshot 1).
*   **Zentrale Benutzeroberfläche:** Eine große Karte bietet Schnellstart-Optionen: „Foto von Buchseite“, „PDF-Inhalt kopieren“, „Thema eingeben“ und „Lückentext erstellen“.
*   **KI-Interaktion:** Am unteren Bildschirmrand befindet sich eine Chat-Leiste („Nachricht an Quiz-Assistent...“). Hier können Nutzer Materialien hochladen oder Anweisungen geben.
*   **Automatischer Workflow:** Sobald die KI (z. B. Gemini) einen Test generiert hat, wird dieser im Hintergrund als **JSON-Objekt** strukturiert und automatisch in den **Bearbeiten-Modus** übertragen.

### Modus 2: Bearbeiten (Editor & Konstruktor)
In diesem Modus wird der Test verfeinert und verwaltet (entspricht Screenshot 2).
*   **Zweigeteiltes Layout:**
    *   **Links (Quiz-Einstellungen & Fragen):** Hier werden Titel und Beschreibung festgelegt. Darunter befinden sich die Fragen-Karten. Jede Karte enthält Felder für die Frage, drei Antwortmöglichkeiten (A, B, C), Radio-Buttons für die korrekte Lösung sowie optionale Felder für „Begründung“ und „Zitat aus dem Text“.
    *   **Rechts (Quiz-Assistent):** Ein seitliches Chat-Fenster erlaubt es, der KI spezifische Änderungswünsche für einzelne Fragen zu senden (z. B. „Mach Frage 3 schwerer“).
*   **Daten-Management:**
    *   **JSON Speichern/Importieren:** Buttons zum Herunterladen des aktuellen Tests als `.json`-Datei und zum Hochladen vorhandener Test-Dateien vom Computer.
    *   **Frage hinzufügen:** Ein Button am Ende der Liste erlaubt das manuelle Erstellen neuer Fragen.
*   **Standard-Beispiel:** Beim ersten Öffnen ist stets die Frage „Was ist die Hauptstadt von Deutschland?“ (Berlin) als Vorlage geladen.

### Modus 3: Vorschau (Player für Schüler)
Dies ist die Ansicht, die der Endnutzer (Schüler) sieht (entspricht Screenshot 3).
*   **Startbildschirm:** Zeigt Titel, Beschreibung und die Anzahl der Fragen. Ein prominenter Button „Quiz Starten“ leitet den Test ein. Nach dem Klicken erscheint ein Test aus dem Editor.
*   **Interaktiver Test:**
    *   Keine Editor-Funktionen oder Chat-Fenster sichtbar.
    *   Ein-Fragen-Logik mit Fortschrittsbalken.
    *   Ergebnisseite mit Score-Tracking und Review-Option (Begründungen anzeigen).
	
	**Ziel:** Selbstüberprüfung. Nach Abschluss werden Ergebnis und Bewertung angezeigt.
*   **Fehlerüberprüfung:** SCHALTFLACHE HINZUFÜGEN „Falsche Antworten“ (rot) und „Richtige Antworten“ (grün). Beim Klicken wird die Frage, die richtige Antwort und (bei Fehlern) die Wahl des Schülers angezeigt. 
*   **Formatierung:** Die Beschriftungen (z. B. „✓ Richtige Antwort“) sind farbig, der eigentliche Antworttext ist immer schwarz.
*   **Begründung** (normaler Text) unter der speziellen Schaltfläche „Begründung anzeigen” in neutralem Grau. Die Begründung ist deutlich als „Begründung” zu kennzeichnen, gefolgt von einem Doppelpunkt und dem Text darunter. Das Zitat ist als „Zitat aus dem Text” zu kennzeichnen. Die Benutzeroberfläche muss für den Benutzer so verständlich wie möglich sein.

*   **Export-Optionen:** Unter dem Start-Button befinden sich die Links „Als HTML herunterladen“ (generiert die Standalone-Datei)

Die Anwendung basiert auf dieser eigenständigen Seite:
https://stadtmenschen-stadtv-gel-quiz-74040208660.us-west1.run.app/

## Die Navigationsleiste mit den Schaltflächen „Erstellen“, „Bearbeiten“ und „Vorschau“ befindet sich am oberen Bildschirmrand, um dem Nutzer jederzeit einen schnellen und bequemen Wechsel zwischen den drei Hauptmodi zu ermöglichen.

## 3. Technische Anforderungen & Logik

### Persistence (F5-Schutz)
*   Die Anwendung nutzt den `localStorage` des Browsers. Bei jeder Änderung im Editor wird der aktuelle Zustand gespeichert.
*   **Verhalten bei Refresh:** Drückt der Nutzer F5, wird der Test nicht gelöscht, sondern automatisch aus dem `localStorage` wieder in den Editor geladen.

### Datenstruktur (JSON)
Der Austausch zwischen den Modi basiert auf einem standardisierten JSON-Format:
```json
{
  "title": "Mein Erstes Quiz",
  "description": "Erstellt mit Lern-Quiz Studio",
  "questions": [
    {
      "question": "Was ist die Hauptstadt von Deutschland?",
      "options": ["München", "Berlin", "Hamburg"],
      "answer": 1,
      "explanation": "Berlin ist die Hauptstadt...",
      "quote": ""
    }
  ]
}
```

### Standalone-Export
*   Beim Klick auf „Als HTML herunterladen“ wird eine neue Datei generiert, die das CSS, das JavaScript für den Player-Modus. Diese Datei funktioniert komplett offline.

## 4. Design-Vorgaben
*   **Stil:** Modernes Card-Design mit weichen Schatten und abgerundeten Ecken (15px).
*   **Farben:** Hintergrund in hellem Grau (`#f4f7f6`), Primärfarbe Blau (`#3498db`), Erfolg in Grün (`#27ae60`).
*   **Typografie:** Serifenlose, klare Schriftarten für optimale Lesbarkeit auf allen Geräten.

## 5. Bewertungsskala (für den Player)
*   **0-3 Punkte:** Noch Übungsbedarf. Lies den Text noch einmal durch.
*   **4-7 Punkte:** Gutes Verständnis! Vertiefe Details für noch bessere Ergebnisse.
*   **8-10 Punkte:** Hervorragend! Du hast das Thema sehr gut verstanden.

---
**Diese Dokumentation dient als exakte Vorlage für die Codegenerierung in Google AI Studio.**


