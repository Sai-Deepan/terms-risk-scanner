# ⚠️ Terms Risk Scanner

> Warns you before companies exploit you.

A browser extension that scans Terms & Conditions in real-time and highlights **risky, abusive, or misleading clauses** before you click “Agree”.

---

## What It Does

Instead of dumping long summaries, this extension:

* **Detects risky clauses** in Terms of Service / Privacy Policies
* **Classifies them into clear categories**
* **Interrupts user decisions** with a warning popup
* **Highlights exact lines** that matter

---

## Problem

Nobody reads Terms & Conditions.

Companies exploit this by hiding:

* Data selling clauses
* Auto-renewal traps
* Legal protections against users
* Ownership claims over user content

Result: users blindly agree to things that harm them.

---

## Solution

A real-time **risk detection engine** that:

1. Extracts Terms & Conditions content from web pages
2. Breaks it into clauses
3. Classifies each clause into risk categories
4. Displays only what matters

---

## ⚠️ Risk Categories (Core Engine)

Each clause is classified into:

* **Data Harvesting**

  * Selling or sharing user data
* **Liability Clauses**

  * Company avoids responsibility
* **Auto-Renewal / Payments**

  * Hidden billing traps
* **Arbitration / Legal Restrictions**

  * Limits user legal rights
* **Content Ownership**

  * Company owns your uploads
* **Tracking / Location Abuse**

  * Excessive tracking permissions

---

## 🖥️ User Experience

### 1. User lands on a Terms page

### 2. Extension scans in background

### 3. Before clicking “Accept” → popup appears:

```
⚠️ WAIT — THIS POLICY HAS RISKS

🔴 They can SELL your data  
🟡 Auto-renewal billing  
🟡 No refunds allowed  

[Continue Anyway]   [Read Details]
```

### 4. Highlighted clauses show exact risks

---

## 🏗️ Architecture

### 1. Text Extraction

* Detect Terms/Privacy pages
* Parse DOM → clean text

### 2. Chunking

* Split into paragraphs / clauses

### 3. Classification Engine

Each chunk →

```
{
  risk_type: string,
  severity: High | Medium | Low,
  explanation: string
}
```

### 4. Aggregation

* Combine results
* Assign overall risk score:

  * 🟢 Safe
  * 🟡 Moderate
  * 🔴 Risky

### 5. UI Layer

* Popup warnings
* Inline highlights

---

## Tech Stack (MVP)

* Chrome Extension (Manifest V3)
* JavaScript / TypeScript
* LLM API (OpenAI or local model)
* Optional: embeddings for caching

---

## 📅 Roadmap

### Week 1

* Extension skeleton
* Detect ToS pages
* Extract text

### Week 2

* Basic classification using LLM
* Implement risk categories

### Week 3

* Popup warning UI
* Highlight risky clauses

### Week 4

* Test across major sites
* Improve accuracy + speed

---

## ⚠️ Challenges

| Problem            | Solution                    |
| ------------------ | --------------------------- |
| Messy HTML pages   | Clean parsing + heuristics  |
| LLM hallucinations | Strict prompts + validation |
| Slow response      | Cache results per domain    |
| Repeated scans     | Store processed domains     |

---

## 🧠 Future Vision

This is not just a browser extension.

This becomes:

### → Global Terms & Conditions Risk Dataset

Future possibilities:

* Rank companies by “User Trust Score”
* Public database of risky policies
* API for browsers / privacy tools
* Enterprise compliance tools

---

## 📈 Positioning

❌ “AI summarizer” → weak, crowded
✅ “Protects users from exploitation” → powerful

---

## 🔒 Core Principles

* **Speed > perfection**
* **Clarity > complexity**
* **Actionable > descriptive**
* **Interrupt decisions, don’t just inform**

---

## 🛠️ Getting Started

```bash
git clone https://github.com/Sai-Deepan/terms-risk-scanner
cd terms-risk-scanner
```

1. Load extension in Chrome:

   * Go to `chrome://extensions`
   * Enable Developer Mode
   * Click "Load unpacked"

2. Open any Terms & Conditions page

3. See risks instantly

---

## Contributing

Contributions are welcome:

* Improve classification accuracy
* Add new risk categories
* Optimize performance
* Enhance UI/UX

---

## 📜 License

MIT License
