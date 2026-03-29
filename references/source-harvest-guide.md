# Source Harvest Guide — Expanded Strategies Per Source Type

This file provides deep tactical guidance for harvesting each source type.
Read the relevant sections when a source type is underperforming or producing sparse results.

---

## 🌐 Source Type 1: Encyclopedic & Reference

### Best sources
- Wikipedia (always start here — rich interlinking)
- Britannica (often more authoritative, less crowdsourced)
- Stanford Encyclopedia of Philosophy (for philosophy, logic, ethics)
- Investopedia (finance, economics)
- WebMD / Mayo Clinic (medicine)
- MDN Web Docs / DevDocs (web technology)
- NIST (science, engineering, standards)

### Deep harvest strategy
1. Fetch the main Wikipedia article with `web_fetch`
2. Extract ALL wikilinks in the "See also" section — fetch each
3. Check the Wikipedia article's "References" section — the most-cited sources are often Tier 1
4. Fetch the "Talk" page for controversies and editorial debates
5. Search Britannica for the same topic — often written differently, catching gaps

### When results are thin
- Try domain-specific encyclopedias: e.g., "Encyclopedia of [field]"
- Search `"[topic]" site:*.edu` to find university reference pages
- Try older reference terms: historical names or synonyms for the concept

---

## 📰 Source Type 2: News & Current Developments

### Best sources
- Reuters, AP News (wire services — reliable, fast)
- Nature News, Science (for scientific topics)
- Financial Times, Bloomberg, WSJ (for economic/business topics)
- MIT Technology Review, Wired, Ars Technica (technology)
- The Atlantic, New Yorker (long-form analysis)
- Domain-specific trade publications

### Deep harvest strategy
1. Search for news from the past 12 months first — most recent developments
2. Then search for "landmark" moments: first breakthrough, major controversy, policy change
3. Use `web_fetch` to get full articles — avoid snippets
4. Look for "timeline of [topic]" articles — these consolidate history + recent events
5. Search for the "controversy" angle specifically — this often surfaces lesser-known perspectives

### When results are thin
- Try Google News search queries: `"[topic]" news after:2023`
- Search for the topic in industry trade press
- Look for regulatory filings or press releases about the topic

---

## 🎓 Source Type 3: Academic & Research

### Best sources by domain
- **All fields**: Google Scholar, ResearchGate, Semantic Scholar
- **Science/Medicine**: PubMed (pubmed.ncbi.nlm.nih.gov), Nature, Science, Cell
- **Computer Science**: arXiv.org (cs.* sections), ACM Digital Library, IEEE Xplore
- **Social Science**: SSRN, JSTOR, Brookings
- **Economics**: NBER (nber.org), AEA journals
- **Psychology**: APA PsycINFO, PsycNet
- **Physics/Math**: arXiv.org (physics.*, math.*), APS journals

### Deep harvest strategy
1. Find the **most-cited paper** on the topic (search "most cited [topic] paper")
2. Find the **most recent systematic review or meta-analysis** — these synthesize dozens of papers
3. Fetch the abstract + conclusion section (not always the full paper)
4. From a key paper, follow: "cited by" (who built on it) + "references" (what it built on)
5. Search for the **original/seminal paper** that defined the concept
6. Look for **review articles** in prestigious journals — they summarize entire subfields

### When results are thin
- Try discipline-specific search terms (technical jargon, not lay terms)
- Search for the names of key researchers in the field + their publications
- Try `"[topic] preprint"` or `"[topic] working paper"`

### What to extract from academic sources
- Abstract: core claim, methodology, key finding
- Conclusion: what the authors say the results mean
- Limitations section: honest accounting of what the research can't tell us
- References: the 3–5 most-cited references in the paper's bibliography

---

## 📚 Source Type 4: Books & Long-form Educational

### Best sources
- Google Books previews (substantial excerpts freely available)
- Open Library (archive.org/details/openlibrary)
- OpenStax (free, peer-reviewed textbooks)
- MIT OpenCourseWare reading lists (ocw.mit.edu)
- Stanford, Yale, Harvard OpenCourseWare
- Project Gutenberg (for historical/classic texts)
- Annual Review of [field] — authoritative yearly summaries

### Deep harvest strategy
1. Search "best books [topic] recommended" — find the canonical texts
2. Search `"[topic]" site:ocw.mit.edu` — find MIT course syllabi and reading lists
3. Use Google Books: search the topic, then look at the preview pages — often substantial
4. Search "[book title] summary key points" — many canonical books have high-quality summaries
5. Search "[topic] open textbook" — many fields have free, peer-reviewed textbooks online
6. Look for "Annual Review of [field]" articles — these are book-length treatments of subtopics

### What to extract
- Table of contents → reveals the canonical structure of the field
- Preface/introduction → tells you what the author thinks is most important
- Chapter summaries → key findings and arguments per section
- Glossary → authoritative definitions

---

## 💬 Source Type 5: Forums & Expert Communities

### Best sources by topic type
- **Technical topics**: Stack Overflow, Stack Exchange (100+ topic-specific sites)
- **Science**: r/science, r/askscience, r/[field] subreddits
- **General questions**: Quora (look for answers by verified experts)
- **Tech/startup/research**: Hacker News (news.ycombinator.com) — high-quality discussion
- **Domain-specific**: Physics Forums, Math Stack Exchange, Cross Validated (statistics), Biology Stack Exchange, etc.

### Deep harvest strategy
1. Search `"[topic] explained" site:reddit.com` — find high-karma explainer posts
2. Search `"[topic]" site:stackoverflow.com` — for technical topics, find canonical Q&As
3. Search `"[topic] ELI5" site:reddit.com` — intuitive explanations often here
4. On Stack Exchange, look for **"accepted" answers** with high votes — these are reviewed for accuracy
5. Search HN: `"[topic]" site:news.ycombinator.com` — look for top-level comments from domain experts
6. Look for **AMA (Ask Me Anything)** threads featuring experts on the topic

### What these sources are uniquely good for
- Intuitive explanations (ELI5, analogies)
- Practical "gotchas" and mistakes not in textbooks
- Expert opinions that aren't peer-reviewed but are insightful
- Disagreements between practitioners that don't show up in formal literature
- "Received wisdom" in the community — what practitioners actually believe vs. what papers say

### Quality filter for community sources
- High vote/karma score
- Long, detailed, cited answer
- Responder has relevant credentials mentioned
- Multiple people upvoted or agreed

---

## 🎥 Source Type 6: Video & Lecture Transcripts

### Best sources
- **MIT OpenCourseWare**: ocw.mit.edu — full lecture notes, transcripts, problem sets
- **Khan Academy**: khanacademy.org — structured, level-appropriate explanations
- **Coursera/edX syllabi**: fetch course pages for reading lists and outlines
- **TED talks**: search `"[topic]" site:ted.com` — look for the transcript on the talk page
- **YouTube**: search `"[topic] lecture"` — many university courses are on YouTube

### Deep harvest strategy
1. Fetch `ocw.mit.edu` course pages for the topic — download syllabi and lecture notes PDFs
2. Search `"[topic] transcript site:ted.com"` — TED transcripts are full-text accessible
3. For YouTube: search `"[topic] explained youtube"` then fetch the video page — YouTube auto-captions are accessible via `web_fetch`
4. Search `"[topic] online course notes"` — many instructors post their lecture slides/notes publicly
5. Coursera and edX course pages often include detailed syllabi — fetch them

### What these sources are uniquely good for
- Pedagogical structure: how experts teach this topic (what order, what analogies)
- Visual intuition translated to text (diagrams described in words)
- Common student misconceptions (instructors address them in lectures)
- Problem-solving approaches (how to think, not just what to know)

---

## 🔬 Source Type 7: Expert Blogs & Practitioner Writing

### Finding the right blogs
1. Search `"[topic] blog"` + add a field expert qualifier: "researcher", "practitioner", "engineer"
2. Search `"[topic] substack"` — growing home for serious long-form expert writing
3. Search `"[topic]" site:medium.com` — filter for authors with many followers or "featured" status
4. Search `"[expert name] blog"` once you know key figures in the field
5. Look for institutional blogs: e.g., Google AI Blog, Facebook Research, Fed Reserve blog, NHS blog

### Quality signals
- Author lists credentials / institutional affiliation
- Post has citations or links to sources
- Other experts in the field have linked to it
- Long-form (2000+ words) with structured argument
- Hosted on institutional domain or credentialed personal site

### What these sources are uniquely good for
- Practitioner perspective vs. theoretical understanding
- "What it's actually like" — messy reality vs. clean textbook version
- Nuanced takes on debates in the field
- Emerging thinking not yet in peer-reviewed literature
- Connections to adjacent fields that specialists notice but don't publish formally

---

## 🗺️ Source Type 8: Frameworks, Models & Structures

### Finding frameworks
1. Search `"[topic] framework"` — look for named models (e.g., "Maslow's hierarchy", "OSI model")
2. Search `"[topic] taxonomy"` — classification systems for the topic
3. Search `"[topic] mental model"` — how experts think about the topic
4. Search `"[topic] comparison table"` — side-by-side comparisons of variants
5. Search `"[topic] decision tree"` — step-by-step decision processes
6. Search `"types of [topic]"` or `"[topic] classification"` — categorical structures

### What to extract from framework sources
- The names and relationships of the categories/components
- The logic behind the structure (why these categories, not others)
- Edge cases: things that don't fit neatly into the framework
- The limitations/criticisms of the framework itself

### What frameworks add to the KB
- Structural clarity: how to organize the knowledge
- Vocabulary: the canonical names for sub-concepts
- Gaps revealed: what the framework acknowledges it doesn't cover

---

## ⚔️ Source Type 9: Criticisms, Debates & Alternative Perspectives

### This is often the MOST NEGLECTED source type — treat it as mandatory

### Finding criticisms
1. `"problems with [topic]"` — direct criticism search
2. `"[topic] is wrong"` or `"[topic] myth"` — debunking pieces
3. `"criticism of [topic]"` + `"academic"` or `"scholarly"` — formal critiques
4. `"[topic] replication crisis"` — for psychology/social science topics
5. `"limitations of [topic]"` — often found in the "limitations" section of papers
6. `"[topic] overrated"` or `"[topic] doesn't work"` — practitioner disillusionment
7. Search for the **historical opposition** to the topic when it was first proposed

### Finding alternative perspectives
1. `"alternative to [topic]"` — competitors, replacements, different approaches
2. `"[topic] vs [competing approach]"` — explicit comparisons
3. `"minority view on [topic]"` — academia sometimes has known minority positions
4. Search in different countries/regions — approaches can vary significantly across cultures
5. Search from a different **discipline's** perspective: "economist's view of [topic]", "sociologist's view of [topic]"

### What criticisms add to the KB
- Known failure modes of the mainstream view
- Edge cases the dominant framework can't handle
- Political/economic interests behind certain positions
- Historical examples of the mainstream view being wrong
- Intellectual humility: any field has limits

---

## 🔗 Source Type 10: Cross-Domain Connections

### Finding connections
1. `"[topic] and [adjacent field]"` — explicit connection searches
2. `"[topic] applied to [domain]"` — application areas
3. `"[field] borrows from [topic]"` — which fields use this as a foundation
4. `"interdisciplinary [topic]"` — formal interdisciplinary work
5. `"[topic] analogy [domain]"` — fields that use this topic as a metaphor
6. Search for surprising connections: `"[topic] and music"`, `"[topic] and biology"`, `"[topic] and economics"` — even if the connection seems unlikely

### Why cross-domain matters
- Reveals universal principles (the topic works in multiple contexts → it's robust)
- Reveals limits (the topic breaks down in some domains → boundaries of applicability)
- Provides new analogies that deepen understanding
- Often reveals cutting-edge applications not yet in mainstream literature
- Prevents tunnel vision — understanding how experts in OTHER fields use or criticize the concept

---

## General Harvest Principles

### Use web_fetch aggressively
`web_search` returns snippets. `web_fetch` returns full content. For any source that looks
relevant, always fetch the full page. A snippet rarely contains the mechanism, example,
or nuance needed to turn a WEAK answer into a STRONG one.

### Follow reference chains
When a high-quality source cites another source, fetch that cited source too.
The most important references in a field often appear repeatedly across many sources —
these are the canonical works that need to be in the source registry.

### Vary query phrasing
The same concept may be referred to by different names in different communities.
Technical term + lay term + historical name + abbreviation — search all of them.

### Signal vs. noise
Quantity of sources ≠ quality of KB. One excellent Tier 1 source that explains the
mechanism clearly is worth more than ten Tier 3 sources that repeat the same surface fact.
Prioritize depth over breadth at every step.
