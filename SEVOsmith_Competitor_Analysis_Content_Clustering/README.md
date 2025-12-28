# 🛠️ SEVOsmith - The Strategy Architect
## Competitor Analysis & Content Clustering with n8n and DataForSEO

## 📋 Overview
This workflow is the intelligence core of the SEVOsmith suite. It automates the end-to-end process of **Competitor Analysis**—identifying market leaders and dissecting their traffic sources—to generate a cohesive **Pillar and Cluster Content Strategy**. By transforming raw SERP data into a structured roadmap, it allows agencies to move from "Research" to "Execution" in minutes.

---
![SEVOsmith Keyword Orchestrator n8n Workflow](Competitor-Analysis-Content-Clustering-with-n8n-and-DataForSEO.jpg)

<br>

[![Get it on Gumroad](https://img.shields.io/badge/Get%20the%20Workflow-Gumroad-%23FF90E8?style=for-the-badge&logo=gumroad)](https://nextgrowth.gumroad.com/l/competitor-analysis-content-clustering-with-n8n-DataForSEO)

> **Note:** This workflow is available as a FREE template on Gumroad. While completely free to download, optional tips are greatly appreciated and help support continued development and new features!
<br>

👉**Ready to turn your content strategy into published articles?**  

Check out **[SEVOsmith: The Autonomous n8n System for AI-Citable Content](https://nextgrowth.ai/sevosmith-ai-citable-content-engine/)** to automate the entire production workflow—from research to publication.

## 🎯 1. User Input & Strategy Modes
The workflow starts via a Form with three distinct operational modes to suit your specific goal:

### 🔭 Mode A: Topic Explorer (Market Research)
*   **Input:** Seed Keywords (e.g., "AI CRM", "Vegan Leather").
*   **Goal:** "I want to enter a niche but don't know who the players are."
*   **Logic:** Auto-discovers the top 100 organic competitors via DataForSEO, filters out directories (Yelp, Clutch), and isolates the true market leaders.

### 🛡️ Mode B: Domain Defender (Gap Analysis)
*   **Input:** Your Website URL.
*   **Goal:** "Who is stealing my traffic?"
*   **Logic:** Identifies direct rivals who rank for the same keywords you do, allowing you to close content gaps.

### 🎯 Mode C: Manual Analysis (The Sniper)
*   **Input:** Specific Competitor Domains (comma-separated).
*   **Goal:** "I want to reverse-engineer `competitor-x.com` specifically."
*   **Logic:** Bypasses discovery APIs to perform a surgical audit on the exact domains you provide.

---

## ✨ Key Features
*   **⚡ The "Competitor Collector":** A smart aggregation engine that merges API discovery with manual inputs, removes duplicates, filters out non-business giants (Wikipedia, LinkedIn), and prioritizes the most relevant threats.
*   **💎 "Money Page" Forensics:** Instead of crawling entire sites, the system identifies the specific URLs driving the highest **Estimated Traffic Value (ETV)** and extracts their winning keywords (Page 1 rankings only).
*   **🧠 Semantic Strategy Engine:** An AI Agent acts as a Senior SEO Strategist, organizing scattered keywords into a logical **Pillar & Cluster Architecture** to build topical authority.
*   **🛡️ Smart Data Upsert:** When saving to Google Sheets, the workflow intelligently merges new data with old data—ensuring you never overwrite rich historical metrics with empty data from a quick manual run.
*   **📂 Dual-Stream Output:** Simultaneously generates a **Strategic Strategy Document** (MS Word) for stakeholders and an **Actionable Content Database** (Google Sheets) for production teams.

---

## ⚙️ How It Works

### 1. The Extraction Loop
For every identified competitor (from any Strategy Mode), the system executes a recursive analysis cycle:
1.  **Fetch Top Pages:** Retrieves the top 5-10 pages sorted by traffic value.
2.  **Extract Winning Keywords:** Pulls the top 50 keywords ranking on Page 1 for those specific URLs.
3.  **Intent Filtering:** Automatically discards "Navigational" (Branded) keywords to focus purely on Commercial and Informational opportunities.

### 2. Strategic Synthesis (The AI Agent)
The cleaned market data is aggregated and sent to a **Master Strategist AI**. The AI analyzes content gaps and outputs:
*   **Market Opportunity Score:** Total addressable volume and difficulty.
*   **Content Architecture:** 3-5 Core Pillars and supporting Cluster articles.
*   **Quick Wins:** A list of High Volume / Low Difficulty keywords to target immediately.

### 3. Production & Delivery
The workflow splits the AI's output into two parallel workstreams:
*   **Stream A (The Document):** Converts the Markdown strategy into a formatted HTML/Word document, names it dynamically (e.g., `Strategy__Client-Name__Date.docx`), and saves it to a designated **Google Drive Folder**.
*   **Stream B (The Database):** Parses the article plan into structured JSON and appends it to **Google Sheets** (`Content_Plan` tab) for project management.
*   **Notification:** Sends a summary Email with direct links to the Strategy Doc, Research Report, and Spreadsheet.

---

## 🛠️ Tech Stack & APIs
*   **Data Source:** DataForSEO (`serp_competitors`, `competitors_domain`, `relevant_pages`, `ranked_keywords`).
*   **Intelligence:** Google Gemini / OpenAI (via LangChain).
*   **Logic:** Javascript (n8n Code Nodes) for complex data flattening and file handling.
*   **Storage:** Google Drive & Google Sheets.
*   **Notification:** Gmail.

## 📊 Output Data Model (Google Sheets)
The workflow populates two specific tabs:

**1. Raw_Competitor_Data (The Evidence):**
*   `Competitor` & `Target Page`
*   `Keyword`, `Search Volume`, `CPC`
*   `Difficulty` & `Top Bid`
*   `Ranking Value ($)` & `Yearly Trend`

**2. Content_Plan (The Action Plan):**
*   `Article ID` & `Type` (Pillar/Cluster)
*   `Primary Keyword` & `Secondary Keywords`
*   `Purpose / Angle` & `Priority`
