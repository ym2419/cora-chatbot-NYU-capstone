# CORA Chatbot – Backend Configuration Guide

This document outlines the full configuration used to develop the CORA chatbot on Microsoft Copilot Studio. The goal is to help others replicate the chatbot in a new environment.

---

## 🧠 Overview

- **Name:** CORA: Chatbot for Reproductive Access  
- **Purpose:** Assist users with information about abortion rights, laws, and self-managed abortion care  
- **Languages Supported:** English & Spanish  
- **Knowledge Source:** Uploaded PDFs + specific URLs (no browsing)

---

## 🗃️ Knowledge Base

**Files:**
- Self-Managed-Abortion-Report-2024.pdf
- CRR-Fact-sheet-on-WHO-Guidelines.pdf
- Self-managed-abortion-Legal-Analysis-by-Country.pdf
- Self-managed-Abortions6.pdf

**Links:**
- https://reproductiverights.org/
- https://reproductiverights.org/self-managed-abortion/
- https://reproductiverights.org/self-managed-abortion/sweden

---

## ⚙️ Agent Settings

### General Instructions:
> “Do not respond to any topic not related to Reproductive rights, such as redesign living room, or help me shop or the weather or dinner recipes. If asked about other topics you should answer ‘I’m here to assist with questions about abortion rights, legal protections, and access to self-managed abortion care. Please ask me something within that scope.’”

### Language Detection:
- Auto-detect language
- Default to English unless Spanish is detected

---

## 🧬 Generative AI Settings

| Setting                        | Value            |
|-------------------------------|------------------|
| Agent Type                    | Generative       |
| Content Moderation            | High (more precise) |
| Image Input                   | Disabled         |
| Knowledge Base Browsing       | Disabled         |

---

## 🔐 Authentication Settings

| Option                      | Selected        |
|----------------------------|-----------------|
| Authentication             | None (Public)   |

---

## 🧩 Topics

There are 4 custom topics:
- Greeting
- Goodbye
- Thank you
- Start Over

System topics like Fallback, End of Conversation, and Escalation are also enabled.

Screenshots for each topic, trigger, and fallback response are saved in `/chatbot_config/screenshots/`.

---

## 🔁 Fallback Logic

If the prompt is outside scope (e.g., unrelated topic), the chatbot responds with:

> *“I’m here to assist with questions about abortion rights, legal protections, and access to self-managed abortion care. Please ask me something within that scope.”*

---

## 📌 Notes

- The chatbot was published on **April 10, 2025**
- Project created by **Yasmin Marsh** for NYU SPS Capstone Project

