# TDS-Virtual-TA
# TDS Course Knowledge Base Builder (TA Assistant)

This project builds a searchable AI-ready knowledge base for the **TDS course** by collecting, cleaning, chunking, and embedding:

- Course website documentation
- Discourse forum discussions

It is designed to help **Teaching Assistants (TAs)** quickly retrieve accurate answers from official course material and past student discussions using semantic search or RAG-based chatbots.

---

## Features

- Scrapes authenticated Discourse forum threads
- Crawls course website pages
- Cleans and normalizes HTML/Markdown content
- Splits content into overlapping semantic chunks
- Stores structured data in SQLite
- Generates vector embeddings for retrieval systems
- Ready backend for chatbot / semantic QA pipelines

---

## Project Structure
.
├── scraper_discourse.py        # Scrapes Discourse forum threads
├── scraper_course.py          # Crawls course website and saves markdown
├── preprocess.py               # Cleans, chunks, embeds, and stores data
├── downloaded_threads/         # Raw Discourse JSON threads
├── markdown_files/             # Crawled markdown pages + metadata
├── knowledge_base.db           # SQLite database with chunks + embeddings
└── README.md

---

## Requirements

- Python 3.9+
- Playwright
- BeautifulSoup
- markdownify
- aiohttp
- tqdm
- python-dotenv

## Architecture 
Discourse + Website
        ↓
 Scrapers & Crawlers
        ↓
  Clean + Chunk
        ↓
   SQLite Storage
        ↓
   Vector Embeddings
        ↓
  RAG / Chatbot Layer


# TDS Knowledge Base System — Overview

This system builds a structured knowledge base for the TDS course by combining:

- Course website documentation
- Historical Discourse forum discussions

It cleans, chunks, embeds, and stores all content into a vector-enabled SQLite database for semantic search and chatbot systems.

Primary users: Teaching Assistants and course staff.




