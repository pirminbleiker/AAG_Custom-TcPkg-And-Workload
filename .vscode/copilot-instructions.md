# Copilot Instructions (Team)

Diese Datei definiert Team-Konventionen für GitHub Copilot (Chat) in diesem Repository.

## Ziele

- Kleine, reviewbare Änderungen (minimaler Diff).
- Bestehende TwinCAT/PLC-Strukturen respektieren.
- Keine "magischen" Änderungen an Projekt-/Build-Artefakten.

## Repo-Regeln

- Ändere nur Dateien, die für die Aufgabe nötig sind.
- Erfinde keine neuen Architektur-Schichten oder große Refactorings ohne explizite Anfrage.
- Keine GUIDs regenerieren/ändern (z.B. in TwinCAT-Projektdateien), außer ausdrücklich gefordert.
- Behalte bestehende Namenskonventionen, Ordnerstruktur und Datei-Layouts bei.

## TwinCAT / PLC-spezifisch

- Schreibe Structured Text (ST) im Stil des bestehenden Codes.
- Vermeide unnötige Pointer-/Interface-Konplexität; bevorzuge klare, sichere Patterns.
- Berücksichtige Echtzeit-/Determinismus-Anforderungen: vermeide unnötige Allokationen in zyklischem Code.
- Wenn Änderungen Auswirkungen auf den Zyklus haben könnten, weise kurz darauf hin.

## Tests / Verifikation

- Wenn passend: ergänze/aktualisiere TcUnit-Tests im `UnitTest`-Projekt.
- Bei Code-Änderungen: nenne einen konkreten Weg zur Verifikation (Build/Run/Tests), falls möglich.

## Kommunikation

- Stelle maximal 1–3 gezielte Rückfragen, wenn Anforderungen unklar sind.
- Wenn du Annahmen triffst, schreibe sie explizit als "Annahme:".
