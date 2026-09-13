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


## Block 3

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
## Block 5

#### Kosten- und Leistungsrechnung

##### 1. Betriebliches Rechnungswesen

Das **betriebliche Rechnungswesen** erfasst sämtliche wirtschaftlichen Geschäftsfälle, die in einem Unternehmen Wertbewegungen auslösen.

Es dient unter anderem zur:

- Erfassung von Veränderungen der Vermögens- und Kapitalstruktur
- Berechnung von Gewinn oder Verlust
- Information, Kontrolle und Steuerung des Unternehmens

Grundsätzlich wird zwischen **internem** und **externem Rechnungswesen** unterschieden.

| Internes Rechnungswesen | Externes Rechnungswesen |
|---|---|
| Kosten- und Leistungsrechnung | Finanzbuchhaltung |
| individuell gestaltbar | gesetzlich geregelt |
| dient internen Entscheidungen | richtet sich u. a. an Eigentümer, Gläubiger und Staat |
| Kostenrechnung und Leistungsrechnung | GuV und Bilanz |

---

## 2. Aufbau der Kosten- und Leistungsrechnung

Die **KLR** besteht aus:

- **Kostenrechnung**
- **Leistungsrechnung**

Die Kostenrechnung gliedert sich in drei Stufen:

1. **Kostenartenrechnung** → Welche Kosten sind angefallen?
2. **Kostenstellenrechnung** → Wo sind die Kosten angefallen?
3. **Kostenträgerrechnung** → Wofür sind die Kosten angefallen?

##### Ablauf der Kostenrechnung

![[Pasted image 20260913143517.png]]

> [!important]
> **Kostenarten → Kostenstellen → Kostenträger**
>
> **Welche Kosten? → Wo? → Wofür?**

**Einzelkosten** können direkt einem Kostenträger zugerechnet werden.

**Gemeinkosten** müssen zunächst über die Kostenstellenrechnung verteilt und anschließend über Gemeinkostenzuschläge den Kostenträgern zugerechnet werden.

---

## 3. Leistungsrechnung

In der Leistungsrechnung werden die betrieblichen Leistungen möglichst detailliert erfasst.

> [!definition]
> **Leistungen** sind in Geldeinheiten bewertete, erfolgswirksame Wertzuflüsse, die aus der betrieblichen Leistungserstellung resultieren.

##### Absatzleistungen

Umsatzerlöse aus dem Verkauf von Waren.

##### Lagerleistungen

Mehrbestände an unfertigen und fertigen Erzeugnissen.

##### Aktivierte Eigenleistungen

Selbst erstellte Anlagen, die im eigenen Betrieb verwendet werden.

##### Gesamtleistungen

$$
\text{Gesamtleistung}
=
\text{Absatzleistung}
+
\text{Lagerleistung}
+
\text{aktivierte Eigenleistung}
$$

---

## 4. Kostenrechnung

Die Kostenrechnung erfasst alle im Unternehmen anfallenden **Kosten**.

> [!definition]
> **Kosten** sind der in Geldeinheiten bewertete mengenmäßige Verbrauch an Gütern und Leistungen, der zur betrieblichen Leistungserstellung erforderlich ist.

Die Kosten werden:

1. nach **Kostenarten** erfasst,
2. nach **Kostenstellen** aufgeteilt,
3. den **Kostenträgern** zugerechnet.

---

## 5. Kostenartenrechnung

Die **Kostenartenrechnung** ist die **1. Stufe der Kostenrechnung**.

Sie dient der Erfassung und Systematisierung aller Kostenarten einer Abrechnungsperiode.

Die Daten stammen hauptsächlich aus:

- Finanzbuchhaltung
- Lohn- und Gehaltsbuchhaltung
- weiteren Hilfsrechnungen

> [!question]
> **Welche Kosten sind in welcher Höhe angefallen?**

##### Beispiele für Kostenarten

- Materialkosten
- Personalkosten
- Mietkosten
- Energiekosten
- Abschreibungen
- Zinsen

---

## 6. Aufgaben der KLR

##### Ermittlung der Selbstkosten einer Abrechnungsperiode

Alle Kosten und Leistungen einer Periode werden erfasst, um das **Betriebsergebnis** zu ermitteln.

##### Ermittlung der Selbstkosten eines Erzeugnisses

Die Selbstkosten einzelner Produkte werden ermittelt.

Sie bilden eine wichtige Grundlage für die **Verkaufspreiskalkulation**.

##### Kontrolle der Wirtschaftlichkeit

Die Entwicklung von Kosten und Leistungen wird überwacht.

Ziel ist es, die Wirtschaftlichkeit der Leistungserstellung und -verwertung zu verbessern.

##### Bewertung von Beständen

Die KLR liefert die Herstellungskosten zur Bewertung von:

- unfertigen Erzeugnissen
- fertigen Erzeugnissen

##### Ermittlung von Deckungsbeiträgen

Mit der Teilkostenrechnung kann festgestellt werden, welchen Beitrag ein Produkt zur:

- Deckung der Fixkosten
- Erzielung eines Gewinns

leistet.

##### Planung und Entscheidungen

Die Informationen der KLR bilden eine wichtige Grundlage für betriebliche Planungen und Entscheidungen.

---

## 7. Aufwand und Kosten

Ausgangspunkt der KLR ist die **GuV** mit ihren Aufwendungen und Erträgen.

Allerdings gilt:

> [!important]
> **Nicht jeder Aufwand ist gleichzeitig eine Kostenposition der KLR.**

Aufwendungen werden zunächst unterschieden in:

- **neutralen Aufwand**
- **Zweckaufwand**

---

## 8. Neutraler Aufwand

> [!definition]
> **Neutraler Aufwand** hat nichts mit der regelmäßigen betrieblichen Leistungserstellung innerhalb der betrachteten Abrechnungsperiode zu tun.

Ein Aufwand ist neutral, wenn mindestens eines der folgenden Merkmale zutrifft:

##### Betriebsfremd

Hat nichts mit dem eigentlichen Betriebszweck zu tun.

Beispiele:

- Spenden
- Spekulationsverluste bei Wertpapieren

##### Periodenfremd

Gehört nicht zur betrachteten Abrechnungsperiode.

Beispiele:

- Steuernachzahlung
- Gehaltsnachzahlung

##### Außerordentlich

Tritt unregelmäßig auf oder ist ungewöhnlich hoch.

Beispiele:

- Verkauf einer Maschine weit unter Buchwert
- Verluste aus Schadenfällen
- Verluste durch Insolvenz eines Geschäftspartners

> [!warning]
> Neutrale Aufwendungen werden **nicht als Kosten in die KLR übernommen**, da sie das Bild des normalen Betriebsgeschehens verfälschen würden.

---

## 9. Zweckaufwand und Grundkosten

Aufwendungen, die durch den eigentlichen Betriebszweck verursacht werden, bezeichnet man als **Zweckaufwendungen**.

Werden diese **unverändert** in die KLR übernommen, handelt es sich um **Grundkosten**.

> [!definition]
> **Grundkosten = Aufwendungen der Finanzbuchhaltung, die in gleicher Höhe in die KLR übernommen werden.**

Beispiele:

- Personalkosten
- Materialkosten
- Mietkosten

---

## 10. Kalkulatorische Kosten

Die KLR wird zusätzlich um **kalkulatorische Kosten** korrigiert.

Dabei wird unterschieden zwischen:

| Kostenart | Bedeutung |
|---|---|
| **Anderskosten** | Aufwand existiert in der GuV, wird in der KLR aber in anderer Höhe angesetzt |
| **Zusatzkosten** | Kosten in der KLR, denen kein Aufwand in der GuV gegenübersteht |

##### Anderskosten

Beispiele:

- kalkulatorische Abschreibungen
- kalkulatorische Wagnisse
- kalkulatorische Zinsen

##### Zusatzkosten

Beispiele:

- kalkulatorischer Unternehmerlohn
- kalkulatorische Miete
- kalkulatorische Zinsen für das Eigenkapital

##### Zusammenhang

```text
Finanzbuchhaltung                         KLR

Aufwand                                  Kosten
│                                         │
├── Neutraler Aufwand                     │
│   → keine Kosten                        │
│                                         │
└── Zweckaufwand ──── Grundkosten ────────┤
                                          │
                       Anderskosten ───────┤
                                          │
                       Zusatzkosten ───────┘
```

---

## 11. Kalkulatorische Abschreibungen

In der Finanzbuchhaltung werden Anlagegüter anhand ihrer **Anschaffungs- bzw. Herstellungskosten** abgeschrieben.

In der KLR sollen kalkulatorische Abschreibungen dagegen den **tatsächlichen Werteverzehr** darstellen.

Dabei gilt:

- nur **betriebsnotwendige Anlagegüter**
- Abschreibung vom **Wiederbeschaffungswert**
- tatsächliche Nutzungsdauer
- lineare Abschreibung

##### Prinzip der Substanzerhaltung

Die KLR geht davon aus, dass ein Anlagegut nach Ablauf seiner Nutzungsdauer durch ein gleichwertiges Anlagegut ersetzt werden muss.

Die zukünftigen Wiederbeschaffungskosten sollen daher über die verkauften Produkte erwirtschaftet werden.

---

## 12. Kalkulatorischer Unternehmerlohn

Bei Einzelunternehmen und Personengesellschaften erhält der Unternehmer normalerweise kein reguläres Gehalt, sondern einen Anteil am Gewinn.

Ohne Berücksichtigung seiner Arbeitsleistung wären die Selbstkosten zu niedrig.

Deshalb wird ein **kalkulatorischer Unternehmerlohn** angesetzt.

Als Orientierung dient das Gehalt eines vergleichbaren leitenden Angestellten.

> **Kalkulatorischer Unternehmerlohn = Zusatzkosten**

---

## 13. Kalkulatorische Miete

Werden eigene private Räume betrieblich genutzt oder besitzt das Unternehmen seine Betriebsräume selbst, entstehen keine tatsächlichen Mietzahlungen.

Damit die Kosten trotzdem realistisch dargestellt werden, wird eine **kalkulatorische Miete** angesetzt.

Als Grundlage dient die **ortsübliche Miete vergleichbarer Räume**.

> **Kalkulatorische Miete = Zusatzkosten**

---

## 14. Kalkulatorische Wagnisse

Für bestimmte betriebliche Einzelrisiken können **kalkulatorische Wagniskosten** berücksichtigt werden.

Beispiele:

- Unfälle
- Brand
- Explosion
- Diebstahl
- Schwund
- Preisverfall
- Verderb
- Materialfehler
- Arbeitsfehler
- Forderungsausfälle

Sie werden nur berücksichtigt, wenn das Risiko **nicht durch eine Versicherung abgedeckt** ist und mit entsprechender Wahrscheinlichkeit eintreten kann.

Das allgemeine Unternehmerrisiko zählt **nicht** dazu.

---

## 15. Einzelkosten und Gemeinkosten

##### Einzelkosten

> [!definition]
> Kosten, die einem Kostenträger **direkt** zugerechnet werden können.

Beispiele:

- Fertigungsmaterial
- Bauteile
- Fertigungslöhne
- Verpackung
- Werbung für ein konkretes Projekt
- Vertreterprovision

##### Gemeinkosten

> [!definition]
> Kosten, die einem Kostenträger **nicht direkt** zugerechnet werden können.

Beispiele:

- Betriebsstoffe
- Gehälter
- Energiekosten
- Miete
- Büromaterial
- Steuern
- Gebäudeabschreibungen
- Maschinenabschreibungen
- allgemeine Werbung
- kalkulatorische Zinsen

Gemeinkosten müssen über einen **Verteilungsschlüssel** verteilt werden.

---

## 16. Kostenstellenrechnung

Die **Kostenstellenrechnung** ist die **2. Stufe der Kostenrechnung**.

Sie verteilt insbesondere die Gemeinkosten auf die Bereiche, in denen sie entstanden sind.

> [!question]
> **Wo sind welche Kosten in welcher Höhe angefallen?**

Eine **Kostenstelle** ist der Ort, an dem Kosten entstehen.

Eine Kostenstelle kann beispielsweise sein:

- Arbeitsplatz
- Unterabteilung
- Abteilung
- betrieblicher Funktionsbereich

##### Typische Kostenstellen eines Industriebetriebs

1. **Material**
2. **Fertigung**
3. **Verwaltung**
4. **Vertrieb**

Kostenstellen können nach verschiedenen Kriterien gebildet werden:

- räumlich
- funktionell
- organisatorisch

---

## 17. Betriebsabrechnungsbogen (BAB)

Der **Betriebsabrechnungsbogen (BAB)** wird innerhalb der Kostenstellenrechnung verwendet.

Seine Aufgaben sind:

- Verteilung der Gemeinkosten auf die Kostenstellen
- Ermittlung der Gemeinkostensummen

Der BAB ist typischerweise aufgebaut nach:

- **senkrecht:** Gemeinkostenarten
- **waagerecht:** Kostenstellen

Dabei wird unterschieden:

##### Kostenstelleneinzelkosten

Gemeinkosten, die einer Kostenstelle **direkt** zugeordnet werden können.

##### Kostenstellengemeinkosten

Gemeinkosten, die einer Kostenstelle nur **indirekt über Verteilungsschlüssel** zugeordnet werden können.

---

## 18. Kostenträgerrechnung

Die **Kostenträgerrechnung** ist die **3. Stufe der Kostenrechnung**.

Sie baut auf den Ergebnissen der:

- Kostenartenrechnung
- Kostenstellenrechnung

auf.

Einzelkosten und die Kosten der Kostenstellen werden möglichst **verursachungsgerecht auf die Kostenträger verteilt**.

> [!question]
> **Wofür sind welche Kosten in welcher Höhe entstanden?**

##### Kostenträger

Kostenträger können sein:

- einzelne Kundenaufträge
- Produkte
- Dienstleistungen
- innerbetriebliche Leistungen

##### Aufgaben der Kostenträgerrechnung

- Ermittlung der Kosten einzelner Kostenträger
- Daten für die Bestandsbewertung fertiger und unfertiger Erzeugnisse
- Kontrolle der Wirtschaftlichkeit des Herstellungsprozesses
- Informationen für Einkauf, Konstruktion, Fertigung und Vertrieb
- Kalkulation der Verkaufspreise

##### Arten der Kostenträgerrechnung

**Kostenträgerstückrechnung**

→ Kalkulation der Kosten eines einzelnen Produkts bzw. einer einzelnen Leistung.

**Kostenträgerzeitrechnung**

→ Betriebsanalyse und Kontrolle der Wirtschaftlichkeit der einzelnen Kostenträger.

---

## 19. Ablauf der Kostenrechnung am Beispiel

Der gesamte Ablauf lässt sich am einfachsten an einem Beispiel verstehen.

Angenommen, ein Unternehmen stellt **Schreibtische** her.

In einem Monat entstehen folgende Kosten:

- Holz: 20.000 €
- Fertigungslöhne: 15.000 €
- Strom: 5.000 €
- Miete: 8.000 €
- Gehälter Verwaltung: 6.000 €
- Werbung: 2.000 €

##### Schritt 1: Kostenartenrechnung

Zuerst wird gefragt:

> **Welche Kosten sind angefallen?**

```text
Holz                     20.000 €
Fertigungslöhne          15.000 €
Strom                     5.000 €
Miete                     8.000 €
Verwaltungsgehälter       6.000 €
Werbung                    2.000 €
---------------------------------
Gesamtkosten             56.000 €
```

Anschließend wird unterschieden:

```text
Kosten
│
├── Einzelkosten
│   ├── Holz
│   └── Fertigungslöhne
│
└── Gemeinkosten
    ├── Strom
    ├── Miete
    ├── Verwaltungsgehälter
    └── Werbung
```

Die **Einzelkosten** können direkt dem Schreibtisch zugerechnet werden.

Die **Gemeinkosten** müssen zunächst über die Kostenstellenrechnung verteilt werden.

---

##### Schritt 2: Kostenstellenrechnung und BAB

Jetzt lautet die Frage:

> **Wo sind die Gemeinkosten entstanden?**

Dazu werden die Gemeinkosten mithilfe des **BAB** auf die Kostenstellen verteilt.

Vereinfachtes Beispiel:

| Gemeinkostenart | Material | Fertigung | Verwaltung | Vertrieb | Gesamt |
|---|---:|---:|---:|---:|---:|
| Strom | 500 € | 4.000 € | 300 € | 200 € | 5.000 € |
| Miete | 1.500 € | 4.000 € | 1.500 € | 1.000 € | 8.000 € |
| Gehälter | – | – | 6.000 € | – | 6.000 € |
| Werbung | – | – | – | 2.000 € | 2.000 € |
| **Summe** | **2.000 €** | **8.000 €** | **7.800 €** | **3.200 €** | **21.000 €** |

Damit wissen wir beispielsweise:

- Materialstelle verursacht 2.000 € Gemeinkosten
- Fertigungsstelle verursacht 8.000 € Gemeinkosten
- Verwaltung verursacht 7.800 € Gemeinkosten
- Vertrieb verursacht 3.200 € Gemeinkosten

Der BAB beantwortet damit die Frage:

> **Wo sind die Gemeinkosten angefallen?**

---

##### Schritt 3: Kostenträgerrechnung

Jetzt müssen die Kosten auf die Produkte bzw. Aufträge verteilt werden.

Die Frage lautet:

> **Wofür sind die Kosten entstanden?**

Angenommen, das Unternehmen produziert zwei Schreibtischmodelle:

- Modell A
- Modell B

Die **Einzelkosten** können direkt zugeordnet werden:

```text
Holz ──────────────────────────────┐
                                   ├──> Modell A / Modell B
Fertigungslöhne ───────────────────┘
```

Die **Gemeinkosten** nehmen dagegen den Weg über die Kostenstellen:

```text
Strom ────────┐
Miete ────────┤
Gehälter ─────┼──> BAB ──> Kostenstellen ──> Gemeinkostenzuschläge ──> Produkte
Werbung ──────┘
```

Am Ende werden **Einzelkosten und zugerechnete Gemeinkosten** zusammengeführt.

Vereinfachtes Beispiel für einen Schreibtisch:

| Kosten | Betrag |
|---|---:|
| Fertigungsmaterial | 80 € |
| + Materialgemeinkosten | 8 € |
| + Fertigungslöhne | 60 € |
| + Fertigungsgemeinkosten | 32 € |
| + Verwaltungs-/Vertriebsgemeinkosten | 20 € |
| **Selbstkosten** | **200 €** |

Damit beantwortet die Kostenträgerrechnung die Frage:

> **Wie viele Kosten hat dieser konkrete Schreibtisch verursacht?**

---

## 20. Gesamtzusammenhang

```text
                    KOSTENRECHNUNG
                          │
                          ▼
              1. KOSTENARTENRECHNUNG
                          │
                  "Welche Kosten?"
                          │
             ┌────────────┴────────────┐
             │                         │
             ▼                         ▼
        Einzelkosten              Gemeinkosten
             │                         │
             │                         ▼
             │              2. KOSTENSTELLENRECHNUNG
             │                         │
             │                        BAB
             │                         │
             │                  "Wo entstanden?"
             │                         │
             │                         ▼
             │               Gemeinkostenzuschläge
             │                         │
             └────────────┬────────────┘
                          ▼
               2. KOSTENTRÄGERRECHNUNG
                          │
                    "Wofür entstanden?"
                          │
                          ▼
              Produkt / Auftrag / Leistung
                          │
                          ▼
                     Selbstkosten
```

> [!important]
> **Kostenartenrechnung:** Welche Kosten sind entstanden?
>
> **Kostenstellenrechnung / BAB:** Wo sind die Gemeinkosten entstanden?
>
> **Kostenträgerrechnung:** Wofür sind die Kosten entstanden?

##### Kurz gesagt

```text
Kostenart
   ↓
Welche Kosten?
   ↓
Einzelkosten ───────────────────────────┐
                                       │
Gemeinkosten                            │
   ↓                                   │
Kostenstelle                            │
   ↓                                   │
BAB                                     │
   ↓                                   │
Gemeinkostenzuschlag                    │
   ↓                                   │
   └───────────────────────────────────┤
                                       ↓
                                Kostenträger
                                       ↓
                                  Selbstkosten
```
