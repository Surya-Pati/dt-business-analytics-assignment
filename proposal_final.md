# Sourcing Strategy + 1000-Company Scale-Up Proposal

## Question 1: How else would I find Federer-profile companies across India?

### 1) Industry association and cluster directories
**Examples:** Telangana life-sciences cluster material, CII, FICCI, AIMED, med-tech park member lists, biotech park directories, and state industrial ecosystem pages.

**Why it works:** Federer companies often show up in ecosystems that reward product depth, certifications, and export ambition. Association directories concentrate the exact kind of manufacturer that DeepThought wants.

**Limitations:** Directory data is often stale, and many entries are aspirational rather than validated manufacturers. Every lead still needs website and company-structure verification.

### 2) Government and regulatory signals
**Examples:** ROC/MCA, Udyam / MSME data, patent databases, DSIR-recognized labs, ISO/WHO-GMP/USFDA/EU-GMP mentions, medical device park lists, biotech cluster approvals, pollution-control or factory disclosures where relevant.

**Why it works:** Federer companies usually leave a technical and regulatory footprint. Certifications and registrations are useful proxies for real manufacturing and process discipline.

**Limitations:** Public records can lag reality. A certificate alone does not prove fit, ownership structure, or current growth.

### 3) Trade-show and expo exhibitor lists
**Examples:** BioAsia, India MedTech Expo, analytica Lab India, CPhI India, India Lab Expo, agro-biotech expos, state export summits.

**Why it works:** Exhibitors are actively selling, investing in market presence, and usually have enough scale to care about process and capability building.

**Limitations:** Exhibitor lists include traders, agents, and brand resellers. The list needs a post-filter for manufacturing and promoter fit.

### 4) Product catalog ecosystems
**Examples:** company websites, IndiaMART / TradeIndia / ExportersIndia / Justdial / Kompass / Thomasnet-style listings, plus product catalog PDFs and buyer manuals.

**Why it works:** Product catalogs expose actual manufacturing depth faster than a generic “about us” page.

**Limitations:** Many profiles are commercial listings, not primary sources. Use them for discovery, then verify on the company’s own site.

### 5) Hiring and career signals
**Examples:** LinkedIn jobs, Naukri, careers pages, recent hiring posts, role count changes, campus recruitment notices.

**Why it works:** A company hiring across QA, production, R&D, regulatory, operations, or business development is usually in motion.

**Limitations:** Hiring alone is not enough. A service company can also be hiring aggressively.

### 6) News, awards, and launch announcements
**Examples:** press releases, local business news, state government news, product-launch articles, expansion news, facility inaugurations, export announcements.

**Why it works:** These often reveal the exact personalization hook needed for first outreach.

**Limitations:** News coverage can be PR-heavy. It should be treated as a signal, not proof.

### 7) Unconventional but effective methods
- search by **product class** rather than company name
- search for **factory address + product**
- use **founder education filters** on LinkedIn
- search **conference speaker lists** for technical founders
- reverse-search **export/import records** for technical product names
- mine **incubator cohorts** at CDFD, CCMB, T-Hub, MedTech Park, Genome Valley, and similar institutions

**Why it works:** These methods surface companies before they become obvious on generic Google queries.

**Limitations:** They are discovery tools, not validation tools.

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

### Hand-drawn diagram to send in chat
Draw a funnel with these stages:

Raw universe → dedupe → manufacturer filter → founder/technical filter → growth signals → manual QA → 1,000 ICP companies

Under each stage, write the tools used:
- search / directories
- website parsing
- LLM classification
- LinkedIn / news / MCA
- human audit

At the bottom, show weekly boxes:
- Week 1: Universe
- Week 2: Filter
- Week 3: Enrich
- Week 4: QA + export
