**Inhalt**
```table-of-contents
```

## Block 1
#### Rechts- und Geschäftsfähigkeit
#### Businesspläne

#### Stellung des Betriebs

#### Unternehmenskennzahlen

#### Kaufmannseigenschaften

## Block 2

#### Rechtsformen

#### Beschaffung 
##### Grundbegriffe Bedarfsermittlung

**Primärbedarf**

**Sekundärbedarf**

**Tertiärbedarf**


![[Pasted image 20250701080241.png]]
##### Operative und strategische Beschaffungsaufgaben
##### Beschaffungsstrategien
| **Kriterium**              | **Strategie**                                               | **Beschreibung**                                                                                  |
| -------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Anzahl der Lieferanten** | **Single Sourcing **(Einquellenbeschaffung)                 | Ein Lieferant. Ziel: enge Kooperation, z. B. gemeinsame F&E, Kosten-/Qualitätsvorteile.           |
|                            | **Dual Sourcing **(Zweiquellenbeschaffung)                  | Zwei Lieferanten. Zusätzliches Ziel: Absicherung gegen Lieferausfälle.                            |
|                            | **Multiple Sourcing **(Mehrquellenbeschaffung)              | Mehrere Lieferanten. Ziel: Wettbewerbsdruck, Risikostreuung.                                      |
| **Beschaffungsobjekt**     | **Unit Sourcing **(Einzelteilbeschaffung)                   | Rohmaterialien/Einzelteile werden beschafft und intern weiterverarbeitet.                         |
|                            | **Modular** Sourcing (Modulbeschaffung)                     | Fertige Module (Baugruppen/Systeme) werden beschafft; geringe Fertigungstiefe im eigenen Betrieb. |
| **Beschaffungsareal**      | **Local** Sourcing (regionale Beschaffung)                  | Material aus der Region.                                                                          |
|                            | **Domestic** Sourcing (nationale Beschaffung)               | Material aus dem Inland.                                                                          |
|                            | **Global** Sourcing (weltweite Beschaffung)                 | Material aus dem weltweiten Markt.                                                                |
| **Art der Bereitstellung** | **Stock** Sourcing (Vorratsbeschaffung)                     | Lagerhaltung im Betrieb. Üblich in der Industrie.                                                 |
|                            | **Just-in-time** Sourcing (fertigungssynchrone Beschaffung) | Lieferung genau dann, wenn benötigt. Minimale oder keine Lagerhaltung („Lager auf Rädern“).       |
| **Beschaffungssubjekt**    | **Individual** Sourcing (individuelle Beschaffung)          | Unternehmen beschafft allein.                                                                     |
|                            | **Collective** Sourcing (kollektive Beschaffung)            | Einkaufskooperation mehrerer Unternehmen zur Stärkung der Verhandlungsposition.                   |
##### Make or Buy

###### Kosten als Entscheidungskriterium

Ein Industriebetrieb muss grundsätzlich entscheiden, welche Produkte selbst gefertigt und welche eingekauft werden sollen („Make-or-buy-Entscheidung“). Dabei kann es sich um kurzfristige oder auch um langfristige Entscheidungen handeln. Viele Betriebe gehen dazu über, den Anteil der Eigenfertigung zugunsten des Fremdbezugs zu senken. In deutschen Industriebetrieben liegt die durchschnittliche Fertigungstiefe (Eigenanteil an der Wertschöpfung) heute bei nur noch rund 30 %. Neben anderen Kriterien sind die Kosten ein wichtiges Entscheidungskriterium für eine Make-or-buy-Entscheidung. Diese können vielfach durch Fremdbezug („Outsourcing“) gesenkt werden. Dabei sind zwei Arten von Kosten zu unterscheiden:

- **Fixkosten** (feste Kosten) sind Kosten, die unabhängig von der Produktionsmenge anfallen. Typische Fixkosten sind Gehälter, Heizkosten, Miete und Zinsen.
- **Variable Kosten** (veränderliche Kosten) sind Kosten, die abhängig von der Produktionsmenge anfallen. Typische variable Kosten sind Kosten für Werkstoffe, Zulieferteile und Löhne.

---

###### Kurzfristige Make-or-buy-Entscheidungen

Für eine kurzfristige Make-or-buy-Entscheidung werden nur die variablen Stückkosten (`k_v`) der Eigenfertigung dem Bezugspreis gegenübergestellt. Fixe Kosten bleiben hier unberücksichtigt, da sie kurzfristig ohnehin anfallen und damit von der Entscheidung unabhängig sind. Voraussetzung ist, dass das Unternehmen über freie Produktionskapazitäten verfügt. Es gilt:

$$
k_v < Bezugspreis  ⇒  Eigenfertigung 

k_v > Bezugspreis  ⇒  Fremdbezug
$$

---

###### Langfristige Make-or-buy-Entscheidungen

Bei langfristigen Make-or-buy-Entscheidungen müssen die Fixkosten (z. B. Bau einer Produktionshalle) mit einbezogen werden, da sie im Fall des Fremdbezugs vollständig entfallen. Deshalb werden hier die gesamten Stückkosten (fixe und variable Stückkosten) der Eigenfertigung dem Bezugspreis gegenübergestellt:

$$
\begin{aligned}
k_f + k_v &< \text{Bezugspreis} \quad \Rightarrow \quad \text{Eigenfertigung} \\
k_f + k_v &> \text{Bezugspreis} \quad \Rightarrow \quad \text{Fremdbezug}
\end{aligned}
$$


Wegen der Fixkosten übersteigen die Kosten der Eigenfertigung bei geringen Mengen die Kosten des Fremdbezugs. Unter der Bedingung, dass die variablen Stückkosten der Eigenfertigung geringer sind als der Bezugspreis, lohnt sich die Eigenfertigung erst ab einer bestimmten Menge. Die Menge, bei der die Gesamtkosten der Eigenfertigung und des Fremdbezugs gleich hoch sind, wird als **„kritische Menge“** bezeichnet. Sie kann mathematisch und grafisch ermittelt werden:
###### Formel zur Berechnung der kritischen Menge

$$
K_f + k_v * x = P_FB * x
⇒ x = K_f / (P_FB - k_v)
$$

**Legende:**
- $K_f$ = fixe Gesamtkosten  
- $k_v$ = variable Stückkosten  
- $P_FB$ = Einstandspreis bei Fremdbezug

---
#### Optimale Bestellmenge

###### Beispiel (Ausgangsdaten)
Ein Automobilzulieferer hat einen Jahresbedarf an gehärteten Stahlfedern von **3.000 Stück**.  
- **Einstandspreis pro Stück**: 25,00 €  
- **Bestellkosten je Bestellung**: 140,00 €  
- **Lagerhaltungskostensatz**: 24 %

###### Mathematisches Verfahren (Andler-Formel)

Die optimale Bestellmenge lässt sich mit folgender Formel berechnen:

$$
\text{Optimale Bestellmenge} = \sqrt{ \frac{200 \cdot \text{Jahresbedarf} \cdot \text{Bestellkosten je Bestellung}}{\text{Einstandspreis je Stück} \cdot \text{Lagerhaltungskostensatz}} }
$$

###### Beispielrechnung:

$$
\text{Optimale Bestellmenge} = \sqrt{ \frac{200 \cdot 3000 \cdot 140}{25 \cdot 24} } = \sqrt{140000} \approx 374{,}17\ \text{Stück}
$$

Das Ergebnis ist meist ein **gebrochener Wert** und stellt das **theoretische Optimum** dar.

##### Tabellarisches Verfahren

###### Vorteile:
- Es werden **ganzzahlige Bestellmengen** berechnet.
- **Verpackungseinheiten** (z. B. 100er-Packs) können berücksichtigt werden.
- Für jede Bestellmenge sind **Kosten direkt ablesbar**.

###### Formeln:

**Ø Lagerbestand in Stück:**
$$
\text{Ø Lagerbestand} = \frac{\text{Bestellmenge}}{2}
$$

**Lagerhaltungskosten pro Jahr:**
$$
\text{Lagerhaltungskosten} = \text{Ø Lagerbestand in €} \cdot \text{Lagerhaltungskostensatz}
$$

---
##### Lieferanten- und Angebotsvergleich

| **Lieferanten-EK-Preis/Stk. netto** | in €       |
| ----------------------------------- | ---------- |
| **minus Lieferantenrabatt**         | in % und € |
| **=Zieleinkaufspreis**              | €          |
| **minus Lieferantenskonto**         | € und %    |
| **=Bareinkaufspreis**               | €          |
| **Bezugskosten**                    | €          |
| **=Bezugspreis / Einstandspreis**   | €          |

$$
\begin{aligned}
\text{Einkaufspreis (netto)} &- \text{Lieferantenrabatt} = \text{Zieleinkaufspreis} \\
\text{Zieleinkaufspreis} &- \text{Skonto} = \text{Bareinkaufspreis} \\
\text{Bareinkaufspreis} &+ \text{Bezugskosten} = \text{Bezugspreis (Einstandspreis)}
\end{aligned}
$$

--- 


### Block 3

#### Kaufvertragsrecht

##### Kaufvertragsstörungen
**Überblick**![[01_02_Fallstudie 2 Kaufvertragsstörungen.png]]**1. Nicht-rechtzeitige Lieferung**
Voraussetzungen:
- Fälligkeit - der Zeitpunkt ab dem der Käufer die Übergabe vom Verkäufer verlangen kann. Wenn nicht vereinbart, dann kann der Käufer sofortige Rausgabe verlangen.
- Mahnung - es sei denn es gibt einen kalendermäßig bestimmten Zeitpunkt ODER der Verkäufer verweigert ODER Fixkauf / Zweckkauf
- Verschulden - wenn Verkäufer vorsätzlich oder fahrlässig Schuld ist.
Rechte des Käufers ohne Nachfrist:
- Auf Lieferung bestehen
- Schadensersatz wegen Verzögerung
Rechte des Käufer nach Frist:
- Rücktritt
- Schadensersatz statt der Leistung

**2. Schlechtleistung**
Voraussetzungen:
- Vorliegen eines Sachmangels
	- Mangel in der Beschaffenheit, weil die Sache:
		- nicht die Beschaffenheit ausweist wie vereinbart
		- nicht für vorgesehene Verwendung eignet
		- nicht eignet oder allgemeine Beschaffenheit hat, die man erwarten würde
		- nicht zu Werbeaussagen oder Produktbeschreibungen passt
- Mangel in der Montage
- Mangel in der Montageanleitung (Lex Ikea)
- Falsch- oder Minderlieferung
Pflichten des Käufers:
- Prüfungspflicht
- Rügepflicht
	- offene / verdeckte Mängel mit Fristen (offene: sofort, verdeckte 1 Jahr), arglistig verschwiegene: 3 Jahre
- Aufbewahrungspflicht
Rechte des Käufers:
- Nacherfüllung
- Schadensersatz neben der Leistung
- Minderung (nachrangig)
- Rücktritt (nachranggig)
- Schadensersatz STATT der Leistung
**3. Annahmeverzug**
Voraussetzungen:
- Fälligkeit
- Ordnungsgemäßes Angebot
- Verweigerung der Warenannahme
Wirkungen:
- Haftungseinschränkung für Verkäufer
- Gefahrenübergang bei Gattungsware
Rechte des *Verkäufers*
- Hinterlegung der Ware
- Klage auf Abnahme
- Selbsthilfeverkauf
**4. Nicht-rechtzeitige Zahlung**
Voraussetzungen:
- Fälligkeit
- Mahnung
Rechte des Verkäufers:
- Auf Zahlung bestehen
- Schadensersatz wegen Verzögerung (Zinsen)
Nach Nachfrist:
- Rücktritt
- Schadensersatz statt der Leistung
**5. Verjährung**
Frist 3 Jahre (Zahlungen, Forderungen wie Miete oder Gehalt).
Beginnt ENDE des Jahres wo der Anspruch entstanden ist

#### Anfechtung und Nichtigkeit
Nichtig heißt von Anfang an ungültig.
Anfechtung bei vorher gültigen Rechtsgeschäften wegen:
**Irrtums der Erklärung**
Sage X aber meinte Y
**Irrtum über Inhalt**
Weiß nicht was ich da eigentlich meinte (Halve Hahn, Logieren vs. Dinieren)
**Irrtum über verkehrswesentliche Eigenschaft einer Person oder Sache**
Kein Führerschein für Fahrer
**Arglistige Täuschung**
**Widerrechtliche Drohung**
**Irrtum in der Übermittlung**
Tippfehler, falsch verstanden
KEINE Anfechtung be Motivirrtum (kaufe Laufschuhe aber Laufpartner will nicht mehr)

## Block 4

#### Marketing
Anhand **strategischer Analyse** (SWOT, - **S**trenght - **W**eakness - **O**pportunities - **T**hreats.-  Marktgrößenanalyse, Produktlebenszyklusanalyse, Portfolioanalyse) und begleitet durch ständige Marktforschung werden **strategische Ziele** für das Marketing festgelegt und überprüft. **Marketingstrategien** sind dabei Wachstumsstrategien, Segementierungsstrageien oder Positionierungsstrategien.

Darauf aufbauend passiert das operative Marketing.
#### Operatives Marketing
- 4 Ps 
	- Product
	- Price
	- Place
	- Promotion
Marketing also mehr als nur Werbung.
#### Product - Produktpolitik
![[Pasted image 20260622163413.png]]**Produktpolitik** unterscheidet zwischen Produkt**innovation**, Produkt**variation** und Produkt**elimination**
##### Produktinnovation
- Einführung neuer Produkte
Produktdifferenzierung, neues Produkt in gleicher Gruppe (Bsp. Auto - Kleinwagen)
Produktdiversifikation - neue Produktgruppe (Bsp. zusätzlich zu Autos noch Fahrräder)
Produktdiversifikation kann horizontal (gleiche Wirtschaftsstufe), vertikal (andere Wirtschaftsstufe) oder diagonal (andere Wirtschaftsstufe und Produktgruppe, auch lateral genannt) passieren

##### Produktvariation
- Veränderung des Produkts, Produkt verschwindet und nur Variante existiert weiter
- kann physisch-funktionell sein
- ästethisch
- Image
- Namensvariation

##### Produktelimination
- Produkt verschwindet
![[Pasted image 20260622163824.png]]
#### Price - Preispolitik
Der Preis kann **Nachfrageorientiert**, **konkurrenzorientiert** oder per **Kostenkalkulation** gebildet werden.

##### Nachfrageorientierung
- Marktforschung um herauszufinden welchen Preis Kunden bereit wären zu zahlen
- es werden Nachfragekurven (Nachfrage x bei Preis y) gebildet
- gibt Effekte wie Snob-Effekt, Preis interessiert nicht wenn Produkt "exklusiv" genug ist
- Preiselastizität beschreibt den Effekt den eine Preisänderung auf die Nachfrage hat, kann elastisch oder unelastisch sein
$$ e = \frac{\text{prozentuale Mengenänderung}}{\text{prozentuale Preisänderung}} \cdot (-1) $$
#### Konkurrenzorientierung
Es wird ein Vergleich mit Preisen und Angeboten der Konkurrenz angestellt und davon abgeleitet ein Preis gebildet.

##### Industriepreiskalkulation
Der Listenverkaufspreis (LV) wird mit Hilfe der Zuschlagskalkulation gebildet.

| Zuschlagssatz | Position                | EUR   |
| ------------- | ----------------------- | ----- |
|               | Fertigungsmaterial      | 6,70  |
| + 10%         | Materialgemeinkosten    | 0,67  |
| =             | Materialkosten          | 7,37  |
|               | Fertigungslöhne         | 12,50 |
| + 90%         | Fertigungsgemeinkosten  | 11,25 |
| =             | Fertigungskosten        | 23,75 |
| =             | **Herstellkosten**      | 31,12 |
| + 12%         | Verwaltungsgemeinkosten | 3,73  |
| + 5%          | Vertriebsgemeinkosten   | 1,56  |
| =             | **Selbstkosten**        | 36,41 |
| + 15%         | Gewinn                  | 5,46  |
| =             | **Barverkaufspreis**    | 41,87 |
| + 2%          | Kundenskonto            | 0,85  |
| =             | **Zielverkaufspreis**   | 42,72 |
| + 20%         | Kundenrabatt            | 10,68 |
| =             | **Listenverkaufspreis** | 53,40 |
Feste Zuschlagssätze werden zu den Fixkosten addiert um Allgemeinkosten des Betriebs aufzufangen. Skonto und Rabatt werden dabei "von Hundert" gerechnet.

$$
\text{Zielverkaufpreis} = \frac{\text{Barverkaufspreis}}{100 - \text{Skonto}} \cdot \text{Skonto}
$$

$$
\text{Listenverkaufspreis} = \frac{\text{Listenverkaufspreis}}{100 - \text{Rabatt}} \cdot \text{Rabatt}
$$

**Deckungsbeitrag**
![[Pasted image 20260622165439.png]]
##### Place - Vertriebspolitik
Der **Vertrieb** kann über **unternehmenseigene** und **unternehmensfremde Absatzorgane** organisiert sein.
Unternehmensfremd sind dabei rechtlich selbstständige Absatzorgane

| Unternehmenseigen       | Unternehmensfremd |
| ----------------------- | ----------------- |
| (Handlungs-) Reisende   | Handel            |
| Verkaufsniederlassungen | Franchising       |
| Internet                | Handelsvertreter  |
| Telefon                 | Handelsmakler     |
| Mitglieder der GF       | Kommisionär       |
| Factory Outlet Center   |                   |
