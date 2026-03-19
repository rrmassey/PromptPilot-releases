# PromptPilot: Evidence-Based AI Verification & Grounding

PromptPilot is a high-fidelity verification engine designed to neutralize AI hallucinations and uphold academic integrity. It bridges the gap between generative AI and empirical rigor by orchestrating ground-truth data retrieval and independent AI-driven adjudication.

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)]()
[![Privacy: Local-First](https://img.shields.io/badge/Privacy-Local--First-blue.svg)]()

---

## 1. What is PromptPilot?

PromptPilot is a specialized platform for researchers, students, and academics who rely on Large Language Models (LLMs) but require absolute factual accuracy. 

Unlike standard LLM interfaces that rely on the model's static training data, PromptPilot treats the LLM as an expert adjudicator that must base its decisions on real-time evidence gathered from trusted external sources. The result is a system that identifies claims, gathers supporting or refuting evidence, and provides a transparent audit trail for every verification.

---

## 2. Why PromptPilot?

The rapid adoption of AI in academia has introduced two critical challenges:
1.  **Hallucinations:** LLMs frequently manufacture plausible-sounding but entirely fabricated citations and facts.
2.  **Data Privacy:** Uploading sensitive research or unfinished manuscripts to cloud AI providers poses significant intellectual property risks.

PromptPilot was built to solve these problems by prioritizing **grounding** and **privacy**. By combining specialized RAG (Retrieval-Augmented Generation) workflows with a local-first desktop architecture, PromptPilot allows researchers to verify their work without compromising the security of their data.

---

## 3. Core Capabilities

-   **Hybrid RAG Architecture:** Interrogates document context alongside real-time searches from scholarly registries (CrossRef, OpenAlex) and the live web (Brave Search).
-   **Local-First Privacy:** All primary document processing, AI detection, and citation highlights occur locally on the user's machine.
-   **Tiered Adjudication:** Supports both high-speed model grounding and deep-reasoning adjudication for complex factual analysis.
-   **Local LLM Integration:** Full support for Ollama and LM Studio, enabling a completely offline verification pipeline.
-   **High-Fidelity Reporting:** Generates structured verification logs and PDF reports that detail the exact source and reasoning used for each claim.

---

## 4. Methodology

PromptPilot follows a rigorous three-stage verification lifecycle:

1.  **AI Detection:** Specialized prompts parse the text to identify potential citations and factual claims.
2.  **Evidence Gathering:** The engine queries academic registries and the web to retrieve bibliographic metadata and source content.
3.  **Adjudication:** A Reasoning Model (e.g., Gemini 2.0 Pro) analyzes the "evidence packet" using a priority-based logic: Direct Link → Scholarly Database → Web Grounding.

---

## 5. Technical Implementation

-   **Frontend:** React 18, Vite, TypeScript (Strict Mode).
-   **Desktop Bridge:** Tauri (Rust) for native OS integration and local security.
-   **Styling:** A custom "High-Contrast Matte" design system utilizing Vanilla CSS and glassmorphism.
-   **Backend:** Firebase Cloud Functions (BFF) for secure provider orchestration and API key management.
-   **AI Orchestration:** Native integration with Gemini SDK and local Ollama servers.

---

## 6. Getting Started

### For Users
The simplest way to use PromptPilot is to download the latest version of the desktop application directly from our website.
-   **Official Website:** [promptpilot.app](https://aipromptpilot.vercel.app)
-   **Platforms:** Support for macOS (Apple Silicon & Intel) and Windows (x64 & ARM64).

---

## 7. Privacy & Data Governance

PromptPilot is designed with a zero-knowledge approach to user data.
-   **No Cloud Caching:** User-uploaded document text is never cached on our servers.
-   **Secure Credential Storage:** API keys are stored in the native OS vault through the Tauri bridge.
-   **Local Persistence:** Session data, chat history, and verification results remain on your local hardware.
