# Make.com Workflow-forslag for Hybrid JSON

## Foreslått arkitektur:

### Modul 1: Google Sheets Data Henter
- Henter alle hardkodede verdier fra sheets
- Eksporterer strukturert data til neste modul

### Modul 2: Statisk JSON Builder  
- Bruker `make-com-hardcoded-template.json`
- Populerer alle {{CELL_XX}} referanser med data fra Modul 1
- Lager basis JSON-struktur

### Modul 3: Nyhetsinnsamling
- RSS feeds, LinkedIn API, nyhetskilder
- Samler artikler og poster fra siste uke
- Filtrerer på relevans for SONAT

### Modul 4: LLM Nyhetsanalyse
- Bruker prompt fra `llm-news-analysis-prompt.md`
- Analyserer nyheter og genererer komplekse JSON-deler
- Fokuserer kun på:
  - key_findings
  - linkedin_posts_pages/accounts/pages
  - strategic_recommendations  
  - action_items
  - top_opportunities
  - weekly_actions

### Modul 5: JSON Merger
- Kombinerer statisk JSON fra Modul 2
- Med LLM-generert JSON fra Modul 4
- Validerer final struktur

### Modul 6: PDF.co Generator
- Mottar komplett JSON
- Genererer PDF med HTML-template
- Sender til destinasjon

## Fordeler med denne tilnærmingen:

✅ **Pålitelige data**: Bedriftsinfo og kontaktdetaljer fra sheets
✅ **Fleksible analyser**: LLM håndterer kun komplekse tekstanalyser  
✅ **Feilreduksjon**: Mindre sannsynlighet for hallusinering i faktadata
✅ **Vedlikehold**: Enkelt å oppdatere statiske data vs dynamiske analyser
✅ **Debugging**: Kan teste hver modul separat

## Spesielle hensyn for nyhetsdelen:

- LinkedIn-data krever fortsatt LLM-analyse (for mange poster å hardkode)
- `key_findings` må analysere trender på tvers av kilder
- `strategic_recommendations` baseres på kombinert innsikt
- `action_items` må koble bedriftsdata med markedsinnsikt

Dette gir deg det beste av begge verdener: pålitelig grunndata med intelligent analyse!
