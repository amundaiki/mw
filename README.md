# SONAT Market Watch 🚀

Et avansert AI-drevet system for markedsovervåking og salgsintelligens som automatisk identifiserer og analyserer forretningsmuligheter for SONAT Consulting.

## 📋 Prosjektbeskrivelse

SONAT Market Watch er et komplett automatiseringssystem som:
- Overvåker norske teknologinyheter og LinkedIn-aktivitet
- Identifiserer potensielle kunder og salgsmuligheter
- Genererer ukentlige PDF-rapporter med prioriterte leads
- Leverer strukturert salgsintelligens for proaktiv kundekontakt

## 🏗️ Systemarkitektur

Systemet består av fire hovedmoduler som arbeider sammen i en prosesseringskjede:

```
Nyhetsdata → News Processor → JSON Merger → HTML Template → PDF Rapport
    ↑              ↓              ↑
LinkedIn → LinkedIn Processor ----┘
```

### Moduler:

1. **News Intelligence Processor** (`prompt_nyheter`)
   - Prosesserer teknologinyheter fra E24, DN, Finansavisen, TU m.fl.
   - Scorer bedrifter basert på SONAT-relevans (1-10 skala)
   - Identifiserer finansieringsrunder, ekspansjon og lederskifte

2. **LinkedIn Intelligence Processor** (`prompt_linkedin-processor`)
   - Analyserer LinkedIn-poster fra målbedrifter
   - Identifiserer ansettelsessignaler og vekstindikatorer
   - Genererer engasjementsscore og salgsmuligheter

3. **LinkedIn Data Enricher** (`prompt_linkedin-merenn6`)
   - Supplerer LinkedIn-data med ytterligere kontekst
   - Validerer og forsterker markedssignaler

4. **JSON Merger** (`prompt_json-merger`)
   - Sammenslår alle datakilder til én strukturert rapport
   - Produserer komplett JSON for PDF-generering
   - Sikrer datakonsistens og kvalitetskontroll

## 🎯 Target Marked

SONAT Market Watch fokuserer på:

**Bedriftsprofil:**
- Norske tech-selskaper ≥15 ansatte
- Årlig omsetning ≥10M NOK
- Sektorer: Bank/Fintech, Maritime, Media, Helse, Telecom, Olje/Gass

**SONAT Tjenester:**
- Digitalisering og teknologirådgivning
- Tjenestedesign og UX
- Maskinlæring og kunstig intelligens  
- VR/AR (virtuell og augmented reality)
- Systemutvikling og arkitektur

## 📊 Relevans-Scoring

**KRITISK (Score 9-10):**
- Kapitalinnhenting ≥50M NOK med tech-fokus
- C-level tech-ansettelser (CTO, CDO)
- AI/ML/Cloud transformasjonsprosjekter
- IPO-forberedelser eller M&A-aktivitet

**HØY (Score 7-8):**
- Betydelig vekst >50% eller store ekspansjonplaner
- Tech-ansettelser (DevOps, Cloud, Data Engineering)
- Strategiske partnerskap med teknologileverandører

**KVALIFISERT (Score 5-6):**
- Generell forretningsvekst i relevante bransjer
- Mindre teknologioppgraderinger
- Bransjepoisjonering som indikerer fremtidige tech-behov

## 🗂️ Filstruktur

```
mw/
├── README.md                           # Denne filen
├── market-watch-template.html          # HTML-template for PDF-generering
├── sonat-styles.css                   # SONAT styling ekstrahert fra nettsiden
├── json mal                           # Komplett JSON-mal med alle variabler
├── pdf_template                       # PDF-template konfigurasjon
├── prompt_nyheter                     # News Intelligence Processor prompt
├── prompt_linkedin-processor          # LinkedIn Intelligence Processor prompt  
├── prompt_linkedin-merenn6            # LinkedIn Data Enricher prompt
├── prompt_json-merger                 # JSON Merger prompt
├── prompt_RSS salgsintelligens-ekspert # RSS/salgsintelligens ekspert prompt
├── market watch 1-2.blueprint (4).json # Blueprint konfigurasjon v1
├── Market watch 2-2.blueprint (3).json # Blueprint konfigurasjon v2
├── json_input/                        # Input data-mappe
├── pdf.co_info                        # PDF.co API-informasjon
└── sonat sin nettside                 # SONAT nettsidedata
```

## 🔧 Teknisk Implementering

### JSON-Struktur
Systemet produserer en standardisert JSON-struktur med:
- `critical_companies`: 4-8 høyprioritet leads
- `qualified_companies`: 8-12 kvalifiserte prospekter  
- `linkedin_posts_pages`: 12 analyserte LinkedIn-poster
- `key_findings`: 2-3 hovedfunn fra markedsanalysen
- `strategic_recommendations`: 3-5 strategiske anbefalinger
- `action_items`: 5-7 konkrete handlingsoppgaver

### Kritiske Tekniske Krav
- **Triple LinkedIn Structure**: `linkedin_pages`, `linkedin_posts_pages` og `linkedin_accounts` må inneholde identiske data
- **Alle felt påkrevd**: Spesielt `critical_companies` må ha alle felt utfylt
- **Make.com kompatibilitet**: JSON må kunne parseres direkte av automatiseringssystem
- **Norsk språk**: All tekst på norsk unntatt tekniske tags

## 📈 Rapportinnhold

Den ukentlige PDF-rapporten inneholder:

1. **Executive Summary**
   - Ukens hovedfunn og kritiske leads
   - Finansieringsaktivitet og markedstrender

2. **Kritiske Bedrifter** 
   - Umiddelbare salgsmuligheter
   - Komplett kontaktinformasjon
   - Tekniske behov kartlagt

3. **LinkedIn-Analyse**
   - 12 høyrelevante poster analysert
   - Engasjementsscore og muligheter
   - Ansettelsessignaler og vekstindikatorer

4. **Strategiske Anbefalinger**
   - Markedsposisjonering
   - Timing for kundekontakt
   - Teknologitrend-analyse

5. **7-Dagers Handlingsplan**
   - Prioriterte oppfølgingsaktiviteter
   - Konkrete kontaktpersoner
   - Timeline for gjennomføring

## 🚀 Bruksområder

**Salgsteam:**
- Prioriterte leads med kontaktinfo
- Tekniske behov og timing kartlagt
- Konkrete samtaleåpnere og verdiprop

**Ledelse:**
- Markedsoversikt og trender
- ROI-beregninger og ressursallokering
- Strategisk posisjonering i markedet

**Teknisk Team:**
- Kunde-tech-stack analyse
- Solutionsarchitecture muligheter
- Kompetansebehov hos prospekter

## 🎯 KPI og Målinger

Systemet sporer og rapporterer:
- Antall kvalifiserte leads identifisert
- Gjennomsnittlig lead-score fordeling
- Konverteringsrate fra rapport til møte
- Sektor-fordeling av muligheter
- LinkedIn engasjement-trender

## 🔐 Sikkerhet og Datahåndtering

- Alle persondata håndteres i henhold til GDPR
- Kun offentlig tilgjengelig bedriftsinformasjon prosesseres
- Strukturert dataminimering og anonymisering
- Sikker API-kommunikasjon med alle datakilder

## 📝 Utviklingsnotater

Prosjektet bruker:
- AI-prompts for intelligent dataprocessering
- JSON-basert dataflyt mellom moduler
- HTML/CSS for PDF-template rendering
- Blueprint-konfigurasjon for automatisering

## 👥 Team

Utviklet for **SONAT Consulting** av AIKI (AI-assistent).

SONAT tilbyr tjenester innen digitalisering, UX-design, maskinlæring, VR/AR, teknologirådgivning og systemutvikling.

---

*Sist oppdatert: [Automatisk generert ved hver push til GitHub]*
