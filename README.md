# DB-Test
## Aufgabe 1
Stelle Entitäten mittels Chen-Notation und Min,Max Notation dar.
Wähle ein sinnvolles Beispiel!
  ## Aufgabe 2
  Kann eine Beziehung Attribute haben?
  - Ja!
  - Wie bei Entitäten: man schreibt es in eine Blase und verbindet diese mit einem Strich mit der Beziehung.
  ## Aufgabe 3
  Welche Codd'schen Anforderungen gibt es (Nenne mindestens 5)
    ---Abgeschrieben---
  - Bentzuersichen: Verschiedene Ansichten für versch. Benutzer
  - Integration: einheitliche, nicht redundante Datenverwalung
  - Katalog: Einsichten in die Datenbeschreibung (Data Dictionary)
  - Operationen: Sichern, Suchen, Einfügen, Ändern
  - Datensicherung: Wiederherstellen von Daten nach Systemfehlern
  - Synchronisation: Das Handling von gleichzeitigem Zugriff zweier Benutzer
  - Transaktion: Verschiedene Operationen als Funktionsgruppen
  - Integritätssicherung: Korrektheit des Datenbestandes
  - Zugriffsrecht: Unbefugten Zugriff von Außen verhindern
  ## Aufgabe 4
  Nenne den Unterschied zwischen Konzeptuellen und Logischem Schema
  - Das konzeptuelle Shema ist die Schriftliche "Angabe". Man Fasst das Problem in Worte.
  - Das logische Schema ist das "Endprodukt". Die Werte in Tabellen und die Beziehungen der Tabellen untereinander.
  ## Aufgabe 5
  Welche 3 Bestandteile gibt es im Entity Relationship Model
  - Entitäten
  - Atribute
  - Beziehungen
  ## Aufgabe 6
  Welche Datentypen gibt es in MySQL? (Nenne mindestens 5)
  - varchar(32)
  - date
  - int
  - float
  - boolean
  ## Aufgabe 7
  Welche Arten von Schlüsseln gibt es und welche Eigenschaften besitzen diese?
  - Primärschlüssel: Ein Tupel (Eine einzelne Zeile der Datenbank) ist eindeutig durch den Prmärschlüsse identifizierbar.
  - Sekundärschlüssel: Verweist auf eine andere Tabelle
  ## Aufgabe 8
  Welche Arten von Beziehungen gibt es? Zeichne für jede ein Beispiel auf
  - Onäre
  - Binäre
  - Trinäre
  -  --> Siehe Bild "Aufgabe 8 Witt 23.09."
  ## Aufgabe 9
  Was bedeutet der Begriff Kardinalität und welche Kardinalitäten gibt es?
  - 1:1 - Eine Mensch kann einen Führerschein haben, Ein Führerschein kann nur einem Menschen gehören
  - 1:n - Ein Mensch kann mehrere E-mail-Adressen haben, aber eine E-mail-Adresse gehört nur einem Menschen
  - n:n - Ein Lied hat viele Akkorde, ein Akkord kann in mehreren Lieder vorkommen
  ## Aufgabe 10
  Was bedeutet der Begriff Datenintegrität und worin unterscheidet sich Integrität und referentielle Integrität?
  - Integrität beschreibt die Richtigkeit der Daten. Die referentielle Integrität beschreibt die Richtigkeit der Beziehungen.
  ## Aufgabe 11
  Erkläre die 3 Normalformen
   1. Normalform: In einer Tupel darf nicht mehr als ein Wert stehen (atomarisierung)
   2. Normalform: Wenn ein vom Primärschlüssel abhängiger Wert mehrmals vorkommt, wird er herrausgenommen und bekommt eine eigene Tabelle
   3. Normalform: Wenn nicht vom Primärschlüssel abhänige Werte mehrmals vorkommen, bekommen sie eine eigene Tabelle
  ## Aufgabe 12
  Erkläre den Unterschied zwischen starken und Schwachen Entitäten und erstelle ein Beispiel.
  Starke Entitäten sind durch einen eigenen Primärschlüssel eindeutig identifizierbar. Schwache Entitäten sind nur mittels Fremschlüssel (verweis auf eine andere Entität)
  eindeutig identifizierbar
## Aufgabe 13
Welche Grundregeln gibt es im Relationenmodell? (Nenne mindestens 4)
  ## Aufgabe 14
  Wie löst man eine M:N Beziehung auf? Erstelle ein Beispiel
  Man fügt eine Tabelle ein. Bei den Entitäten steht dann ein 1, bei der Tabelle ein n.
   --> Siehe Bild "Aufgabe 14 Witt 23.09."
## Aufgabe 15
Ein Handelsbetrieb verkauft ein Sortiment von Artikeln, die er von verschiedenen Herstellern bezieht. Der Handelsbetrieb hat einen 
bestimmten Kundenkreis, der regelmäßig Bestellungen aufgibt. Eine Bestellung kann mehrere Artikel umfassen. Ein Artikel kann von 
mehreren Lieferanten bezogen werden und ein Lieferant liefert natürlich meist mehr als einen Artikel. Erstelle ein ERD und ein 
Relationenmodell, welches der 3. Normalform entspricht.
    --> Siehe Bild "Aufgabe 15 erd Witt 23.09."
  ## Aufgabe 16
  Welche Anomalien kennst du und was beschreiben sie?
  - Insert-Anomalie - Wenn man einen neuen Eintrag anlegt, aber zb nichts in den Primärschlüssel einträgt.
  - Update-Anomalie - Wenn man was neues in die Tabelle schreibt und dadurch einen "Doppeleintrag" erhällt
  - Delete-Anomalie - Wenn man ein Objekt löscht, aber andere Objekte damit verbunden sind (oder diese Objekt zur identifikation braucht (schwache Entität))
## Aufgabe 17
Modellieren Sie den angeführten Realitätsausschnitt einer Fluggesellschaft mit Hilfe eines Entity Relationship- Diagramms. Treffen Sie, falls notwendig, sinnvolle Annahmen und dokumentieren Sie diese nachvollziehbar in Ihrer Lösung. Der zu betrachtende Realitätsausschnitt der Fluggesellschaft umfasst folgenden
Sachverhalt:
Flughäfen haben ein Kürzel (= Schlüssel) und gehören zu einer Stadt (z.B. „FRA“ für Frankfurt, „FCO“ für Roma Fiumicino).
Flüge haben eine Flugnummer (z.B. „LH 306“), führen von einem Flughafen zu einem anderen, mit jeweils einer festen Abflugs- und Ankunftszeit (z.B. ab Frankfurt um 07:30 nach Roma Fiumicino mit Ankunft um 09:15).
Jeder Flugzeugtyp hat einen Namen (z.B. „747-400“) und eine Sitzanzahl (z.B. 430 Sitze).
Piloten haben einen Namen (z.B. „Meier“), ein Geburtsdatum (z.B. „1.1.1960“) und eine Berechtigung, bestimmte Flugzeugtypen zu fliegen (z.B. „747-400“ und „A310“).
Jedes einzelne Flugzeug ist von einem bestimmten Flugzeugtyp (z.B. „747-400“) und hat einen Namen (z.B. „Mozart“).
Bei einem Flug-Einsatz wird ein Flug (z.B. „LH 306“) an einem bestimmten Datum (z.B. „6.2.2011“) von einem bestimmten Piloten (z.B. „Meier“) mit einem bestimmten Flugzeug (z.B. „Mozart“) geflogen.
Bilden Sie das konzeptuelle Schema in ein relationales Schema ab. Das relationale Schema soll der 3. Normalform genügen
 --> Siehe Bild "Aufgabe 17 erd Witt 23.09."