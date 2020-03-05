# DB-Test
## Aufgabe 1
Stelle Entitäten mittels Chen-Notation und Min,Max Notation dar.
Wähle ein sinnvolles Beispiel!
  ## Aufgabe 2
  Kann eine Beziehung Attribute haben?
  - Ja!
  Wenn ja, wie stelle ich es im ERD dar?
  - Wie bei Entitäten: man schreibt es in eine Blase und verbindet diese mit einem Strich mit der Beziehung.
  ## Aufgabe 3
  Welche Codd'schen Anforderungen gibt es (Nenne mindestens 5)
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
  - Konzeptuelles Schema ist die Aufgabe in Text, Logisches Schema ist die Auflistung in Tabellen
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
  - Sekundärschlüssel: Dient auch zu identifizierung eines Tupel, ist aber von einem anderen Schlüssel abhängig
  ## Aufgabe 8
  Welche Arten von Beziehungen gibt es? Zeichne für jede ein Beispiel auf
  - 1:1 - Ein Haus hat nur ein Fundament und auf einem Fundament steht nur ein Haus
  - 1:n - Ein Haus hat mehrere Räume aber ein Raum kann nur in einem Haus sein
  - n:n - Eine Firma kann mehrere Mitarbeiter beschäftigen und eine Person kann mehrere Jobs haben
## Aufgabe 9
Was bedeutet der Begriff Kardinalität und welche Kardinalitäten gibt es?
Eine majestätische Anrede eines religiösen Oberhauptes (Kardinalität = Kardinal + Majestät). Da ich aus der Kirche ausgetreten bin weiß ich leider die Namen der Kardinalitäten nicht auswendig. (Was das mit Datenbanken zu tun hat ist mir allerdings schleierhaft...)
  ## Aufgabe 10
  Was bedeutet der Begriff Datenintegrität und worin unterscheidet sich Integrität und referentielle Integrität?
  - Integrität beschreibt die Korrektheit des Datenbestandes. 
  ## Aufgabe 11
  Erkläre die 3 Normalformen
   - 1. Normalform: Atomare Datenauffassung: Es werden alle Atribute in eine eigene Zelle geschrieben. z.B.: Für Vor- und Nachnamen 
   nicht ein gemeinsames Feld benutzen, sondern eine weitere Spalte einfügen, damit Vor- und Nachnamen eine Spale für sich haben; + 
   Kommen in einem Feld mehrere Aufzählungen vor (wie z.B.: ein Mitarbeiter arbeitet an mehreren Projekten) so wird für jedes eine 
   eigene Zeile verwendet. Der Name des Mitarbeiteres kommt dadurch in mehreren Zeilen untereinander vor.
   - 2. Normalform: Es wird überprüft, ob alle Atribute von ALLEN Primärschlüsseln abhängig sind. Ist das nicht der Fall, wird die 
   Tabelle geteilt und über Kardinalitäten miteinander Verbunden.
    - 3. Normalform: Es wird überprüft ob ein Atribut dierekt von einem anderen Atribut abhänig ist. Ist das der Fall, wird eine neue 
    Tabelle erstellt, die die Beziehung der beiden darstellt und nur die eindeutige Beschreibung (meist eine Seriennummer) bleibt in der 
    ursprünglichen Tabelle erhalten 

  ## Aufgabe 12
  Erkläre den Unterschied zwischen starken und Schwachen Entitäten und erstelle ein Beispiel.
  - Eine starke Entität ist durch einen Primärschlüsse eindeutig beschreibbar (z.B.: ein Haus durch eine Adresse),
  - Eine schwache Entität ist nur mit hilfe der ihr zugewiesenen starken Entität eindeutig beschreibbar (z.B.: Der Raum 204 in dem Haus 
    an der Adresse: .......)
## Aufgabe 13
Welche Grundregeln gibt es im Relationenmodell? (Nenne mindestens 4)
  ## Aufgabe 14
  Wie löst man eine M:N Beziehung auf? Erstelle ein Beispiel
  - Man fügt eine Tabelle ein (die dann als eigene Entität zählt). 
  Beispiel: |Mitarbeiternummer|Vorname|Nachname| -n----------------m- |ProjektID|Projektname|Abteilung|    wir zu:
  |Mitarbeiternummer|Vorname|Nachname| -1------n- |Mitarbeiternummer|ProjektID| -m--------1- |ProjektID|Projektname|Abteilung|
  ## Aufgabe 15
  Ein Handelsbetrieb verkauft ein Sortiment von Artikeln, die er von verschiedenen Herstellern bezieht. Der Handelsbetrieb hat einen 
  bestimmten Kundenkreis, der regelmäßig Bestellungen aufgibt. Eine Bestellung kann mehrere Artikel umfassen. Ein Artikel kann von 
  mehreren Lieferanten bezogen werden und ein Lieferant liefert natürlich meist mehr als einen Artikel. Erstelle ein ERD und ein 
  Relationenmodell, welches der 3. Normalform entspricht.
  "Primärschlüssel" 'Fremdschlüssel'
  - Article ("Articlenr.:int", Article_description:varchar(32))
  - Maker ("Maker_ID:int", Maker_name:varchar(32))
  - Order ("ID:int")
  - Customer ("Customer_ID:int")
  - Customer_info ('Customer_ID:int', Beforename:varchar(32), Aftername:varchar(32), Area_code:int, Tel.:int, e-mail:varchar(32))
  - City ('Area_code:int', City_name:varchar(32))

## Aufgabe 16
Welche Anomalien kennst du und was beschreiben sie?
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

"Primärschlüssel" 'Fremdschlüssel'
- Flight harbor ("Flight_harbor_ID:varchar(32)", City_ID:varchar(32))
- Flight ("Flight_number:varchar(32)", Departure_time:time, Departure_date:date, Departure_flight_harbor:varchar(32), Arrival_time:time, Arrival_date:date, Arrival_flight_harbor:varchar(32), 'Pilot_ID:int', Plane_name:varchar(32))
- Plane ("Plane_name:varchar(32)", 'Planetype_ID:varchar(32))
- Planetype ("Planetype:ID:varchar(32)", Seatcount:int)
- Pilot ("Pilot_ID:int", Beforename:varchar(32), Aftername:varchar(32), Birthdate:date)
