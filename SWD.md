
```table-of-contents
```

### Block 1
#### Datentypen und Typkonvertierung
#### Ein- und Ausgabe
#### Format-Strings
#### Arithmetische Operatoren
#### Funktionen
#### Kontrollstrukturen und Testen
##### Schreibtischtest
### Block 2

#### Generationen von Programmiersprachen
1. Generation: **Maschinensprache**

Auf der untersten Ebene der Programmiersprachen arbeitet man nur mit Zahlen. Dementsprechend sind die Programme völlig unleserlich und schwer zu erstellen. Die Programme sind sehr schnell.

- Beispiel: *Binärcode (01010101 10001100)*.
- Merkmale: Direkter Maschinenanweisungen, schwer lesbar, hardwareabhängig. 

2. Generation: **Assemblersprache**

Die Assembler Sprachen orientieren sich an den Maschinenbefehlen des jeweiligen Prozessors. Diese Befehle kann man sich besser merken als den Zahlencode der Maschinensprache. Komfortable Compiler beherrschen zudem Schleifen, Sprungmarken und Unterprogramme. Damit wurde die Lesbarkeit des Quellcodes erhöht.

- Beispiel: *Mnemonics (wie MOVE, ADD, JMP)*.
- Merkmale: Leichter lesbar, hardwareabhängig, wird von einem Assembler in Maschinencode übersetzt. 

3. Generation: **Höhere Programmiersprachen**

Sprachen wie BASIC, PASCAL, C, C++  oder Python sind schon an die menschlichen Denkweisen angepasst. Sie ermöglichen den Austausch des Quellcodes zwischen verschiedenen Betriebssystemen und Prozessoren, wenn der Programmierer sich an den Standard hält

- Beispiele: *C, C++, Java, Python*.
- Merkmale: Menschlich lesbarer Code, abstrahiert von der Hardware, kompiliert oder interpretiert. 

4. Generation: **Nicht-prozedurale Sprachen**

Mit dieser Technik wird nicht mehr beschrieben, WIE ein Problem gelöst werden soll, sondern nur noch WELCHES zu lösen ist. Diese Programmiersprachen sind natürlich nur für ganz spezielle Probleme konzipiert worden. Hierzu zählt beispielsweise SQL.

- Beispiele: *SQL, XML, 4GL*.
- Merkmale: Erleichtern die Interaktion mit Datenbanken, Fokus auf "was" und nicht auf "wie". 

5. Generation: **KI-Sprachen**

Mit diesen Programmiersprachen werden Lösungen mit Hilfe von bestimmten Regeln erarbeitet. Hierzu sind ausgefeilte Mechanismen zu implementieren, die bei Problemen selbstständig aus diesen herausfinden. Leider sind diese Sprachen noch etwas langsam. Hierzu zählen LISP (EMACS), PROLOG und SMALLTALK.

- Beispiele: *LISP, PROLOG, Smalltalk.*
- Merkmale: Konzipiert für KI-Aufgaben, basieren auf Logik und Regeln.
#### Compiler vs. Interpreter Sprachen
Compiler- und Interpretersprachen

In der Informatik werden Programmiersprachen traditionell in die Klassen Compiler- und Interpretersprache eingeordnet. Schauen wir uns zunächst anhand eines Schemas an, was der Unterschied zwischen Compiler- und Interpretersprachen ist und besprechen die beiden Typen anschließend:

![[Pasted image 20250626114257.png]]
**Compilersprachen**

Compilersprachen wie c, c++ oder Fortran übersetzen den Quellcode an einem bestimmten Zeitpunkt der Programmentwicklung in Maschinencode. Dieser liegt anschließend als Datei (bspw. exe) bereit und kann zu beliebiger Zeit ausgeführt werden.

Da die Übersetzung von Quell- zu Maschinencode bereits geschehen ist (und Maschinencode naturgemäß sehr schnell auszuführen ist) haben Compilersprachen den Vorteil schneller Ausführungsgeschwindigkeiten von Programmen. Der Nachteil liegt in ihrer Plattformabhängigkeit der ausführbaren Dateien.

**Interpretersprachen**

Interpretersprachen führen Quellcode instantan zur Laufzeit des Programms aus. Der Interpreter selbst ist ein vorkompiliertes Programm, welches die Quellcodeanweisungen versteht (sie interpretieren kann) und entsprechenden Maschinencode ausführt. Inzwischen existieren unterschiedliche Technologien von Interpretern. Der klassische Interpreter übersetzt Quellcode sequenziell in Maschinencode und führt diesen auf der entsprechenden Plattform aus. Daneben existieren Bytecodeinterpreter, welche aus dem Quellcode Binärcode generieren und diesen in einer virtuellen Maschine ausführen. In einem Bytecodeinterpreter wird aus dem Quellcode kein direkter Maschinencode erzeugt – auch wenn das oftmals missverstanden wird! Der Zwischenschritt – das erzeugen von Binärcode – sorgt für Plattformunabhängigkeit der zu interpretierenden Sprache. Eine Alternative zum Interpreter ist der sog. JIT (Just-In-Time-Compiler). Auch dieser erzeugt in einem Zwischenschritt Binärcode, optimiert diesen jedoch und erzeugt daraus wiederum Maschinencode – alles zur Laufzeit. Der wesentliche Unterschied eines JIT-Compilers zu einem Interpreter liegt darin, bereits kompilierten Code mit Caching-Mechanismen wiederverwendbar zu machen. Während ein klassischer Interpreter die Kompilierung bei jeder Ausführung von Code erneut vornimmt, kann der JIT-Compiler bestimmten (vorkompilerten) Bytecode aus dem Cache abrufen.

Ein zentraler Vorteil von interpretierten Sprachen ist ihre Plattformunabhängigkeit. Außerdem ermöglichen interpretierte Sprachen User-Daten-Interaktionen und sind daher im Bereich der Datenanalyse sehr beliebt (siehe R und Python). Der Nachteil von Interpretersprachen liegt in der langsamen Ausführungsgeschwindigkeit der Programme.

**Python**

Python kombiniert die Eigenschaften von Compiler- und Interpretersprachen. Im Sinne einer Compilersprache agiert Python, indem es Quellcode zunächst in Bytecode übersetzt, bevor der Code prozessiert wird. Externe Python-Module liegen in der Regel sogar als kompilierter Code (pyc-Dateien) vor. Quellcode, welcher durch Prompt-Anweisung oder in Form von Quellcodedateien (py-Dateien) ausgeführt werden soll, muss dagegen noch (zur Laufzeit) kompiliert werden. Der entstandene Bytecode ist kompakter, schneller ausführbar und macht Python (ebenso wie andere interpretierte Sprachen) plattformunabhängig. Nach dem Kompilieren wird der Bytecode in einem zweiten Schritt in eine virtuelle Maschine, die sog. Python-Virtual-Machine, geladen und interpretiert.

![[Pasted image 20250626114456.png]]
**Zusammenfassung**

- Python ist in erster Linie eine interpretierte Sprache. -> Hinweis: Wird in IHK-Musterlösungen auch als Interpreter-Sprache genannt
- Der Python-Interpreter kann aber auch als Compiler betrachtet werden, da er den Quellcode in Bytecode umwandelt, bevor er ihn ausführt.
- Die Bytecode-Übersetzung geschieht virtuell und nicht, wie bei einem Compiler, in Maschinencode, weshalb CPython kein Compiler ist.
#### Kopf- und Fußgesteuerte Schleifen
#### Objektorientierte Programmierung
##### Objektorientierte Programmiersprachen

Der Programmierer beschäftigt sich mit Elementen aus der Problemstellung ( Objekten) und ihrer Darstellung im Lösungsraum. Die Anwendbarkeit ist nicht auf einen bestimmten Typ von Problemen beschränkt.

- Ein Programm ist eine Menge von Objekten, die einander durch Botschaften mitteilen, was zu tun ist.
- Jedes Objekt hat sein eigenes Gedächtnis ( Zustand). Dieses Gedächtnis besteht aus anderen Objekten.
- Jedes Objekt hat einen Typ (,,ist eine Instanz einer Klasse``).
- Alle Objekte eines bestimmten Typs können die gleichen Botschaften empfangen.

**Wiederverwendung und Wiederverwendbarkeit** von Klassen ist eines der Schlüsselkonzepte der objektorientierten Programmierung.

Zwei Formen:

- Komposition durch Elementobjekte
- Vererbung

##### Schnittstelle und Implementierung

Die Schnittstelle (interface) eines Objektes legt fest, welche Botschaften ein Objekt verarbeiten kann.

![[Pasted image 20250626114905.png]]
``` Python
class Server:
    def start(self):
        #Hier der entsprechende Code
        pass

    def stop(self):
        #Hier der entsprechende Code
        pass

    def restart(self):
        #Hier der entsprechende Code
        pass
```
**So erzeugt man einen Server und macht ihn an:**

```Python 
meinServer = Server()
meinServer.start()
```

- ```meinServer``` ist ein Behälter (eine Variable) für einen Server.
- Server() erzeugt ein Objekt vom Typ Server.
- = legt diesen Server in den Behälter meinServer.
- ```meinServer.start()``` schickt die Botschaft ```start()``` an diesen Server.

Die Schnittstelle stellt die Charakterisierung eines Objektes für die Öffentlichkeit dar. Versteckt sind (i.d.R.)

- Der Zustand des Objektes, gespeichert in Attributen.
- Die Implementierung der Botschaften.

Wenn die Schnittstelle sich nicht ändert, kann beides ausgetauscht werden, ohne die Anwendung zu tangieren.
##### Klassen, Attribute, Methoden
**Was ist eine Klasse?**

Eine Klasse in der objektorientierten Programmierung ist ein Bauplan für Objekte. Sie definiert, welche Eigenschaften (Attribute) und welche Fähigkeiten (Methoden) ein Objekt besitzt.

**Attribute**

Attribute speichern den Zustand eines Objekts.

Sie können:
- öffentlich (public) sein – von außen direkt zugreifbar
- privat (private) sein – in Python mit Unterstrich _ oder Doppelunterstrich __ markiert, nicht direkt von außen zugänglich

**Methoden**

Methoden beschreiben das Verhalten eines Objekts.

Auch sie können:
- öffentlich sein – z. B. start()
- privat sein – z. B. __starteService(), nur intern verwendbar

**Der Konstruktor (__init__)**

Der Konstruktor ist eine spezielle Methode in Python mit dem Namen __init__().

Er wird automatisch aufgerufen, wenn ein neues Objekt erstellt wird.

Sein Zweck ist es, das Objekt zu initialisieren, also Startwerte für Attribute zu setzen.

**Beispiel**
```Python
class Server:

    def __init__(self, ip_address):
        self.ip_address = ip_address  # öffentliches Attribut

    def start(self):
        print(f"Server {self.ip_address} wird gestartet...")
        self.__starteService()

    def stop(self):
        print(f"Server {self.ip_address} wird gestoppt...")

    def restart(self):
        self.stop()
        self.start()

    def __starteService(self):
        print("Interner Dienststart läuft...")

s = Server("192.168.1.10")

s.start()
s.restart()

# s.__starteService()  ❌ Fehler: privat!
```
**Was bedeutet *self* in Python?**

In Python ist *self* der Verweis auf das aktuelle Objekt selbst.

Es wird immer als erster Parameter in Methoden einer Klasse übergeben – automatisch beim Aufruf.

**Warum braucht man *self*?**

Mit *self* greift man innerhalb der Klasse auf:

- die Attribute des aktuellen Objekts (self.ip_address)
- andere Methoden desselben Objekts (self.__starteService())

→ Ohne *self* wüsste Python nicht, zu welchem Objekt das Attribut oder die Methode gehört.

**Fazit**

- Klassen = Baupläne
- Attribute = Daten
- Methoden = Aktionen
- Public = von außen nutzbar
- Private = intern geschützt
##### Objekte als Instanzen von Klassen

Wiederverwendung durch Komposition

Einfachste Art der Wiederverwendung. Eine Klasse wird wiederverwendet, indem Objekte dieser Klasse als Elemente in anderen Klassen benutzt werden.

**Komposition – Ein Objekt besteht aus anderen Objekten**

Komposition bedeutet in der objektorientierten Programmierung, dass ein Objekt andere Objekte als Bestandteile enthält.

Beispiel: Ein Rechenzentrum besteht aus mehreren Servern.

→ „Ein Rechenzentrum *hat* Server“ (HAS-A-Beziehung)

Allgemein:

| Die Komposition von Klassen modelliert eine<br><br>**hat ein**<br><br>Beziehung |
| ------------------------------------------------------------------------------- |
```Python
class Server:

    def __init__(self, name, ip_address):
        self.name = name
        self.ip_address = ip_address

    def start(self):
        print(f"{self.name} ({self.ip_address}) wird gestartet.")

class Rechenzentrum:

    def __init__(self):

        self.server_liste = []

    def add_server(self, server):

        self.server_liste.append(server)

    def start_all(self):

        for server in self.server_liste:
            server.start()

#Verwendung:

s1 = Server("Webserver", "192.168.1.10")
s2 = Server("Mailserver", "192.168.1.11")

rz = Rechenzentrum()

rz.add_server(s1)
rz.add_server(s2)
rz.start_all()

# Ausgabe:

Webserver (192.168.1.10) wird gestartet.
Mailserver (192.168.1.11) wird gestartet.
```

**Fazit**

- Komposition: Ein Objekt (Rechenzentrum) enthält andere Objekte (Server)
- Fördert Wiederverwendbarkeit und klare Struktur
- Typisches Prinzip in realitätsnahen Modellierungen


#### Praxis
##### Schleifen
##### Textdateien schreiben und lesen
##### Datenstrukturen
###### Liste
###### Dictionary
##### Klassen
###### Attribute, Methoden
###### Objekte erzeugen

### Block 3

### UML-Diagramme

Wichtige Diagramme sind **Strukturdiagramme** und **Verhaltensdiagramme** - Struktur zeiugt wie ein System aufgebaut ist. Dies ist statisch.

Verhaltensdiagramme sind dynamisch und zeigen Abläufe.

Beispiele sind Klassendiagramme für Struktur- und Aktivitätsdiagramme für Verhaltensdiagramme.

Beispiel Use-Case-Diagramm
![[Pasted image 20260126160711.png]]
#### Use Case Diagramm 

- visuelle Darstellung der Interaktion zwischen Benutzer und System
- besteht aus:
	- System
	- Akteur
	- Anwendungsfall
	- Assoziationen
Vorteile sind die Benutzerzentrierung, Anforderungsanalyse, Kommunikation zwischen Anwendern und Entwicklern, helfen bei Entwicklung von Testfällen.

**Beziehungen**
Assoziationen zwischen Akteuren und Anwendungsfällen
Include-Beziehung
Extend-Beziehung, erweitert einen Basis Use-Case
Generalisierung: Vererbung von Eigenschaften.

![[Pasted image 20260126161034.png]]
Pfeil zeigt immer auf den GENERELLEN Anwendungsfall.


#### Aktivitätendiagramm
Flussdiagramm, welches von einem System ausgeführte Aktivitäten abbildet.

Beispiele:
- Zur Demonstration der Logik eines Algorithmus.
- Zur Beschreibung der Schritte, die in einem UML-Anwendungsfall durchgeführt werden.
- Zur Illustration von Geschäftsprozessen oder Workflows zwischen Benutzern und dem System.
- Zur Vereinfachung und Optimierung von Prozessen durch die verständliche Erläuterung komplizierter Anwendungsfälle.
- Zur Modellierung von Software-Architekturelementen (z. B. Methode, Funktion und Betrieb).

![[Pasted image 20260126161242.png]]
Symbole bei der IHK

![[Pasted image 20260126161310.png]]
Es gibt immer **START und ENDKNOTEN**, es KANN Schwimmbahnen geben wenn Dinge parallel ablaufen.

Beispiel wo Schwimmbahn sinnvoll:
**![[Pasted image 20260126161426.png]]**

---
### Datenbanken

Warum Datenbanken:
Konsistenz - Datenbestand zu jeder Zeit logisch korrekt.
Integrität - Gesamtheit der Regeln die bestimmen welche Daten(typen) erlaubt sind und in welcher Beziehung sie zueinander stehen.
Constraints: technische Zwangsregeln die Integrität gewährleisten sollen.

- **Integrität** beschreibt die Regeln
- **Constraints** setzen diese Regeln technisch um
- **Konsistenz** ist der Zustand, wenn alle *Constraints* eingehalten werden
#### Entity-Relationship-Modell (ER-Modell)

![[Pasted image 20260129180518.png]]
##### Grundkomponenten

- **Entitätstypen** (Rechtecke): Datenobjekte wie `Kunde`, `Bestellung`, `Produkt`.  
- **Attribute** (Ovale): Eigenschaften wie `KundenID`, `Name`, `Preis`.  
- **Beziehungstypen** (Raute): Verknüpfungen zwischen Entitäten.  
- **Kardinalitäten**: Wie viele Entitäten zueinander in Beziehung stehen können (1:1, 1:n, n:m).

---

**Kardinalitäten – Der Trick zum Verstehen**

**Merksatz**: *"Links → rechts, wie viele?"*  
**Leserichtung**: Immer von **links nach rechts** die Kardinalität lesen.

**1:1 (eins zu eins)**

- **Jede** Entität links ist mit **genau einer** rechts verbunden (und umgekehrt).  
- **Beispiele**:  
  - `Person` 1:1 `Personalausweis`  
  - `Auto` 1:1 `Kennzeichen` (vor Wechselkennzeichen)  

**1:n (eins zu n/vielen)**

- **Eine** Entität links ist mit **0, 1 oder vielen** rechts verbunden.  
- **Eine** rechts ist mit **genau einer** links verbunden.  
- **Beispiele**:  
  - `Mutter` 1:n `Kind`  
  - `Abteilung` 1:n `Mitarbeiter`  
  - `Museum` 1:n `Kunstwerk`

**n:m (viele zu vielen)**

- **Viele** links können mit **vielen** rechts verbunden sein.  
- **Beispiele**:  
  - `Student` n:m `Professor`  
  - `Kunde` n:m `Produkt`  
  - `Laden` n:m `Produkt`

---

**Beispiel 1: Online-Shop**

```text
Entitäten:
[Kunde] ---arbeitet--- [Bestellung] ---enthält--- [Produkt]

Kardinalitäten:
Kunde 1:n Bestellung  (ein Kunde kann viele Bestellungen haben)
Bestellung n:m Produkt (eine Bestellung kann viele Produkte enthalten)
```

---

**Zusammenfassungstabelle**

| Kardinalität | Links → rechts | Rechts → links | **Beispiel** |
| :-- | :-- | :-- | :-- |
| **1:1** | genau 1 | genau 1 | Auto ↔ Kennzeichen |
| **1:n** | 0..n | genau 1 | Abteilung ↔ Mitarbeiter |
| **n:m** | 0..n | 0..n | Student ↔ Kurs |

 **Merksätze**

- **$1:n$**: "Eine Firma → viele Mitarbeiter"  
- **$n:m$**: "Viele Kunden kaufen viele Produkte"  
- **Immer**: Von der "**Mutter**-Seite" aus denken!

#### Relation, Tabelle, Datensatz, Feld

- **Relation**  
    Eine mathematische Menge von Tupeln (Datensätzen).  
    In der Praxis: Tabelle

| Einschub: Relationen und Mengenlehre (kartesisches Produkt)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| In der Mengenlehre ist das kartesische Produkt die Kombination aller Elemente zweier Mengen.<br><br>Beispiel:<br><br>- Menge A: Musikstücke<br>- Menge B: Interpreten<br><br>Das kartesische Produkt enthält alle möglichen Kombinationen, auch unsinnige.<br><br>=> Eine Relation ist immer nur eine Teilmenge dieses kartesischen Produkts – nämlich die fachlich sinnvollen Kombinationen.<br><br>Wichtig:<br><br>- Relationen sind Mengen<br>- Mengen enthalten keine Duplikate  <br>    → Daher dürfen Datensätze in einer Tabelle nicht identisch sein |

- **Tabelle**  
    Strukturierte Darstellung einer Relation mit Spalten und Zeilen

- **Datensatz** (Zeile der Tabelle)  
    Eine Zeile in einer Tabelle  
    → beschreibt ein konkretes Objekt (z. B. ein Gerät)

- **Feld**  
    Eine einzelne Zelle bzw. ein Attribut eines Datensatzes

- **Attribute** (Spalte der Tabelle)

Ein Attribut beschreibt eine Eigenschaft eines Objekts, das in der Datenbank gespeichert wird.

In einer relationalen Datenbank entspricht ein Attribut einer Spalte in einer Tabelle.

Jedes Attribut besitzt:

- einen Namen (z. B. seriennummer)
- einen Datentyp (z. B. VARCHAR, INT, DATE)
- optional Constraints (z. B. NOT NULL, UNIQUE)

Eine Spalte ist die technische Darstellung eines Attributs innerhalb einer Tabelle.

Alle Werte in einer Spalte:

- gehören zum gleichen Attribut
- haben den gleichen Datentyp
- unterliegen den gleichen Regeln (Constraints)

Beispiel: Tabelle geraete

| geraet_id | seriennummer | kaufdatum  | preis |
| --------- | ------------ | ---------- | ----- |
| 1         | SN-001       | 01.03.2023 | 1200  |
| 2         | SN-002       | 15.04.2023 | 980   |

- *seriennummer* → Attribut
- Die gesamte Spalte *seriennummer* → Spalte
- SN-001 → Feldwert

Zusammenhang mit Integrität und Constraints

Da Attribute Eigenschaften beschreiben, müssen sie fachlich korrekt definiert werden.

Beispiele:

- Ein Attribut preis darf nicht negativ sein → CHECK-Constraint
- Ein Attribut seriennummer darf nicht leer oder doppelt sein → NOT NULL + UNIQUE
- Ein Attribut mitarbeiter_id muss auf einen existierenden Mitarbeiter verweisen → FOREIGN KEY

=> Constraints werden immer auf Attributen (Spalten) oder Tabellen definiert.

Abgrenzung der Begriffe

| Begriff   | Bedeutung                             |
| --------- | ------------------------------------- |
| Attribut  | Fachliche Eigenschaft eines Objekts   |
| Spalte    | Technische Umsetzung eines Attributs  |
| Feld      | Einzelner Wert in einer Zeile         |
| Datensatz | Gesamtheit aller Felder einer Zeile   |
| Tabelle   | Menge aller Datensätze einer Relation |
| Relation  | Mathematische Grundlage der Tabelle   |

**Primärschlüssel**

Ein Primärschlüssel (Primary Key, PK) ist ein Attribut oder eine Kombination von Attributen, mit dem jeder Datensatz einer Tabelle eindeutig identifiziert werden kann.

Ein Primärschlüssel:

- identifiziert einen Datensatz eindeutig
- darf nicht leer (NULL) sein
- darf nicht doppelt vorkommen

Beispiel:

- Geraete_ID
- Inventarnummer

**Fremdschlüssel**

Ein Fremdschlüssel (Foreign Key, FK) ist ein Attribut (oder Attributkombination), das auf den Primärschlüssel einer anderen Tabelle verweist.

Ein Fremdschlüssel:

- verweist auf den Primärschlüssel einer anderen Tabelle
- stellt eine Relation (Beziehung) zwischen Tabellen her

Beispiel:

- Ein Gerät verweist über mitarbeiter_id auf einen Mitarbeiter
#### Normalformen
####  1. Normalform (1NF)

- Alle Attribute sind **atomar** (unteilbar, keine Listen/Wiederholungsgruppen in einem Feld).
- In jedem Feld steht genau ein Wert.
- Jede Zeile ist eindeutig identifizierbar (Primärschlüssel).

**Beispiel (Verletzung der 1NF)**

```text
Kunde(KundenID, Name, Telefonnummern)

1 | Alice | 01234-1, 05678-9
```

- Problem: `Telefonnummern` enthält mehrere Werte in einem Feld.


**Korrektur (1NF-konform)**

```text
Kunde(KundenID, Name)
Telefon(KundenID, Telefonnummer)

1 | Alice | 01234-1
1 | Alice | 05678-9
```

- Jetzt ist jeder Attributwert atomar, Telefonnummern stehen in separaten Zeilen.

---

#### 2. Normalform (2NF)

- Voraussetzung: Tabelle ist in 1NF.
- Alle Nichtschlüsselattribute hängen voll funktional vom **gesamten** (ggf. zusammengesetzten) Primärschlüssel ab.
- Keine partiellen Abhängigkeiten von nur einem Teil eines zusammengesetzten Schlüssels.


** Beispiel (Verletzung der 2NF)**

```text
Bestellposition(BestellNr, Artikelnr, ArtikelName, Menge)

Primärschlüssel: (BestellNr, Artikelnr)

1001 | A1 | Tastatur | 2
1001 | A2 | Maus     | 1
```

- Problem: `ArtikelName` hängt nur von `Artikelnr` ab, nicht von der ganzen Kombination `(BestellNr, Artikelnr)`.


**Korrektur (2NF-konform)**

```text
Bestellposition(BestellNr, Artikelnr, Menge)
Artikel(Artikelnr, ArtikelName)
```

- `ArtikelName` ist in einer eigenen Tabelle und hängt nur von `Artikelnr` ab.

---

#### 3. Normalform (3NF)

- Voraussetzung: Tabelle ist in 2NF.
- Keine **transitiven Abhängigkeiten**: Kein Nichtschlüsselattribut hängt über ein anderes Nichtschlüsselattribut vom Schlüssel ab.
- Alle Nichtschlüsselattribute hängen direkt vom Primärschlüssel ab.


** Beispiel (Verletzung der 3NF)**

```text
Mitarbeiter(MitarbeiterID, Name, AbteilungsID, AbteilungsName)

1 | Bob | 10 | Vertrieb
2 | Eve | 10 | Vertrieb
```

- Problem: `AbteilungsName` hängt transitiv von `MitarbeiterID` ab:
    - MitarbeiterID → AbteilungsID → AbteilungsName


**Korrektur (3NF-konform)**

```text
Mitarbeiter(MitarbeiterID, Name, AbteilungsID)
Abteilung(AbteilungsID, AbteilungsName)
```

- In jeder Tabelle hängen alle Nichtschlüsselattribute direkt vom Primärschlüssel ab.

