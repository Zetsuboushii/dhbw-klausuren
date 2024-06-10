### Von-Neumann-Architektur

- **Komponenten**: Steuerwerk, ALU, gemeinsamer Speicher, gemeinsames BUS-System, Ein-/Ausgabeeinheit
- **Vorteile**: Einfacher Aufbau, kostengünstig, Flexibilität
- **Nachteile**: Von-Neumann-Flaschenhals, Geschwindigkeitsbegrenzungen

### Harvard-Architektur

- **Komponenten**: Separate Speicher und BUS-Systeme für Daten und Programme
- **Vorteile**: Schnellere Datenverarbeitung
- **Nachteile**: Komplexer und teurer

### ROM-Arten

- **Masken-ROM**: Unveränderbar
- **PROM**: Einmal programmierbar
- **EPROM**: Mit UV-Licht löschbar
- **EEPROM**: Elektrisch lösch- und beschreibbar
- **Flash-Speicher**: Schnell, in Blöcken lösch- und beschreibbar

### PLDs (Programmable Logic Devices)

- **PLA**: Beide Ebenen programmierbar
- **PAL**: Nur AND-Ebene programmierbar
- **GAL**: Wiederbeschreibbare PAL-Version
- **CPLD**: Komplexere logische Schaltungen
- **FPGA**: Hochkomplexe Logikelemente

### RAM (Random Access Memory)

- **Typen**:
    - **DRAM**: Regelmäßiges Auffrischen nötig
    - **SRAM**: Kein regelmäßiges Auffrischen, schneller, aber teurer
- **Cache**: L1, L2, L3

### IOPS (Input/Output Operations Per Second)

- **Definition**: Maß für die Anzahl der Ein- und Ausgabeoperationen pro Sekunde
- **Faktoren**: Latenz, Suchzeit

### SATA (Serial ATA)

- **Funktionalität**: SMART, Hot-Swap-Fähigkeit
- **Vorteile**: Höhere Datenraten, Zuverlässigkeit

### RAID Level (Redundant Array of Independent Disks)

| RAID Typ | Anzahl Festplatten | Datenredundanz | Lese-Performance | Schreib-Performance |
|----------|--------------------|----------------|------------------|---------------------|
| RAID 0   | 2 (+)              | Keine          | Schnell          | Schnell             |
| RAID 1   | 2 (+)              | Hoch           | Schnell          | Etwas langsamer     |
| RAID 5   | 3 (+)              | Mittel         | Schnell          | Etwas langsamer     |
| RAID 6   | 4 (+)              | Hoch           | Schnell          | Etwas langsamer     |

### Busstruktur

- **Typen von Bussen**: Steuerbus, Adressbus, Datenbus

### DMA (Direct Memory Access)

- **Vorteile**: Reduziert CPU-Last, erhöht Datenübertragungsgeschwindigkeit

### PCI-Express (PCIe)

- **Vorteile**: Hohe Datenraten, Flexibilität
- **Architektur**: Lane-Paare, Switches

### CISC (Complex Instruction Set Computing)

- **Merkmale**: Komplexe Befehle, variable Befehlslängen
- **Vorteile**: Weniger Anweisungen pro Programm
- **Nachteile**: Komplexere Hardware, langsamere Befehlsausführung

### RISC (Reduced Instruction Set Computing)

- **Merkmale**: Einfache, einheitliche Befehle, feste Befehlslängen
- **Vorteile**: Schnellere Befehlsausführung, einfachere Hardware
- **Nachteile**: Mehr Anweisungen pro Programm

### CPU Register

- **Data Register**: Halten die Daten
- **Flag Register**: Zustandsinformationen
- **Pointer/Adress Register**: Program/Instruction Pointer, Stack Pointer, Index Register

### Adressierungsarten

- **Immediate Addressing**: Wert als Teil des Befehls
- **Direct/Absolute Addressing**: Absolute Speicheradresse
- **Extended Addressing**: Größere Adressen
- **Index Addressing**: Basiswert plus Indexregister
- **Register Addressing**: Datenbewegung zwischen Registern
- **Register Indirect Addressing**: Adresse der Daten im Register
- **Register Indirect Addressing with Offset**: Adresse im Register plus Offset

### Stack

- **Struktur**: LIFO
- **Verwendung**: Rücksprungadressen, lokale Variablen, Interrupts

### Interrupts

- **Definition**: Signal, das die CPU unterbricht
- **Ablauf**: Sichern der Register, Sprung zur ISR, Rückkehr zum normalen Betrieb

### Caches

- **Fully Associative Caches**: Keine Konkurrenzprobleme, hohe Kosten
- **Direct Mapped Caches**: Konkurrenzsituationen
- **Set-Associative Caches**: Mischung aus Fully Associative und Direct Mapped Cache

### Pipeline

- **Stufen**: Fetch, Decode, Execute, Write
- **Konflikte**: Strukturkonflikte, Datenkonflikte, Steuerungskonflikte

### SIMD (Single Instruction, Multiple Data)

- **Zweck**: Beschleunigung durch parallele Verarbeitung
- **Erweiterungen**: MMX, SSE, AVX

### AVX (Advanced Vector Extensions)

- **Registergrößen**: 128 Bit, 256 Bit, 512 Bit
- **Anwendungen**: Mathematische Berechnungen, Multimedia
