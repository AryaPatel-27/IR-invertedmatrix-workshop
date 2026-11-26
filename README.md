
# PROG8245 — Inverted Matrix Workshop

**Group 5 | Machine Learning Programming**

## Project Overview

In this workshop, our team used Python to build a simple information retrieval system using blog posts from the Python Software Foundation.

We collected documents, cleaned and tokenized the text, removed stop words, and applied stemming. We then built an inverted index to connect words with the documents where they appear.

We also implemented Boolean retrieval, biword and positional indexes, phrase searches, and TF-IDF calculations to understand how search engines retrieve and rank documents.

Finally, we explored how these information retrieval techniques can support Retrieval-Augmented Generation (RAG) and AI agents.

## Team Members

**Group 5**

- Arya Patel
- Preethi Vasudevan Nair
- Asangika Hettiarachchi
- Alamir Ibrahim

## Dataset

We used blog posts from the [Python Software Foundation News blog](https://pyfound.blogspot.com/).

The notebook downloads posts using the [PSF RSS feed](https://pyfound.blogspot.com/feeds/posts/default?alt=rss), removes HTML tags, and combines each post's title and body.

In our saved execution, we collected:

- **25 documents**
- **2,768 unique words** before stop-word removal and stemming

These numbers may change because the RSS feed is updated with new posts.

**Dataset license:** A reuse license for the blog posts has not been verified.

## Workshop Implementation

### 1. Document Collection and Tokenization

- Collected blog posts using an RSS feed.
- Removed HTML tags from the content.
- Combined titles and blog content.
- Converted text into lowercase tokens.
- Calculated document and vocabulary counts.

### 2. Linguistic Processing

- Removed common English stop words using NLTK.
- Applied Porter stemming to reduce related word forms.
- Demonstrated suffix stripping using words such as `playing`, `connected`, and `running`.
- Applied the same preprocessing pipeline to documents and search queries.

### 3. Inverted Index and Boolean Retrieval

- Created an inverted index mapping terms to document IDs.
- Implemented Boolean AND queries.
- Implemented Boolean AND NOT queries.
- Tested document retrieval using `python` and `softwar`.

### 4. Biword and Positional Indexes

- Built a biword index containing consecutive token pairs.
- Created a positional index recording word positions.
- Implemented phrase searches using positional matching.
- Compared biword and positional search results.

Example searches:

- `Python software` — 13 matching documents
- `Python community` — 19 matching documents

Both methods returned matching document IDs in our saved execution.

### 5. TF-IDF Calculation and Document Ranking

- Calculated term frequency (TF).
- Calculated inverse document frequency (IDF).
- Combined TF and IDF to calculate TF-IDF scores.
- Ranked documents based on the calculated scores.

For the term `softwar` in Document 0:

- TF = 3
- IDF = 0.446287
- TF-IDF = 1.338861

Documents with higher scores for the term were ranked above those with lower scores.

### 6. Applications in RAG and AI Agents

We explored how information retrieval can support AI applications.

**Retrieval-Augmented Generation (RAG):**

A RAG system can retrieve relevant documents and provide their contents to a language model to help generate an answer.

**AI Agents:**

AI agents can use document retrieval to find information needed for tasks such as searching articles, comparing results, and preparing summaries.

These applications were discussed as examples. The workshop does not implement a complete RAG system or autonomous AI agent.

## Technologies Used

- Python
- Jupyter Notebook
- VS Code
- NLTK
- Pandas
- Requests
- Feedparser
- BeautifulSoup

## How to Run the Notebook

### 1. Clone the Repository

```bash
git clone https://github.com/AryaPatel-27/IR-invertedmatrix-workshop.git
```

### 2. Open the Project

Open the cloned project folder in Visual Studio Code.

### 3. Create a Virtual Environment

In Windows PowerShell:

```powershell
py -m venv .venv
```

### 4. Install Required Packages

```powershell
.\.venv\Scripts\python.exe -m pip install ipykernel requests feedparser beautifulsoup4 nltk pandas
```

### 5. Download NLTK Resources

```powershell
.\.venv\Scripts\python.exe -m nltk.downloader stopwords
```

### 6. Run the Notebook

1. Open `IR_InvertedMatrix_Workshop.ipynb`.
2. Select the `.venv` Python kernel.
3. Run the notebook cells in order.
4. Review the generated outputs and observations.

**Note:** Internet access is needed to retrieve the RSS feed and download missing NLTK resources.

## Results and Observations

From this workshop, our team learned how document preprocessing helps build a searchable collection.

We observed that inverted indexes make it easier to identify documents containing specific words. Boolean queries allow us to combine search conditions, while biword and positional indexes help with phrase searches.

We also learned that TF-IDF can help rank documents by measuring the importance of a search term.

These techniques form a foundation for document search, RAG systems, and retrieval tools used by AI agents.

## GitHub Repository

[IR-invertedmatrix-workshop](https://github.com/AryaPatel-27/IR-invertedmatrix-workshop)

## Submission

This workshop was prepared by Group 5 for PROG8245 — Machine Learning Programming.

The submission PDF includes the team members' names, student IDs, and GitHub repository link.

The notebook's course submission command references `submit_assignment.py`, which was not included in the available project files. The submission script must be obtained from the instructor if its execution is required.
