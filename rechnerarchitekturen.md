### !Von-Neumann-Architektur

- **Komponenten**:
    - Control Unit (Steuerwerk)
    - ALU (arithmetisch-logische Einheit)
    - Memory (gemeinsamer Speicher für Daten und Programme)
    - Gemeinsames BUS-System für Daten und Instruktionen
    - I/O Unit (Ein-/Ausgabeeinheit)

- **Vorteile**:
    - Einfacher Aufbau, kostengünstig
    - Flexibilität: Daten und Programme im gleichen Speicher

- **Nachteile**:
    - Von-Neumann-Flaschenhals: gemeinsamer BUS führt zu Engpässen
    - Geschwindigkeitsbegrenzungen durch gemeinsamen BUS

### !Harvard-Architektur

- **Komponenten**:
    - Separate Speicher und BUS-Systeme für Daten und Programme

- **Vorteile**:
    - Schnellere Datenverarbeitung, da Daten und Instruktionen parallel verarbeitet werden können

- **Nachteile**:
    - Komplexer und teurer als Von-Neumann-Architektur

### ROM-Arten

- **Masken-ROM**: Programmiert während der Herstellung, unveränderbar, früher als BIOS-Chip verwendet.
- **PROM (Programmable ROM)**: Nach Herstellung programmierbar, kann nur einmalig beschrieben werden.
- **EPROM (Erasable Programmable ROM)**: Mit UV-Licht löschbar, wieder programmierbar, aber umständlich in der
  Handhabung.
- **EEPROM (Electrically Erasable Programmable ROM)**: Elektrisch lösch- und beschreibbar, häufig in modernen
  Anwendungen wie BIOS und Mikrocontrollern.
- **Flash-Speicher**: Schneller, in Blöcken lösch- und beschreibbar, häufig in SSDs und USB-Sticks, unterscheidet sich
  in NAND (nicht linear adressierbar) und NOR (linear adressierbar).

### PLDs (Programmable Logic Devices)

- **PLA (Programmable Logic Array)**: Beide Ebenen (AND und OR) programmierbar, flexibel zur Implementierung von
  logischen Funktionen.
- **PAL (Programmable Array Logic)**: Nur die AND-Ebene programmierbar, die OR-Ebene ist fest, einfacher und schneller
  als PLA.
- **GAL (Generic Array Logic)**: Wiederbeschreibbare Version von PAL, ermöglicht flexiblere Anwendungen durch erneutes
  Programmieren.
- **CPLD (Complex Programmable Logic Device)**: Enthält mehrere Logikelemente, Flip-Flops und Routing-Ressourcen,
  ermöglicht komplexere logische Schaltungen und Funktionalitäten.
- **FPGA (Field Programmable Gate Array)**: Hochkomplexe Logikelemente und umfangreiche Routing-Optionen, geeignet für
  die Entwicklung und Prototyping von komplexen Systemen wie CPUs und SoCs.

### RAM (Random Access Memory)

- **Definition**: Flüchtiger Speicher, der Daten bei Stromverlust verliert.
- **Typen**:
    - **DRAM (Dynamic RAM)**: Nutzt Kondensatoren zur Speicherung, muss regelmäßig aufgefrischt werden.
        - **SDRAM (Synchronous DRAM)**: Synchronisiert mit dem Systemtakt der CPU.
        - **DDR (Double Data Rate)**: Überträgt Daten auf beiden Taktflanken, mehrere Generationen (DDR1, DDR2, DDR3,
          DDR4, DDR5).
    - **SRAM (Static RAM)**: Verwendet Flip-Flops zur Speicherung, benötigt kein regelmäßiges Auffrischen, schneller
      aber teurer als DRAM.
        - **Verwendung**: Cache-Speicher, Register, BIOS.

- **Speicher-Controller**:
    - Verwalten den Speicherzugriff und verhindern Kollisionen.
    - Enthalten oft Funktionen wie Error Correction Code (ECC) für Datensicherheit.
    - In modernen Systemen meist in der CPU integriert für bessere Performance.

- **Cache**:
    - **L1, L2, L3 Caches**: Verschiedene Ebenen, die unterschiedliche Geschwindigkeiten und Größen haben.
    - **Verdrängungsstrategien**:
        - FIFO (First In First Out)
        - LRU (Least Recently Used)
        - LFU (Least Frequently Used)
        - Random, CLOCK, und statistische Verfahren

- **Speicher Hierarchie**:
    - **Register**: Schnellster, kleinster Speicher, direkt in der CPU.
    - **L1 Cache**: Sehr schnell, nahe der CPU, klein.
    - **L2 Cache**: Größer als L1, etwas langsamer.
    - **L3 Cache**: Noch größer, geteilt zwischen CPU-Kernen.
    - **Hauptspeicher (RAM)**: Größer als Caches, langsamer, flüchtig.
    - **Festplatte/SSD**: Größter, langsamster Speicher, nicht-flüchtig.

- **SDRAM/DDR-RAM**:
    - **Technologien**: Von PC66 SDR (66 MHz) bis DDR5 (bis zu 25,6 GByte/s).
    - **Synchronisation**: DDR überträgt mehrere Datenbits pro Taktzyklus.

### !IOPS (Input/Output Operations Per Second)

- **Definition**: Maß für die Anzahl der Ein- und Ausgabeoperationen, die ein Speichersystem pro Sekunde durchführen
  kann.

- **Wichtige Faktoren**:
    - **Latenz**: Zeit, die benötigt wird, um auf eine Datenanforderung zu reagieren.
    - **Suchzeit**: Zeit, die benötigt wird, um die genaue Position der Daten zu finden.
    - **IOPS-Formel**:
      IOPS = [1/(Latenz + Suchzeit)] * 1000
      Beispiel: Eine Festplatte mit einer Suchzeit von 3,5 ms und einer Latenz von 3,2 ms hat etwa 155 IOPS.

- **Unterschiede bei Zugriffsarten**:
    - **Sequenzieller Zugriff**: Daten werden in einer kontinuierlichen Reihenfolge gelesen oder geschrieben, was höhere
      IOPS ermöglicht.
    - **Zufälliger Zugriff (Random Access)**: Daten werden in zufälligen Bereichen gelesen oder geschrieben, was
      tendenziell niedrigere IOPS zur Folge hat.

- **Einfluss auf die Performance**:
    - **Kleine Dateien**: Können schnell eine hohe Anzahl an IOPS verbrauchen, was zu Performance-Einbußen führt, wenn
      die IOPS-Kapazität des Systems überschritten wird.
    - **Große Dateien**: Weniger IOPS-anfordernd, profitieren jedoch von hoher Bandbreite.

- **Bedeutung in der Praxis**:
    - **SSDs**: Hohe IOPS-Werte, besonders bei zufälligen Zugriffen, wodurch sie herkömmliche HDDs in vielen Anwendungen
      überlegen sind.
    - **HDDs**: Niedrigere IOPS-Werte, geeignet für sequenzielle Zugriffe, langsamer bei zufälligen Zugriffen.

### SATA (Serial ATA)

- **Definition**: Ein serielles Protokoll für den Datentransfer zwischen Computern und Speichermedien, entwickelt zur
  Überwindung der Limitierungen der parallelen ATA-Schnittstellen.

- **Funktionalität**:
    - **SMART (Self-Monitoring, Analysis, and Reporting Technology)**: Zur Überwachung und Analyse von
      Festplattenzuständen und Vorhersage von Fehlern.
    - **Hot-Swap-Fähigkeit**: Ermöglicht das Austauschen von Festplatten im laufenden Betrieb ohne Abschaltung des
      Systems.

- **Kompatibilität**:
    - **Abwärtskompatibilität**: Jüngere SATA-Generationen sind abwärtskompatibel zu älteren Versionen.
    - **Kompatibilität mit SAS (Serial Attached SCSI)**: SAS-Controller können SATA-Festplatten steuern, umgekehrt
      jedoch nicht.

- **Vorteile von SATA**:
    - Höhere Datenraten und Zuverlässigkeit im Vergleich zu parallelen ATA-Schnittstellen.
    - Geringerer Kabelaufwand und besseres Kabelmanagement durch serielle Datenübertragung.

### !RAID Level (Redundant Array of Independent Disks)

- **Definition**: RAID ist eine Technologie zur Kombination mehrerer physischer Festplatten zu einer logischen Einheit,
  um Datenredundanz und/oder Performance zu verbessern.

| RAID Typ | Anzahl Festplatten | Datenredundanz | Lese-Performance | Schreib-Performance   |
|----------|--------------------|----------------|------------------|-----------------------|
| RAID 0   | 2 (+)              | Keine          | Schnell          | Schnell               |
| RAID 1   | 2 (+)              | Hoch           | Schnell          | Etwas langsamer (99%) |
| RAID 5   | 3 (+)              | Mittel         | Schnell          | Etwas langsamer       |
| RAID 6   | 4 (+)              | Hoch           | Schnell          | Etwas langsamer       |

### !SSD RAID

- Hochleistungscontroller nutzen PCI Express, um die Performance auf den Bus zu bringen, da SATA oder SAS an ihre
  Grenzen stoßen.
- Verschiebung von festplattenartigen SSDs hin zu M.2 SSDs, die direkt auf das Mainboard gesteckt werden können.

### !Busstruktur

- **Definition**: Busse sind Kommunikationssysteme, die Daten zwischen verschiedenen Komponenten eines Computers
  übertragen.

- **Typen von Bussen**:
    - **Steuerbus (Control Bus)**: Überträgt Steuerinformationen und Signale zur Koordination der Aktivitäten innerhalb
      des Computers.
    - **Adressbus**: Unidirektionaler Bus, der die Speicheradressen übermittelt, um festzulegen, wohin Daten gesendet
      oder von wo Daten abgerufen werden sollen.
    - **Datenbus**: Bidirektionaler Bus, der die eigentlichen Daten zwischen den Komponenten überträgt.

- **Speichercontroller**:
    - **Funktion**: Managt den Zugriff auf den Speicher, überwacht die Datenintegrität und stellt sicher, dass nur eine
      Komponente zur gleichen Zeit auf den Speicher zugreift.
    - **Arbitersteuerung**: Verhindert Kollisionen durch Koordination der Speicherzugriffe.
    - **Waitstate**: Zustand, in dem die CPU wartet, bis die Datenübertragung abgeschlossen ist. Caches können dieses
      Problem reduzieren.

### DMA (Direct Memory Access)

- **Definition**: Eine Technik, die es Peripheriegeräten ermöglicht, direkt auf den Speicher zuzugreifen, ohne die CPU
  zu belasten.

- **Vorteile**:
    - Reduziert die CPU-Last, indem es direkte Datenübertragungen zwischen Speicher und Peripheriegeräten ermöglicht.
    - Erhöht die Datenübertragungsgeschwindigkeit und die Gesamtleistung des Systems.

- **Funktionsweise**:
    - **DMA-Controller** übernimmt die Datenübertragung und signalisiert dem Speichercontroller, wenn er Zugriff auf den
      Speicher benötigt.
    - **Arbiter-Mechanismus**: Stellt sicher, dass keine Konflikte auftreten, indem er den Speicherzugriff zwischen CPU
      und DMA-Controller koordiniert.
    - Nach Abschluss der Übertragung gibt der DMA-Controller die Kontrolle zurück an die CPU.

### !PCI-Express (PCIe)

- **Definition**: Ein Hochgeschwindigkeits-Serienbus-Standard, der dedizierte Punkt-zu-Punkt-Verbindungen zwischen
  verschiedenen Computerkomponenten bietet.

- **Vorteile**:
    - **Hohe Datenraten**: Unterstützt durch serielle Punkt-zu-Punkt-Verbindungen, die höhere Geschwindigkeiten und
      Effizienz im Vergleich zu parallelen Bus-Systemen bieten.
    - **Flexibilität**: Ermöglicht die Nutzung von verschiedenen Steckplatzgrößen (x1, x4, x8, x16), je nach Anforderung
      der angeschlossenen Geräte.

- **Architektur**:
    - **Lane-Paare**: Verwendet zwei Leitungspaare, eines für den Datenempfang und eines für den Datenversand. Ein
      Steckplatz kann maximal 16 Lanes bündeln.
    - **Switches**: Verbindungen zwischen PCIe-Geräten können direkt oder über Switches erfolgen, die eine effiziente
      Kommunikation ermöglichen und Störungen vermeiden.

### CISC (Complex Instruction Set Computing)

- **Definition**: Eine Prozessorarchitektur, die darauf abzielt, den Computer mit einem komplexen Satz von Befehlen
  auszustatten, um Aufgaben effizienter zu erledigen.

- **Merkmale**:
    - **Viele komplexe Befehle**: Reduziert die Anzahl der benötigten Anweisungen pro Programm.
    - **Variable Befehlslängen**: Unterschiedliche Befehle können unterschiedlich lang sein.
    - **Mehrere Takte pro Befehl**: Komplexe Anweisungen können mehrere Taktzyklen zur Ausführung benötigen.
    - **Beispiele**: x86-Architektur, Z80-Prozessor.

- **Vorteile**:
    - **Reduzierte Anzahl von Anweisungen pro Programm**: Durch komplexere Befehle kann ein Programm mit weniger
      Anweisungen auskommen.
    - **Effiziente Speicherverwaltung**: Durch die variable Länge der Befehle kann der Speicher effizienter genutzt
      werden.

- **Nachteile**:
    - **Komplexere Hardware**: Die Implementierung eines CISC-Prozessors ist hardwareseitig aufwändiger.
    - **Langsamere Befehlsausführung**: Einige komplexe Befehle können viele Taktzyklen zur Ausführung benötigen.

### RISC (Reduced Instruction Set Computing)

- **Definition**: Eine Prozessorarchitektur, die darauf abzielt, die Anzahl und Komplexität der Befehle zu reduzieren
  und diese möglichst schnell auszuführen.

- **Merkmale**:
    - **Einfachere, einheitliche Befehle**: Alle Befehle haben eine ähnliche Länge und werden in einem Taktzyklus
      ausgeführt.
    - **Feste Befehlslänge**: Alle Befehle haben die gleiche Länge, was die Dekodierung vereinfacht.
    - **Load/Store-Architektur**: Datenoperationen sind auf Register beschränkt; der Speicherzugriff erfolgt nur über
      spezielle Lade- und Speicherbefehle.
    - **Beispiele**: ARM-Architektur, MIPS-Architektur.

- **Vorteile**:
    - **Schnellere Befehlsausführung**: Da alle Befehle in der Regel in einem Taktzyklus ausgeführt werden.
    - **Einfachere Hardware**: Die Hardware-Implementierung ist einfacher und kostengünstiger.
    - **Effiziente Nutzung der Pipeline**: Durch die Einfachheit und Einheitlichkeit der Befehle kann die Pipeline
      effizienter genutzt werden.

- **Nachteile**:
    - **Größere Anzahl von Anweisungen pro Programm**: Da jeder Befehl nur eine einfache Operation ausführt, benötigt
      ein Programm möglicherweise mehr Anweisungen.

### Grundstruktur der Assembler Abarbeitung in einer CPU

- **Ablauf der Abarbeitung**:
    1. **Fetch**: Holen der Anweisung aus dem Speicher.
    2. **Decode**: Dekodieren der Anweisung und Bestimmen der notwendigen Operationen.
    3. **Execute**: Ausführen der Operationen durch die ALU oder andere Funktionseinheiten.
    4. **Write**: Zurückschreiben der Ergebnisse in das Register oder den Speicher.

- Die Control Unit überwacht die Ausführung der Befehle und stellt sicher, dass alle Schritte in der richtigen
  Reihenfolge und ohne Konflikte ablaufen.

### CPU Register

- **Data Register**: Halten die Daten, die von der CPU verarbeitet werden.

- **Flag Register**:
    - Speichert Zustandsinformationen und Flags wie Zero Flag, Carry Flag usw.
    - Beispiel: Zeigt an, ob das Ergebnis einer Operation Null ist.

- **Pointer/Adress Register**:
    - **Program/Instruction Pointer**: Enthält die Adresse der nächsten auszuführenden Anweisung. Kann für Sprünge (
      branches) verändert werden.
    - **Stack Pointer**: Hält die Adresse des Stack-Anfangs, wo Daten nach dem FIFO-Prinzip abgelegt werden.
    - **Index Register**: Wird als Index bei Speicherzugriffen verwendet, CPU-abhängig.

### Grundlegende Adressierungsarten

#### Immediate Addressing

- **Beschreibung**: Wert als Teil des Befehls.
- **Beispiel**: `MOV R0, #22` (ARM).

#### Direct/Absolute Addressing

- **Beschreibung**: Absolute Speicheradresse im Befehl.
- **Beispiel**: `LDA $25` (6502).

#### Extended Addressing

- **Beschreibung**: Direkter Zugriff auf größere Adressen.
- **Beispiel**: `LDAA 1000h`.

#### Index Addressing

- **Beschreibung**: Basiswert plus Indexregister.
- **Beispiel**: `LDA ($25,X)` (6502).

#### Register Addressing

- **Beschreibung**: Datenbewegung zwischen Registern.
- **Beispiel**: `MOV R0, R1` (ARM).

#### Register Indirect Addressing

- **Beschreibung**: Adresse der Daten im Register.
- **Beispiel**: `LDR R1, [R0]` (ARM).

#### Register Indirect Addressing with Offset

- **Beschreibung**: Adresse im Register plus Offset.
- **Beispiel**: `LDR R1, [R0, #10]` (ARM).

### Stack

- **Struktur**: LIFO (Last In, First Out)
- **Stack Pointer**: Hält die Adresse des aktuellen Stack-Top.
- **Befehle**:
    - **PUSH**: Speichert einen Wert auf dem Stack.
    - **POP**: Entnimmt einen Wert vom Stack.
    - **PEEK**: Zeigt den obersten Wert des Stacks an, ohne ihn zu entfernen.
- **Verwendung**:
    - Speicherung von Rücksprungadressen bei Funktionsaufrufen.
    - Verwaltung lokaler Variablen und Zwischenwerte.
    - Umgang mit Interrupts und Kontextwechseln.

- **Subroutine Calls**:
    - **CALL**: Sichert die aktuelle Adresse (Program Counter) auf dem Stack und springt zu einer Subroutine.
    - **RET (Return)**: Holt die gesicherte Adresse vom Stack und setzt die Programmausführung dort fort.
- **Software Interrupts**:
    - **INT**: Sichert Register und Flags auf dem Stack und führt eine Interrupt Service Routine (ISR) aus.
    - **IRET (Interrupt Return)**: Stellt die gesicherten Register und Flags wieder her und setzt die Programmausführung
      fort.
- **Vorteile**:
    - Ermöglicht verschachtelte Funktionsaufrufe.
    - Unterstützt die Handhabung von Interrupts und Ausnahmebedingungen.

### Interrupts

- **Definition**: Ein Signal, das die CPU unterbricht und sie dazu veranlasst, eine spezielle Routine auszuführen.
- **Polling vs. Interrupts**:
    - **Polling**: CPU fragt regelmäßig externe Geräte ab, was ineffizient sein kann.
    - **Interrupts**: Geräte signalisieren der CPU direkt, was effizienter und reaktionsschneller ist.
- **Interrupt Controller**: Setzt ein Signal auf den Steuerbus und führt den Aufruf an das externe Gerät durch.
- **Problemhistorie**: In der PC-Welt wurden Interrupt Controller oft klein dimensioniert, was zu Engpässen führte.

- **Ablauf des Interrupt-Handlings**:
    1. **Aufruf eines Interrupts**: Sichern aller Register, Pointer und Flags auf dem Stack.
    2. **Interrupt Vektor**: Springt zur Adresse der Interrupt Service Routine (ISR), die im Interrupt Vektor definiert
       ist.
    3. **ISR ausführen**: Spezifische Routine, die auf den Interrupt reagiert.
    4. **Rückkehr zum normalen Betrieb**: Nach Beendigung der ISR werden die Register, Pointer und Flags vom Stack
       zurückgeschrieben, und die Programmausführung wird fortgesetzt.
- **Software-Interrupts**:
    - **INT xxh**: Aufruf eines Software-Interrupts, der die Register und Flags sichert und eine ISR aufruft.
    - **IRET**: Rückkehr vom Interrupt, stellt die gesicherten Register und Flags wieder her.

### Caches

#### Cache Grundlagen

- Adressen werden in Blöcke aufgeteilt, wobei die letzten Bits die Word IDs bilden.
- Größere Blöcke ermöglichen schnellere Zugriffe, aber weniger unterschiedliche Daten im Cache.

#### Fully Associative Caches

- **Strategie**:
    - Daten werden nach Blöcken assoziiert.
    - Keine Konkurrenzprobleme, aber hohe Kosten.
    - Verwendung im L1-Bereich.

#### Direct Mapped Caches

- **Gruppierung**:
    - Adressen werden in Lines gespeichert.
    - Konkurrenzsituationen können auftreten, wenn mehrere Adressen dieselbe Line haben.

- **Beispiel**:
    - Adressen mit gleicher Line ID teilen sich denselben Platz.
    - Trashing kann auftreten, wenn häufig auf dieselbe Line zugegriffen wird.

#### Set-Associative Caches

- **Kombination**:
    - Mischung aus Fully Associative und Direct Mapped Cache.
    - Mehrere Lines können gespeichert werden.
    - Reduziert Konkurrenzsituationen.

- **Beispiel**:
    - Adressen mit demselben Set ID teilen sich den Platz.
    - 2-way set associative Cache für Tags.

#### Flags eines Caches für die Lines

- **Flags**:
    - **T (Type)**: Datentyp (Daten oder Instruktionen).
    - **V (Valid)**: Gültigkeit der Daten.
    - **L (Lock)**: Sperrung der Daten im Cache.
    - **D (Dirty)**: Daten müssen synchronisiert werden.

#### Data Structure Alignment

- **Alignment**:
    - Daten sollen in sortierter Form vorliegen.
    - N-Byte Werte müssen durch n teilbar sein.
    - Ziel: Performance-Einbußen durch ineffizientes Caching vermeiden.

Hier sind die Zusammenfassungen der Folien 55 bis 63 aus dem hochgeladenen Foliensatz:

### Pipeline

- **Stufen der Pipeline**:
    - Fetch: Holen der Anweisung aus dem Speicher.
    - Decode: Dekodieren der Anweisung.
    - Execute: Ausführen der Anweisung.
    - Fetch (Write): Zurückschreiben des Ergebnisses.

#### Betrachtung der Pipeline

- **Herausforderungen**:
    - **Strukturkonflikte**: Mehrere Anweisungen benötigen gleichzeitig dieselbe Hardware-Ressource.
    - **Datenkonflikte**: Eine Anweisung benötigt Daten, die von einer vorherigen Anweisung noch nicht bereitgestellt
      wurden.
    - **Steuerungskonflikte**: Sprungbefehle und Interrupts führen zu Verzögerungen in der Pipeline.

#### RAR (Read After Read)

- **Definition**: Zwei Anweisungen lesen aus demselben Register.
- **Beispiel**: `ADD .., R5` gefolgt von `ADD .., R5`.

#### RAW (Read After Write)

- **Definition**: Eine Anweisung liest ein Register, das von einer vorherigen Anweisung geschrieben wurde.
- **Beispiel**: `ADD R1, ...` gefolgt von `AND ..., R1`.

#### WAR (Write After Read)

- **Definition**: Eine Anweisung schreibt in ein Register, das von einer vorherigen Anweisung gelesen wird.
- **Beispiel**: `ADD ..., R2` gefolgt von `ADD ..., R2, ...`.

#### WAW (Write After Write)

- **Definition**: Zwei Anweisungen schreiben in dasselbe Register.
- **Beispiel**: `ADD ..., R2` gefolgt von `ADD ..., R2`.

#### Pipeline Stall

- **Definition**: Bearbeitungspause der Pipeline, wenn eine Anweisung auf das Ergebnis einer vorherigen Anweisung warten
  muss.
- **Beispiel**:
    - `ADD R2, ...`
    - `ADD R2, ...` (muss warten)
- **Lösungsstrategie**: Reordering der Befehle, um die Pipeline ohne Wartezeiten arbeiten zu lassen.
- **Beispiel**:
    - `ADD R2, ...`
    - `AND ...`
    - `SUB ...`
    - `ADD ...`
    - `ADD R2, ...`

#### Pipeline Optimierungsstrategien

- **Out-of-Order Execution**: Optimierung der Befehlsreihenfolge, um die Auslastung der Funktionseinheiten zu
  maximieren.
- **Speculative Execution**: Vorhersage von Verzweigungen und Ausführung der vermuteten Pfade, um Leerlaufzeiten zu
  vermeiden.
- **Operand Forwarding**: Vorab Laden von benötigten Daten in die Pipeline.

### SIMD (Single Instruction, Multiple Data)
- **Zweck**: Beschleunigung von Berechnungen durch parallele Verarbeitung mehrerer Datenpunkte.
- **Erweiterungen**:
    - **MMX**: Erste SIMD-Erweiterung für Multimedia-Anwendungen.
    - **SSE, SSE2, SSE3, SSE4**: Erweiterungen zur Unterstützung komplexerer mathematischer Funktionen.
    - **AVX (Advanced Vector Extensions)**: Einführung größerer Register (256 und 512 Bit) für noch schnellere und
      effizientere Berechnungen.
- **Vorteile**: Reduziert die Anzahl der notwendigen Lese- und Schreiboperationen, was zu einer deutlichen
  Geschwindigkeitssteigerung führt.

### AVX (Advanced Vector Extensions)
- **Registergrößen**:
    - **SSE (AVX 128 Bit)**: Ursprüngliche Erweiterung.
    - **AVX 256 Bit**: Vergrößerte Register für mehr Parallelität.
    - **AVX 512 Bit**: Noch größere Register, die verschiedene Datentypen abbilden können.
- **Anwendungen**:
    - **Mathematische Berechnungen**: Schnellere und effizientere Verarbeitung von großen Datenmengen.
    - **Multimedia**: Optimierung von Grafik- und Videoverarbeitung.
- **Besonderheiten**:
    - Nur Vielfache der Registergröße können berechnet werden.
    - Beispiel: Bei 18 `int16` können nur 16 in einem SIMD-Register berechnet werden, die restlichen 2 müssen normal
      berechnet werden.


Big Endian -> 01 02 03 04
Little Endian -> 04 03 02 01