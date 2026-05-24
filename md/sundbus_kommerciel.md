
---

## Managementrapport – Kommerciel Driftsopfølgning (Helsingør–Helsingborg-ruten)

### Executive Overview

Managementrapporten er rederiets **centrale kommercielle styringsværktøj**. Den samler daglige data fra alle salgssteder (barer, køkken, shop, billetter) og kobler dem med passagertal, budgetter og dækningsbidrag. Rapporten giver ledelsen et **aktuelt, handlingsorienteret overblik** over performance, så afvigelser kan adresseres hurtigt – og beslutninger om priser, sortiment og bemanding træffes datadrevent.

Rapporten er Excel-baseret med en fast struktur pr. måned, genbrugelig skabelon og understøttelse af scenarieplanlægning.

### Hovedfunktioner

| Funktion | Beskrivelse |
|----------|-------------|
| **Daglig salgsregistrering** | Omsætning pr. salgssted (Øvre bar, Forbar, Shop, Nedre bar, Solbar, Extra bar) fordelt på billetter, køkken, bar, tobak, slik, shopvarer, diverse, bingo. Data manuel eller importeret. |
| **Produktspecifik detaljering** | Underliggende faner (”H-ark”) nedbryder kategorier til enkeltprodukter (fadøl, cider, drinks, kaffe, cigaretter, spiritus, vin, slikvarianter) pr. salgssted. Understøtter marginstyring og sortimentsoptimering. |
| **Betalingsafstemning** | Daglige skemaer for kontanter (DKK/SEK), kort, MobilePay, vouchers, fakturaer. Automatisk differanceberegning mod salgstal. Sikrer kontrol, svindminimering og regnskabsdokumentation. |
| **Passagertal & kapacitet** | Registrering af ombordstigende og viderefarende passagerer pr. dag, sammenholdt med budget. Giver indsigt i rutebelastning. |
| **Budgetopfølgning pr. passager (PAX)** | Omsætning omregnes til nøgletal pr. PAX og holdes op mod budget. Afvigelser vises absolut og relativt. |
| **Dækningsbidrag & lønsomhed** | Månedsberegning af bruttodækningsbidrag (DG) pr. salgskonto og produktgruppe. Identificerer rentable indtægtsstrømme. |
| **Forudsætninger & scenarieplanlægning** | Et forudsætningsark fastsætter budgetterede passagertal, valutakurs (SEK/DKK) og omsætningsmål. Skabelonen kopieres til nye måneder; ”hvad nu hvis”-scenarier testes. |
| **Periodesammenligning** | Fast struktur muliggør direkte sammenligning af samme måned på tværs af år samt sæsonudvikling. Understøtter trendanalyse og strategisk planlægning. |
| **Effektiviseringsmodul (”Rest”)** | Tracker igangværende forbedringsinitiativer: automatisering af kontanthåndtering (Sundbus Bank), digitalisering af toldbog, lager-/indkøbssystemer, datavarehusintegration, infrastrukturprojekter. Estimerer tidsbesparelser og omkostningseffekter. |

### Overordnet værdiskabelse

Rapporten fungerer som ét **samlet kommercielt cockpit**. Den sikrer, at ledelsen dagligt kan følge omsætning, passagerflow, bidrag pr. passager, afvigelser og svind – i en struktureret, genbrugelig Excel-ramme med minimal månedlig opsætning.

---

## Mermaid-diagrammer (GitHub-kompatibel)

### 1. Datastrømme i managementrapporten

```mermaid
graph TD
    subgraph "Datakilder"
        POS["Shopbox POS (kassesystem)"]
        BIL["Billetsystem"]
        MAN["Manuel indtastning"]
    end

    subgraph "Managementrapport (Excel)"
        DAG["Daglige ark (salgssteder)"]
        PROD["Produktfaner (H-ark)"]
        AFST["Betalingsafstemning"]
        PAX["Passagertal"]
        BUD["Budget & forudsætninger"]
        DG["Dækningsbidrag"]
    end

    subgraph "Output til ledelse"
        R1["Dagligt overblik over omsætning"]
        R2["Afvigelser pr. PAX"]
        R3["Trends på tværs af perioder"]
        R4["Scenarieanalyser"]
    end

    POS --> DAG
    BIL --> DAG
    MAN --> DAG
    DAG --> PROD
    DAG --> AFST
    DAG --> PAX
    BUD --> PAX
    BUD --> DG
    PROD --> DG
    DAG --> DG
    DG --> R2
    PAX --> R2
    DAG --> R1
    AFST --> R1
    BUD --> R4
    DAG --> R3
```

### 2. Rapports struktur – månedligt workflow

```mermaid
graph LR
    subgraph "Forberedelse"
        F1["Kopier skabelon"]
        F2["Opdater forudsætninger\n(budget, kurs, PAX-mål)"]
    end

    subgraph "Daglig drift"
        D1["Indtast salg pr. sted"]
        D2["Registrer betalinger"]
        D3["Notér passagertal"]
        D4["Beregn afvigelser"]
    end

    subgraph "Månedsafslutning"
        M1["Beregn dækningsbidrag"]
        M2["Sammenlign med budget"]
        M3["Trendanalyse (år/sæson)"]
        M4["Opdater effektiviseringsmodul"]
    end

    F1 --> F2
    F2 --> D1
    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> M1
    M1 --> M2
    M2 --> M3
    M2 --> M4
```

### 3. Nøgletal og afvigelser – fra data til handling

```mermaid
graph TD
    O["Omsætning pr. salgssted"]
    P["Passagertal (ombordstigende)"]
    B["Budget pr. PAX"]

    O --> O1["Omsætning/PAX"]
    P --> O1
    O1 --> A["Afvigelse (absolut/relativ)"]
    B --> A

    A -->|"Underperformance"| H1["Justering af priser/sortiment"]
    A -->|"Overperformance"| H2["Skalering af succes"]
    A -->|"Stor differance"| H3["Kontrol for svind/fejl"]

    H1 --> H4["Handlingsplan"]
    H2 --> H4
    H3 --> H4
```

---

