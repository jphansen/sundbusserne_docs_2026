
---
## Executive Overview: Infrastruktur på M/S Pernille

### Netværks- & connectivitylag

*Pernille* anvender samme **MiWire-antenneopsætning** som *Jeppe*: to uafhængige antenner, der fødes ind i en **MiWire BDU (Below Deck Unit)** med load balancing mellem Telia og TDC 4G.  

**Dog** er BDU’ens Ethernet-udgang ikke tilsluttet en moderne Ubiquity Border Gateway, men derimod en **ældre, Asvig-udviklet load-balancer**. Denne enhed har i praksis **begrænset effekt**, fordi MiWire-setuppet allerede håndterer operator-failover. Den Asvig-udviklede enhed tilfører ingen yderligere redundans eller optimering.

### 1. Nuværende netværksarkitektur – Pernille (mangelfuld)

```mermaid
graph TD
    A1["MiWire Antenne 1"]
    A2["MiWire Antenne 2"]
    BDU["MiWire BDU<br/>(load balancer + failover)"]
    TELIA["4G: Telia"]
    TDC["4G: TDC"]
    ASVIG["Asvig load-balancer (ældre, begrænset effekt)"]
    ETH["Ethernet netværk (ingen central overvågning)"]
    WIFI["WiFi (ingen management)"]

    A1 --> BDU
    A2 --> BDU
    BDU -->|Load balancer| TELIA
    BDU -->|Load balancer| TDC
    BDU -->|Ethernet| ASVIG
    ASVIG -->|"Ingen ekstra værdi"| ETH
    ETH --> WIFI
```



**Konsekvenser:**
- **Ingen central netværksovervågning** – hverken over WiFi-adgangspunkter, kablede porte eller enhedsstatus.
- **Ingen mulighed for moderne netværksmanagement** (f.eks. UniFi-controller eller tilsvarende).
- Ældre komponenter giver generelt lavere stabilitet og sværere fejlsøgning.

### POS- & betalingsinfrastruktur

Kassestationerne (cellerne) er **identiske** med *Jeppe*: hver celle består af en iPad (Shopbox), en bonprinter (Star/Epson) og en betalingsautomat, der kommunikerer via kendte IP-adresser inden for cellen.

### 2. POS-celle

```mermaid
graph LR
    IPAD["iPad (Shopbox POS)"]
    BON["Bonprinter (Star/Epson)"]
    BET["Betalingsautomat (kortterminal)"]

    IPAD -->|"Kender IP på"| BON
    IPAD -->|"Kender IP på"| BET
    BON -->|"Udskrift"| IPAD
    BET -->|"Betalingsrespons"| IPAD
```


### Videoovervågning

**Ingen videoserver om bord.** *Pernille* har i dag **ingen ISPS-videoovervågning** – hvilket er et bemærket sikkerhedsmæssigt gab.

### Øvrige enheder

- En laserprinter til kontorfunktioner (antages at være tilsluttet det eksisterende netværk).

### Samlet vurdering & anbefaling

Infrastrukturen på *Pernille* er **betydeligt ældre** end på *Jeppe* og lider under:
- Forældet og ineffektiv load-balancer
- Ingen central netværksovervågning
- Ingen videoovervågning

**Anbefaling:** Et **fuldt overhaul** af netværksinfrastrukturen anbefales. Dette bør inkludere:
1. Udskiftning af den Asvig-udviklede load-balancer med en moderne **Ubiquity Border Gateway** (eller tilsvarende).
2. Implementering af **central netværksovervågning** (f.eks. UniFi-controller).
3. Etablering af **videoovervågning (videoserver + kameraer)** i overensstemmelse med ISPS-krav.
4. Eventuel opgradering af kabling og WiFi-access points.

---

### 3. Mangler og flaskehalse – visuel oversigt

```mermaid
graph TD
    subgraph "Eksisterende (utilstrækkeligt)"
        M1["MiWire BDU (ok)"]
        M2["Asvig load-balancer"]
        M3["Ingen netværksovervågning"]
        M4["Ingen videoserver"]
    end

    subgraph "Anbefalet fremtidig tilstand"
        F1["Ubiquity Border Gateway"]
        F2["Central UniFi-controller"]
        F3["Videoserver + kameraer"]
    end

    M1 --> M2 --> M3
    M3 --> M4
    M4 -.->|"Opgrader til"| F1
    F1 --> F2
    F2 --> F3
```

### 4. Samlet enhedsoversigt på Pernille (nuværende)

```mermaid
graph TD
    subgraph "Netværk (Asvig load-balancer, ingen overvågning)"
        ETH["Kablet Ethernet"]
        WIFI["WiFi (uovervåget)"]
    end

    subgraph "POS-celler (flere)"
        C1["iPad + bonprinter + betalingsterminal"]
        C2["iPad + bonprinter + betalingsterminal"]
        C3["..."]
    end

    subgraph "Øvrige enheder"
        PRN["Laserprinter"]
        NOTE["Ingen videoserver"]
    end

    ETH --- C1
    ETH --- C2
    ETH --- C3
    ETH --- PRN
    WIFI --- C1
    WIFI --- C2
    WIFI --- C3
    NOTE -.->|Manglende| ETH
```

