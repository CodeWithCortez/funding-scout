# Funding-Scout

A Python project powered by [CrewAI](https://github.com/crewai/crewai) that:
1. Searches the internet (via SerperDevTool) for a single grant matching a user-specified topic.
2. Saves that grant’s key details into `search_results.json`.
3. Automatically drafts a complete grant proposal in Markdown, based on your program description.

This repository contains all code, configuration files, and instructions to get started. No prior experience with CrewAI is required—just follow the steps below.

---

## 🔍 Project Overview

When you run the script, it performs two main steps:

1. **Funding-Source Scout**  
   - Uses the SerperDevTool to issue a web search for your topic (e.g. “workforce grants” or “STEM after-school grants”).  
   - Retrieves exactly 1 grant result (title, funder, URL, etc.) and writes it to `search_results.json`.

2. **Grant Writer**  
   - Reads that single grant from `search_results.json`.  
   - Uses an OpenAI LLM to draft a fully formatted grant proposal in Markdown (saved as `proposal.md`), incorporating your program description.

The result: you get one real-world grant opportunity plus a complete proposal you can submit or modify further.

---

## ⚙️ Prerequisites

1. **macOS or Linux (Windows 10+ with WSL)**  
2. **Python 3.11** (recommended)  
   - (Wheels for CrewAI dependencies, including `tiktoken`, are pre-built for 3.11.)  
3. **Git** (to clone this repository)  
4. **A Serper API Key** (for web search)  
   - Sign up at [Serper.dev](https://serper.dev/) → copy your `SERPER_API_KEY`.  
5. **An OpenAI API Key** (for grant writing)  
   - Sign up at [OpenAI](https://platform.openai.com/) → copy your `OPENAI_API_KEY`.

---

## 🛠️ Installation & Setup

1. **Clone this repository**  
   Open a terminal and run:
   ```bash
   git clone https://github.com/<YourGitHubUsername>/funding-scout.git
   cd funding-scout
