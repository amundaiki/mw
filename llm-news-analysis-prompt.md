# LLM Prompt for Market Watch - De 12 Beste Bedriftene

## Instruksjoner
Du skal analysere nyhetsartikler og LinkedIn-poster for å generere en komplett Market Watch rapport fokusert på de 12 beste og mest relevante bedriftene for Sonat.

## Ny tilnærming:
- Alle 12 bedrifter er pre-kvalifisert som "beste muligheter"
- Ingen tier-system - fokus på prioritering og actionable insights
- Konkrete kontaktstrategier og timing-anbefalinger

## Input du mottar:
- Liste med nyhetsartikler (tittel, innhold, kilde, URL)
- LinkedIn-poster fra overvåkede bedrifter
- Pre-kvalifiserte bedriftsdata (de 12 beste)

## Du skal generere:

### 1. key_findings (2-3 hovedfunn)
```json
"key_findings": [
  {
    "number": 1,
    "priority_class": "critical|high|medium",
    "text": "150-300 tegn analyse av markedstrend med forretningsverdi for SONAT"
  }
]
```

### 2. LinkedIn-analyse (alle 3 strukturer)
```json
"linkedin_posts_pages": [...],
"linkedin_accounts": [...],
"linkedin_pages": [...]
```

### 3. Strategiske anbefalinger
```json
"strategic_recommendations": [
  {
    "title": "30-60 tegn overskrift",
    "content": "150-300 tegn konkret anbefaling"
  }
]
```

### 4. Handlingsoppgaver
```json
"action_items": [
  {
    "number": 1,
    "priority": "critical|high|medium", 
    "timeline": "Denne uken|Neste uke|Denne måneden",
    "action": "100-200 tegn konkret oppgave med kontaktinfo"
  }
]
```

### 5. Topp 3 muligheter
```json
"top_opportunities": [
  {
    "number": 1,
    "company_name": "Fra hardkodet liste",
    "potential_value": "Estimert prosjektverdi og type",
    "recommended_action": "Konkret handlingsanbefaling",
    "priority_level": "critical|high",
    "urgency_indicator": "RING NÅ|48 TIMER|DENNE UKE"
  }
]
```

### 6. Ukesplan
```json
"weekly_actions": [
  {
    "day_number": 1,
    "day_label": "MANDAG",
    "action_description": "Kort beskrivelse",
    "target_companies": "Antall og type bedrifter"
  }
]
```

## Viktige retningslinjer:
- Fokuser på SONATs tjenester: AI/ML, cloud, DevOps, digitalisering
- Bruk norsk språk (unntatt tekniske tags)
- Alle 12 bedrifter er pre-kvalifisert - fokus på prioritering og timing
- Alle anbefalinger må være konkrete og handlingsrettede
- Inkluder kontaktinformasjon og urgency-indikatorer
- Lag konkrete 5-dagers handlingsplaner

## Fokusområder for de 12 beste:
- Rangering etter umiddelbar salgsmulighet
- Konkrete tekniske behov som matcher Sonat
- Timing og kontaktstrategier
- Estimerte prosjektverdier og ROI

## Output format:
Returner kun ren JSON uten forklaringer eller kommentarer.
