# 1000-Company Scale-Up Proposal

## Question 2: How I would build a list of 1000 ICP-qualified companies in one month

### Core approach
I would run a **funnel, not a list-building exercise**.

**Universe → Score → Verify → Shortlist → Enrich → QA**

**Target yield assumption:**  
- 8,000–12,000 raw company records
- 1,500–2,000 medium-confidence candidates
- 900–1,200 ICP-qualified records after QA
- 1,000 final companies with evidence attached

### Week 1 — Build the universe
**Goal:** collect 8,000–12,000 raw records from high-density sources.

**Sources**
- sector association/member directories
- exhibitor lists
- cluster member pages
- MCA/ROC lookups
- IndiaMART / TradeIndia / Kompass / Justdial discovery
- official company websites from targeted keyword searches
- LinkedIn company pages

**Automation**
- use search scrapers / SERP APIs to build discovery queries by city, product class, and manufacturer terms
- normalize names, addresses, websites, and phone numbers
- de-duplicate with fuzzy matching

**Expected yield**
- 8k–12k raw leads
- 30–40% duplicate / irrelevant cleanup
- 5k–7k usable records

### Week 2 — First-pass qualification
**Goal:** filter to 1,500–2,000 plausible Federer companies.

**Automation**
- LLM-assisted classification on website text and snippets
- rule-based filters for:
  - manufacturer keywords
  - India presence
  - product-led language
  - certification language
  - founder/leadership clues
- exclude:
  - services-only
  - trading/distribution-only
  - subsidiaries of large groups
  - generic pharma / commodity businesses
  - dead sites / stale footprints

**Expected yield**
- 20–30% pass rate from the clean universe
- 1,500–2,000 candidates survive

### Week 3 — Evidence enrichment and scoring
**Goal:** create the actual target list with evidence.

**Automation**
- one agent extracts:
  - products
  - founder/MD name and background
  - certifications
  - facility location
  - hiring / news / expansion
- another agent assigns C1–C6 scores with citations to source snippets
- another agent writes the personalization hook

**Quality control**
- sample audit every 25th record manually
- reject entries with weak or ambiguous evidence
- downgrade anything with service/distributor ambiguity
- flag companies above Rs.500Cr if public data suggests they are too large

**Expected yield**
- 1,500–2,000 enriched
- 1,100–1,300 accepted by the scoring layer

### Week 4 — Final QA and packaging
**Goal:** finalize 1,000 names that a sales team can use immediately.

**Quality control checks**
- no duplicate legal entities
- no missing website if a website exists
- no obviously wrong city mapping
- no large-group / PE-owned misfits
- verify every personalization hook against a source
- ensure every row has at least one explicit manufacturing signal

**Expected final yield**
- 1,000–1,050 publishable companies
- 200–300 reserve names
- a fail list of excluded companies with reason codes

### Tooling stack
- Claude / Gemini / GPT for extraction and scoring
- Python + Playwright + requests/BeautifulSoup for scraping and page capture
- Pandas / Openpyxl for cleaning and export
- Google Sheets / Airtable for review workflow
- LinkedIn / Naukri / company websites / MCA / directories as source layers

### Operating principle
I would optimize for **high-confidence ICP fit, not scale at any cost**.  
A smaller list with clear evidence is more useful than a bloated list with weak screening.
