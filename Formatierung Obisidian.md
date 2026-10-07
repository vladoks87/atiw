# Formatierung für Obsidian-Unterlagen

Diese Datei beschreibt, wie Unterrichtsunterlagen, PDFs und Zusammenfassungen für meinen Obsidian-Vault aufbereitet werden sollen.

## Überschriften-Hierarchie

- `###` = Block / Hauptabschnitt, z. B. `### Block 5`
- `####` = echtes Überthema innerhalb des Blocks, z. B. `#### Software-Ergonomie`
- `#####` = nur für echte, klar abgegrenzte Unterthemen verwenden

## Grundregel zur Übersichtlichkeit

**Überschriften sparsam einsetzen.**

Nicht jeder einzelne Punkt, Schritt oder Begriff soll eine eigene Überschrift bekommen. Zu viele `#####`-Überschriften machen die Notiz unübersichtlich.

Stattdessen:

- **Abläufe und Schrittfolgen** als nummerierte Listen darstellen
- **Vergleiche, Merkmale, Normen, Kategorien und Beispiele** bevorzugt als Tabellen darstellen
- **kleine Unterpunkte** mit Fettschrift hervorheben
- Aufzählungen verwenden, wenn mehrere kurze Aspekte zu einem Thema gehören
- `#####` nur verwenden, wenn tatsächlich ein eigenes Unterthema beginnt

### Beispiel: vermeiden

```md
#### Vorgehen bei einer Testplanung

##### 1. Software und Testbereich festlegen
...

##### 2. Qualitätsanforderung bestimmen
...

##### 3. Testziel formulieren
...
```

### Beispiel: bevorzugt

```md
#### Vorgehen bei einer Testplanung

1. **Software und Testbereich festlegen**
   - Software
   - Zweck
   - Zielgruppe
   - Testbereich

2. **Qualitätsanforderung bestimmen**
   - funktionale Eignung
   - Benutzbarkeit
   - Zuverlässigkeit

3. **Testziel formulieren**
   - konkret festlegen, was überprüft werden soll
```

## Tabellen bevorzugen, wenn sie Übersicht schaffen

Tabellen sind besonders geeignet für:

- Normen und deren Bedeutung
- Qualitätsmerkmale
- Vor- und Nachteile
- Begriffe mit Erklärung und Beispiel
- Gegenüberstellungen
- Testarten und Testverfahren
- Merkmale mit Messgrößen oder Akzeptanzkriterien

Beispiel:

```md
| Merkmal | Bedeutung | Beispiel |
|---|---|---|
| Fehlertoleranz | Fehler sollen korrigierbar sein | Undo-Funktion |
| Steuerbarkeit | Nutzer kann den Ablauf beeinflussen | Abbrechen / Zurück |
```

## Allgemeine Formatierungsregeln

- Abschnitte sinnvoll mit `---` trennen
- Fokus auf **Übersichtlichkeit und Lernbarkeit**
- Inhalte nicht einfach 1:1 aus der Quelle abschreiben, sondern sinnvoll strukturieren
- Formeln sauber in Markdown/LaTeX formatieren
- Code immer in passenden Codeblöcken darstellen
- Callouts wie `> [!info]`, `> [!summary]` oder `> [!warning]` nur verwenden, wenn sie einen echten Mehrwert bieten
- Keine Emojis verwenden, außer sie sind ausdrücklich gewünscht
- Keine unnötigen Wiederholungen
- Beispiele kurz und prüfungsnah halten

## Bilder

- Bilder, die eingebunden werden sollen, im Ordner `Images_Files` speichern
- In Markdown mit Obsidian-Syntax referenzieren, z. B.:

```md
![[Images_Files/Dateiname.png]]
```

- Grafiken nur übernehmen oder neu erstellen, wenn sie den Inhalt wirklich verständlicher machen

## Querverweise

Wo sinnvoll, Querverweise zwischen Themen, Blöcken und Unterrichtsfächern anlegen.

Beispiele:

```md
[[ISO IEC 25010]]
[[Softwareergonomie]]
[[Testplanung]]
```

Querverweise nur setzen, wenn das Zielthema tatsächlich sinnvoll zusammenhängt; nicht künstlich jeden Begriff verlinken.

## Zielbild

Die fertige Obsidian-Notiz soll:

- auf einen Blick erfassbar sein
- möglichst wenig verschachtelte Überschriften enthalten
- Tabellen für strukturierte Informationen nutzen
- Listen für Abläufe verwenden
- wichtige Begriffe durch **Fettschrift** hervorheben
- kompakt genug zum Lernen sein
- trotzdem alle prüfungsrelevanten Inhalte der Quelle enthalten

**Priorität bei der Formatierung:**

1. Übersichtlichkeit
2. Lernbarkeit
3. Vollständigkeit der relevanten Inhalte
4. Nähe zur Struktur der Quelle
