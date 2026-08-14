# PromptPilot: Evidence-Based AI Citation Verification & Research Grounding

PromptPilot is a local-first desktop verification engine designed to cross-examine AI-generated citations and claims against verified scholarly registries. It bridges the gap between generative AI and empirical rigor through real-time bibliographic retrieval, client-side PDF extraction, and local LLM reasoning.

[![Privacy: Local-First](https://img.shields.io/badge/Privacy-100%25%20Local--First-brightgreen.svg)]()
[![Platform: macOS | Windows](https://img.shields.io/badge/Platform-macOS%20%7C%20Windows-lightgrey.svg)]()

---

## 1. What is PromptPilot?

PromptPilot is a specialized desktop platform for researchers, students, and professionals who use Large Language Models (LLMs) and require independent verification of citations, quotes, and factual claims.

Rather than relying on static training data or unverified web summaries, PromptPilot extracts bibliographic anchors from user documents and cross-references them against public academic databases and verified search APIs. The result is a transparent, auditable breakdown showing whether a referenced paper, DOI, or claim exists in real-world scholarly literature.

---

## 2. Why PromptPilot?

The rapid adoption of generative AI in research and writing has introduced two major challenges:
1. **Citation Hallucinations:** LLMs frequently produce plausible-sounding but fabricated authors, paper titles, journal names, and non-existent DOIs.
2. **Data Confidentiality:** Transmitting sensitive manuscripts, proprietary drafts, or unfinished research to third-party cloud servers poses intellectual property and privacy risks.

PromptPilot solves both challenges through a **strictly local-first architecture**: your documents, chat sessions, and extracted text never leave your machine during local AI processing.

---

## 3. Core Capabilities

- **Academic Registry Grounding:** Queries public scholarly databases (CrossRef, OpenAlex, ArXiv, Wikipedia, Semantic Scholar, Unpaywall) to verify paper existence, authors, publication years, and DOIs.
- **Local-First Processing:** Document text extraction and local LLM inferences execute entirely on your device via loopback interfaces (`127.0.0.1`).
- **Integrated Local LLM Engine:** Native support for built-in local inference (`llama-server` / GGUF), as well as Ollama and LM Studio servers.
- **Client-Side Document Parsing:** High-performance local text extraction for PDFs (via Apache-2.0 LiteParse) and DOCX files.
- **Pre-Flight PII Redaction:** Automatically scrubs personal identifiable information (emails, phone numbers, API keys) from search queries before external registry lookups.
- **Hardware-Backed Credential Security:** Search API keys (Brave Search, Tavily) are encrypted and stored in your native OS credential vault (macOS Keychain / Windows Credential Manager).
- **Exportable Audit Reports:** Generates structured verification logs and PDF reports complete with regulatory disclaimers and methodology audit trails.

---

## 4. Verification Methodology

PromptPilot follows a structured verification pipeline:

1. **Extraction & Parsing:** Client-side extractors parse the document text, separating prose, citations (APA, MLA, Chicago, IEEE), and inline markers.
2. **Bibliographic Grounding:** The engine searches scholarly registries for candidate DOI, title, and author matches using rate-limited, polite API pools.
3. **Adjudication & Cross-Examination:** The model evaluates the gathered evidence packet against the document claim using deterministic verification rules (Verified, Unverified, Ambiguous, Contradicted).

---

## 5. Technical Implementation

- **Desktop Framework:** Tauri v2 (Rust) for native OS performance, memory isolation, and OS Keyring integration.
- **Frontend:** React 18, TypeScript (Strict Mode), Vite.
- **PDF Extraction Engine:** LiteParse (Apache-2.0 / PDFium) bundled runtime.
- **Styling:** Custom High-Contrast Matte design system with Vanilla CSS and responsive glassmorphism.
- **Local Storage:** Client-side IndexedDB (`LocalCacheService`) and AES-256-GCM encrypted local state. Zero cloud database dependency.

---

## 6. Installation & Downloads

PromptPilot is distributed as a standalone desktop application for macOS and Windows.

- **Official Website:** [aipromptpilot.vercel.app](https://aipromptpilot.vercel.app)
- **Direct Downloads:**
  - **macOS:** Download the `.dmg` installer (Apple Silicon & Intel supported) from the website.
  - **Windows:** Download the `.exe` / `.msi` installer from the website.

Simply download and run the installer for your platform to get started with the Free Community Tier.

---

## 7. Privacy & Data Governance

PromptPilot is engineered from the ground up with a zero-knowledge privacy philosophy:
- **No Central Document Storage:** PromptPilot operates no servers that store your documents, prompts, or chat histories.
- **Zero In-App Telemetry on Desktop:** The desktop application contains no analytics SDKs, advertising trackers, or behavioral telemetry.
- **Data Portability & Erasure:** Full compliance with GDPR (Art. 17 & 20) and CCPA—export all data to JSON or purge all local stores with a single click in Settings.
- **Opt-In Web Analytics:** Public website analytics are strictly opt-in and automatically respect browser Global Privacy Control (GPC) signals.

---

## 8. Legal & Regulatory Advisory

*PromptPilot is an academic research assistance tool and verification aid. Automated AI verifications are probabilistic and should not be used as a substitute for primary-source review. PromptPilot does not provide legal, financial, or medical advice.*
