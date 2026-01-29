**Inhalt**

- [[#Block 1|Block 1]]
		- [[#IP-Adressen|IP-Adressen]]
			- [[#IP-Adressen#IPv4|IPv4]]
			- [[#IP-Adressen#IPv6|IPv6]]
				- [[#IPv6#Formaler Aufbau:|Formaler Aufbau:]]
				- [[#IPv6#IPv6-Unicast|IPv6-Unicast]]
				- [[#IPv6#1. Link-Local (LLA)|1. Link-Local (LLA)]]
				- [[#IPv6#2. Globale Unicast Adresse (GUA)|2. Globale Unicast Adresse (GUA)]]
				- [[#IPv6#IPv6 Multicast|IPv6 Multicast]]
		- [[#MAC-Adressen (Media Access Control)|MAC-Adressen (Media Access Control)]]
		- [[#Schichtenmodelle|Schichtenmodelle]]
			- [[#Schichtenmodelle#OSI 7 Schichten Referenzmodell|OSI 7 Schichten Referenzmodell]]
			- [[#Schichtenmodelle#TCP/IP Referenzmodell|TCP/IP Referenzmodell]]
			- [[#Schichtenmodelle#ARP|ARP]]
		- [[#Ausdehnung von Netzwerken|Ausdehnung von Netzwerken]]
		- [[#Umrechnung Dezimal/Binär/Hexadezimal|Umrechnung Dezimal/Binär/Hexadezimal]]
			- [[#Umrechnung Dezimal/Binär/Hexadezimal#Allgemeine Anforderungen an Netzwerke|Allgemeine Anforderungen an Netzwerke]]
- [[#Block 2|Block 2]]
		- [[#Subnetting|Subnetting]]
			- [[#Subnetting#Subnetting in IPv4|Subnetting in IPv4]]
			- [[#Subnetting#Subnetting in IPv6|Subnetting in IPv6]]
		- [[#IP Protokoll|IP Protokoll]]
			- [[#IP Protokoll#IP Protokoll Header|IP Protokoll Header]]
		- [[#DHCP v4 und v6|DHCP v4 und v6]]
			- [[#DHCP v4 und v6#DHCP v4|DHCP v4]]
			- [[#DHCP v4 und v6#IGMP - Internet Group Management Protocol|IGMP - Internet Group Management Protocol]]
		- [[#ICMP und NDP|ICMP und NDP]]
			- [[#ICMP und NDP#ICMP|ICMP]]
			- [[#ICMP und NDP#NDP - Neighbor Discovery Protocol|NDP - Neighbor Discovery Protocol]]
		- [[#Routing|Routing]]
		- [[#TCP, UDP und Portadressen - Transportschicht|TCP, UDP und Portadressen - Transportschicht]]


## Block 1
#### IP-Adressen
##### IPv4
Eine IPv4 Adresse besteht aus 4 Oktetten, wobei ein Oktett ein Byte ist. Das ergibt eine Größe von **32 Bit**
Jedes Oktett kann den Wertebereich von 0-255 abdecken.
Eine IPv4 Adresse kann nur mithilfe einer **Subnetzmaske** gelesen werden. Diese teilt die IPv4 Adresse in den **Netzanteil** und den **Hostanteil**
```
IP-Adresse: 172.20.8.1
Subnetzmaske: 255.255.0.0
-> Binär verunden
Die ersten beiden Oktette sind Netzanteil, die zweiten Hostanteil
```
![[Pasted image 20250311174338.png]]
Eine andere Notation für IPv4 und Hostanteil ist auch 192.168.4.36 **/16** wobei die 16 die Zahl der auf 1 gesetzten Subnetzbits angibt, hier 16 also 255.255.0.0. Das ergibt einen Hostanteil von 2^16 Bits.

Bei einer **Netzwerkadresse** sind **alle Hostbits binär 0**, diese fast alle Hosts zusammen, also 192.168.4.0 im Beispiel oben.
Eine **Broadcastadresse** setzt **alle Hostbits auf 1**. also 192.168.4.255
Beide Adressen dürfen niemals einem Gerät zugewiesen werden und man muss bei der Berechnung der möglichen Hosts immer 2 abziehen.
Weitere Sonderfälle sind **Unicast**, die eindeutige IP eines Rechners, z.B. eines Webservers, **Multicast** welches alle Hosts adressiert die sich eine Multicastadresse teilen (Class D, 239.1.168.200). **Multicast**adressen haben den IP-Bereich von 224-239 im ersten Oktett.
 
Spezielle IPv4 Adressen:
![[Pasted image 20250310175706.png]]
Weitere private IP-Adressen:
10.0.0.0/8 -> für privaten Gebrauch (Class A)
192.168.0.0/16 -> auch privater Gebraucht (Class D)
224.0.0.0/4 (224-239) -> Multicast Adressen

---
##### IPv6
**Überblick Unterschiede v4 zu v6**
![[Pasted image 20250310180554.png]]
###### Formaler Aufbau:
**Trennzeichen:** ":"
Einheiten sind **Hextette** statt Oktetten
**Zahlensystem: Hexadezimal**
0...9 und A...F
**Zahlenbasis ist die 16**, eine Zahl benötigt 4 Bits. Daher kann man aus einem Byte 2 Hexadezimalzahlen bilden.
**Größe einer IPv6: 128 Bits** = 8 Hextette
**keine Subnetzmaske mehr** nur noch Standard-Präfix /64
 - das Präfix unterteilt in **Netzanteil und Schnittstellen ID**
 IPv6 können **gekürzt** werden
 Regeln für das Kürzen:
	 - Führende Nullen in enem Hextett werden gekürzt
	 - Mehrere Nuller-Hextette werden durch **"::"** gekürzt
###### IPv6-Unicast
Unicast Adresse identifiziert wie bei IPv4 eindeutig ein Gerät, Source-Address eines Pakets muss zwingend eine Unicast Adresse sein. Ziel kann **Multicast** sein, **Broadcast** gibt es in v6 nicht mehr! Dies hat den Vorteil Traffic zu reduzieren und macht NAT unnötig und den Nachteil, dass jeder IPv6 fähige Rechner für das Internet zwingend zwei Adressen benötigt.
###### 1. Link-Local (LLA)
- Sind auf das gleiche Netzwerk beschränkt.
- Kommunizieren dort mit anderen Geräten
- **FE80::/10**
###### 2. Globale Unicast Adresse (GUA)
- vergleichbar zu einer öffentlichen IPv4 Adresse
- können statisch oder dynamisch zugewiesen werden
- GUA besteht aus 3 Teilen
	- 1. Globales Routing Prefix /48 vom Provider
	- 2. Subnetz-ID mit 16 Bit zur Adressierung von Teilnetzen z.B. im Unternehmen
	- 3. Schnittstellen-ID mit 64 Bit
###### IPv6 Multicast
- besonders wichtig, da es keinen Broadcast mehr gibt
- beginnen mit **FF00::/8**
- das Präfix /8 sagt dabei, dass die ersten 8 Bit fest vorgegeben sind
![[Pasted image 20250310181435.png]]
---
#### MAC-Adressen (Media Access Control)
- identifiziert das *physische* Quell- und Zielgerät (**NIC - Network Interface Connector**)
- nur im lokalen Netz gültig
- 12 Hexadezimale Ziffern (z.B.: 90-1B-0E-4B-ED), also 48 Bit oder 6 Byte
- Besteht aus 24 Bit OUI (Organizationally Unique Identifier, von der IEEE) und einer fortlaufenden Nummer von 24 Bit
![[Pasted image 20250311170619.png]]
---
### Schichtenmodelle
#### OSI 7 Schichten Referenzmodell
![[Pasted image 20250311170929.png]]
Besteht aus 7 Schichten, jede Schicht (oder Layer) behandelt eine andere Ebene, mit eigenen Protokollen und Standards.
Merksätze:
Deutsch: **A**lle **S**chüler **t**rinken **v**erschiedene **S**orten **B**ier 7 -> 1
Englisch: **P**lease **D**o **N**ot **T**hrow **S**alami **P**izza **A**way 1 -> 7

---
#### TCP/IP Referenzmodell
- Umsetzung des theoretischen OSI-Modells in Praxis
- Fasst Schichten zusammen
- OSI 1,2 = TCP/IP **Netzzugriff**, OSI 3 = TCP **Internet**, OSI 4 = TCP **Transport**, OSI 5-7 = TCP/IP **Anwendung**
- Transport der Daten passiert im Prozess der Encapsulation
![[Pasted image 20250311171804.png]]![[Pasted image 20250311171853.png]]
- je nach Schicht werden andere Arten der Adressierung verwendet, Schicht 2 (**TCP/IP Schicht Netzzugriff**) verwndet MAC-Adressen und das **Ethernet Protokoll** für den nächsten Hop (Host zu Host), Schicht 3 (**TCP/IP Internet**) verwendet IP-Adressen und das **IP-Protokoll**, Schicht 4 (**TCP/IP Schicht Transport**) verwendet Portnummern zur Adressierung. Schicht 3-4 sind **Ende zu Ende**
---
##### ARP
**Address Resolution Protocol**
- Verfahren zur Zuordnung von MAC-Adressen zu IP-Adressen
- Gerät, dass einen Layer 2 Header bauen will braucht MAC-Adresse
- Sendet also eine ARP Anfrage (*ARP-Request*) zu dieser IP per **Broadcast-MAC FF-FF-FF-FF-FF-FF**
- jedes Gerät im Netz empfängt diesen Broadcast und vergleicht die angefragte IP-Adresse mit der eigenen
- wenn diese übereinstimmen sendet es an die **Source-MAC-Adresse** zurück seine Antwort mit der eigenen MAC-Adresse (*ARP-Reply*)
- der Ziel PC kann diese Antwort im ARP-Cache speichern, dieser lässt sich mit ```arp -a```anzeigen
---
#### Ausdehnung von Netzwerken
![[Pasted image 20250311181240.png]]
**Wichtig sind nur WAN, LAN und MAN** 
#### Umrechnung Dezimal/Binär/Hexadezimal
**Dezimal zu Binär -Divisionsrestverfahren**

Beispiel 229
229 / 2 = 114 Rest 1 **Einerstelle** 
114 / 2 = 57  Rest 0
57 / 2 = 28   Rest 1
28 / 2 = 14   Rest 0
14 / 2 = 7      Rest 0
7 / 2 = 3        Rest 1
3 / 2 = 1        Rest 1
1 / 2 = 0        Rest 1 **128er Stelle** 
Dann von unten nach oben eintragen

| 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1   | 1   | 1   | 0   | 0   | 1   | 0   | 1   |
**Hexadezimal zu Binär**
- 2 Stellige Hexadezimalzahl lässt sich leicht binär umrechnen da diese in 1 Byte passen
- halbiert man dieses Byte kann man durch einsetzen des Werts binär die Hexadezimalzahl umrechnen
Beispiel E9 - E im linken Teil des Bytes, 9 im rechten Teil. E entspricht 14

| 8   | 4   | 2   | 1   | 8   | 4   | 2   | 1   |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1   | 1   | 1   | 0   | 1   | 0   | 0   | 1   |
Das ergibt also binär 11101001 = 233 = E9

##### Allgemeine Anforderungen an Netzwerke
- müssen skalierbar sein
	- **vertikale Skalierbarkeit** also Verbesserung innerhalb eines Systems (mehr RAM für einen Server)
	- **horizontale Skalierbarkeit** also Verbesserung durch Hinzufügen von Ressourcen (z.B.: extra Server bereitstellen)
- **Quality of Service (QoS)** muss geregelt sein, also z.B.: dort Echtzeitanwendungen priorisieren wo diese genutzt werden

## Block 2

#### Subnetting
- Einteilung eines Netzes in kleinere Teilnetze
- z.B. sinnvoll für Provider die ihnen zugewiesene IP Bereiche aufteilen wollen
##### Subnetting in IPv4

Beispiel das Netz 192.168.100.0/24 in zwei **Teilnetze**:
Subnetzmaske 255.255.255.0 benötigt **ein weiteres Bit** im Netzwerkanteil
-> 255.255.255.128 oder 192.168.100.0/25
	Netz 1: 100.0 - 100.127 (0 = Netzadresse, 127 = Broadcastadresse)
	Netz 2: 100.128 - 100.255 (128 = Netzadresse, 255 = Broadcast)
Vorgehen:
1. Wieviele Netze benötige ich? Daraus leite ich meine Anzahl benötigter Bits ab.
2. Neue Subnetzmaske berechnen.
3. Schrittgröße berechnen, 256 - Subnetzmaske
		3a. IP-Adresse letztes Oktett / Schrittgröße, ganzzahligen Anteil \* Schrittgröße = Netzadresse
4. Anzahl Hosts = 2 hoch restliche Bits

| Präfix | Anzahl Netze | Anzahl Hosts  | Schrittgröße |
| ------ | ------------ | ------------- | ------------ |
| /25    | 2^1=**2**    | 2^7-2=**126** | 128          |
| /26    | 2^2=**4**    | 2^6-2=**62**  | 64           |
| /27    | 2^3=**8**    | 2^5-2=**30**  | 32           |
| /28    | 2^4=**16**   | 2^4-2=**14**  | 16           |
| /29    | 2^5=**32**   | 2^3-2=**6**   | 8            |
| /30    | 2^6=**64**   | 2^2-2=**2**   | 4            |

##### Subnetting in IPv6
gleiches Prinzip, Ermittlung der zusätzlich notwendigen Bits. Für IHK landet man meistens bei 4 Teilnetzen (00, 40, 80, C0) - also 2 zusätzliche Bits


Beispiel:
**``` 2025:ACAD:1:ABC0::/58```**  soll in Netze eingeteilt werden - wir benötigen 2 extra Bits, da 2^2 = 4
Bisher feste Bits: 
2025 = 16, ACAD = 32, 0001 = 48, AB = 56 
Beim C sind 2 Bits bereits fest (8, 4):

| 8   | 4   | 2   | 1   |
| --- | --- | --- | --- |
| 1   | 1   | 0   | 0   |
Unsere Subnetze werden also aus den letzten beiden Bits des C gebildet.

| 8   | 4   | 2   | 1   | ergibt   |
| --- | --- | --- | --- | -------- |
| 1   | 1   | 0   | 0   | AB**C**0 |
| 1   | 1   | 0   | 1   | AB**D**0 |
| 1   | 1   | 1   | 0   | AB**E**0 |
| 1   | 1   | 1   | 1   | AB**F**0 |
Und das neue Präfix lautet /60.
Unsere Netze sind also 
``` 
2025:ACAD:1:ABC0:: /60
2025:ACAD:1:ABD0:: /60
2025:ACAD:1:ABE0:: /60
2025:ACAD:1:ABF0:: /60
``` 
***
#### IP Protokoll 
##### IP Protokoll Header
**Eigenschaften des IP-Protokolls**
**Verbindungslos** - keine Überprüfung ob Daten das Ziel erreichen
**Best Effort** - Weg ist immer unterschiedlich
**Medienunabhängig**

![[Pasted image 20250619161215.png]]
**Version** IPv4 oder IPv6
**TTL** Time To Live - gibt an wieviele Hops passiert werden können, jeder Hop (Router) zählt um 1 runter
**Protokoll** zB ICMP
**Header-Prüfsumme** berechnet eine Prüfsumme über alle Header-Bestandteile

**IPv6 Header**: keine TTL - dafür Hop-Limit, keine Prüfsumme, kein Protokoll

Beispiel:
![[Pasted image 20250619161625.png]]
Jede **Zeile** hat 32 Bit, die vier Ziffern am Anfang sind die Zeilennummern und können ignoriert werden. Abzählen von jeweils 32 Bit - also **4 Hexadezimalen Zahlen** für jede Zeile.
So steht die Source-IP in Zeile 4 - daher lautet sie **C0 A8 01 11** oder dezimal **192.168.1.17**
***
#### DHCP v4 und v6

##### DHCP v4
Automatische Vergabe von IP Adressen.
Vorteile:
- Weniger Aufwand
- Weniger Fehler
- Möglichkeiten für Technologien wie PXE Boot
![[Pasted image 20250622164419.png]]
##### IGMP - Internet Group Management Protocol
1. **Was ist das Internet Group Management Protocol (IGMP)?**

Das Internet Group Management Protocol (IGMP) ist ein Protokoll, das es mehreren Geräten ermöglicht, sich eine IP-Adresse zu teilen, sodass sie alle die gleichen Daten empfangen können. IGMP ist ein Protokoll auf Netzwerkebene. Es wird zur Einrichtung von Multicasting in Netzwerken verwendet, die unter IPv4 laufen. IGMP ermöglicht es Geräten, einer Multicasting-Gruppe beizutreten.

2. **Wie funktioniert IGMP?**

Rechner und andere an ein Netzwerk angeschlossene Geräte verwenden IGMP, wenn sie einer Multicast-Gruppe beitreten möchten. Ein Router, der IGMP unterstützt, hört die IGMP-Übertragungen von Geräten ab, um herauszufinden, welche Geräte zu welchen Multicast-Gruppen gehören.

IGMP verwendet IP-Adressen, die für Multicasting reserviert sind. Multicast-IP-Adressen liegen in einem Bereich zwischen 224.0.0.0 und 239.255.255.255. (Im Gegensatz dazu können Anycast-Netzwerke jede normale IP-Adresse verwenden.) Jede Multicast-Gruppe teilt sich eine dieser IP-Adressen. Wenn ein Router eine Reihe von Paketen empfängt, die an die gemeinsame IP-Adresse gerichtet sind, dupliziert er diese Pakete und sendet Kopien an alle Mitglieder der Multicast-Gruppe.

IGMP-Multicast-Gruppen können sich jederzeit ändern. Ein Gerät kann jederzeit eine IGMP-Nachricht „Gruppe beitreten“ oder „Gruppe verlassen“ senden.

IGMP arbeitet direkt auf dem Internet-Protokoll (IP). Jedes IGMP-Paket hat sowohl einen IGMP-Header als auch einen IP-Header.

3. **Welche Arten von IGMP-Nachrichten gibt es?**

Das IGMP-Protokoll lässt mehrere Arten von IGMP-Nachrichten zu:

Mitgliedschaftsberichte: Geräte senden diese an einen Multicast-Router, um Mitglied einer Multicast-Gruppe zu werden.

Nachrichten „Gruppe verlassen“: Diese Nachrichten gehen von einem Gerät an einen Router und erlauben es den Geräten, eine Multicast-Gruppe zu verlassen.

Allgemeine Abfragen zur Mitgliedschaft: Ein multicastfähiger Router sendet diese Nachrichten an das gesamte angeschlossene Netzwerk von Geräten, um die Multicast-Gruppenmitgliedschaft für alle Gruppen im Netzwerk zu aktualisieren.

Gruppenspezifische Abfragen zur Mitgliedschaft: Router senden diese Nachrichten an eine bestimmte Multicast-Gruppe, anstatt an das gesamte Netzwerk.

4.  **Wie unterscheidet sich das Multicasting in IPv4 und IPv6?**

IPv4 und IPv6 sind zwei verschiedene Versionen des Internetprotokolls (IP). IPv6 ist moderner, aber IPv4 ist immer noch weit verbreitet. In IPv6 ist Multicast Listener Discovery (MLD) das Protokoll für Multicasting, nicht IGMP.

5. **Wie unterscheidet sich das Multicasting von Anycast und Unicast?**

[Anycast](https://www.cloudflare.com/learning/cdn/glossary/anycast-network/) ist eine weitere Technologie, die es ermöglicht, die Netzwerkkommunikation an mehrere Orte zu leiten. Ähnlich wie beim Multicast ermöglicht ein Anycast-Netzwerk, dass dieselbe Servergruppe eine oder mehrere IP-Adressen gemeinsam nutzt. Anstatt dass jedoch alle Server den gesamten Traffic zu diesen IP-Adressen erhalten, routet das Netzwerk den Traffic auf der Grundlage einer vorgegebenen Reihe von Kriterien zu einem dieser Server. Anycast-Netzwerke können auch einen größeren Bereich von IP-Adressen unterstützen als Multicast-Gruppen. Das [Cloudflare-Netzwerk](https://www.cloudflare.com/network/) verwendet beispielsweise Anycast, um den gesamten Traffic der Nutzer an das nächstgelegene Rechenzentrum zu routen.

**Multicast vs. Unicast**

„Unicast“ beschreibt, wie der größte Teil des Internets funktioniert. In Unicast-Netzwerken hat jedes angeschlossene Gerät im Netzwerk eine eindeutige Adresse. Nachrichten, die an diese Adresse (im Internet eine IP-Adresse) gerichtet sind, gehen nur an dieses Gerät – und nicht an mehrere Geräte, wie beim Multicasting.

#### ICMP und NDP
##### ICMP 
1. Welche **Aufgabe** hat ICMP?
	Diagnose im Netzwerk
2. Mit welchen **Befehlen** wird ICMP aktiviert?
	Ping-Befehl bzw. tracert
3. Erstellen Sie eine Übersicht über die ICMP-**Nachrichten**!
	ICMP Echo Request mit der IP-Adresse (Typ 8, Code 0) von der Quelle zum Ziel
	ICMP Echo Reply (Typ 0, Code 0)

##### NDP - Neighbor Discovery Protocol
Das Neighbor Discovery Protocol ist ein Protokoll für IPv6. **Es ersetzt z.B. das ARP-Protokoll**, das Broadcast-Prinzip basiert!

| NDP-Nachricht in IPv6       | Aufgabe                                                | ARP-Nachricht in IPv4 | Zieladresse |
| --------------------------- | ------------------------------------------------------ | --------------------- | ----------- |
| Neighbor Solicitation (NS)  | Wie ARP: Fragt nach MAC-Adresse zu einer IPv6-Adresse. | ARP-Request           | FF02::1     |
| Neighbor Advertisement (NA) | Antwort auf NS mit MAC-Adresse                         | ARP-Reply             |             |

Socilicited Node Adress FF02::1:ABCD:DEEF:AFFE:1 – Multicast mit Hostanteil
#### Routing

#### TCP, UDP und Portadressen - Transportschicht
![[Pasted image 20250624150555.png]]
**Aufgaben** 
 
1. Nachverfolgung einzelner Konversationen
2. Segmentierung von Daten und Zusammensetzen von Segmenten
3. Identifizieren der Anwendungen

![[Pasted image 20250624150626.png]]**Portadressen**
- Well-Known Ports (Bekannte Ports) (Nr. 0 bis 1023)
- Registered Ports (1024 bis 49151)
- Dynamic/Private Ports (49151 bis 65535)

**TCP-3-Wege-Handshake**
SYN - SYN, ACK - ACK

**TCP vs. UDP**

| TCP                                                      | UDP                                                        |
| -------------------------------------------------------- | ---------------------------------------------------------- |
| Verbindungsorientiert                                    | Verbindungslos                                             |
| Sendet verlorene Daten erneut                            | sendet nichts noch einmal                                  |
| Gut dort, wo alles komplett ankommen muss (z.B. E-Mails) | Gut dort, wo einzelne Teile folgenlos verlorengehen können |

## Block 3

### Subnetting und VLSM
#### VLSM (Variable Length Subnet Mask)

##### Grundidee
- Mit **VLSM** kannst du innerhalb eines IP-Adressbereichs Subnetze mit unterschiedlich langen Präfixen (z.B. **/24**, **/26**, **/27**) verwenden.
- Ziel ist eine **effiziente** Nutzung des Adressraums, indem jedes Subnetz nur so groß ist, wie es tatsächlich benötigt wird.

##### Grundvorgehen bei VLSM

1. **Gesamten IP-Block** festlegen (z.B. **192.168.1.0/24**).
2. Für jedes Netz den **Hostbedarf** bestimmen (inkl. Reserve).
3. Netze nach **Hostanzahl absteigend** sortieren.
4. Für jedes Netz die **kleinstmögliche passende Maske** wählen.
5. Subnetze nacheinander aus dem Adressraum vergeben (typisch numerisch aufsteigend).

---

**Beispiel 1: 192.168.1.0/24 in unterschiedlich große Netze aufteilen**

Anforderungen (Hosts):

- **Netz A**: ca. **100 Hosts**
- **Netz B**: ca. **50 Hosts**
- **Netz C**: ca. **25 Hosts**
- **Netz D**: ca. **10 Hosts**

**Passende Präfixe**

- Für ~100 Hosts: **/25** → 128 Adressen, 126 nutzbar.
- Für ~50 Hosts: **/26** → 64 Adressen, 62 nutzbar.
- Für ~25 Hosts: **/27** → 32 Adressen, 30 nutzbar.
- Für ~10 Hosts: **/28** → 16 Adressen, 14 nutzbar.

**Adressvergabe (vom größten zum kleinsten Netz)**

Ausgangsnetz: 192.168.1.0/24
**Netz A** (≈100 Hosts) → /25   
Netz:        192.168.1.0/25  
Hostbereich: 192.168.1.1 – 192.168.1.126  
Broadcast:   192.168.1.127 

**Netz B** (≈50 Hosts) → /26   
Netz:        192.168.1.128/26  
Hostbereich: 192.168.1.129 – 192.168.1.190  
Broadcast:   192.168.1.191

**Netz C** (≈25 Hosts) → /27   
Netz:  192.168.1.192/27  
Hostbereich: 192.168.1.193 – 192.168.1.222  
Broadcast:   192.168.1.223 

**Netz D** (≈10 Hosts) → /28   
Netz:        192.168.1.224/28  
Hostbereich: 192.168.1.225 – 192.168.1.238  
Broadcast:   192.168.1.239`

**Hosts pro Netz**: $(2^h - 2)$, mit **h = Anzahl Host-Bits** (z.B. **/26 → 6 Host-Bits → 62 Hosts**).
**Merkregel**: Je **größer** der Präfix (z.B. **/28**, **/29**, …), desto **kleiner** das Subnetz.

### Routing

#### Statisches Routing

#### Dynamisches Routing

##### RIP
##### OSPF
### Firewalls und ACLs

### Kryptographie