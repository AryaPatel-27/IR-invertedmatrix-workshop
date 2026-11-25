# PROG8245 — Inverted Matrix Workshop

In this workshop, we use Python to build a simple search tool for a collection of blog posts. We clean the text, split it into tokens, and build an inverted index. The index connects each term to the documents where it appears. By storing token positions, we can also check whether words appear together in the right order for a phrase search.

## Team Members

- Arya Patel
- [Team Member 2]
- [Team Member 3]
- [Team Member 4]

## Dataset

We use posts from the [Python Software Foundation News blog](https://pyfound.blogspot.com/). Each post is one document. The notebook downloads posts through the [PSF RSS feed](https://pyfound.blogspot.com/feeds/posts/default?alt=rss), removes HTML tags, and combines each post’s title and body.

Our saved run collected **25 documents** with **2,768 unique words** before stop-word removal and stemming. These counts may change when new posts appear in the live feed.

**Dataset license** — A reuse license for the blog posts has not been verified.

## Workshop Steps

1. **Document collection** — Load the cleaned posts and check the document and word counts.
2. **Tokenization** — Split the text into lowercase tokens and use punctuation as separators.
3. **Normalization** — Remove common stop words and use stemming to group related word forms.
4. **Inverted index and phrase search** — Connect terms to document IDs and use token positions to check phrase matches.

## Run the Notebook in VS Code

1. Open the repository folder in VS Code.
2. In the terminal, create a virtual environment and install the packages. These commands are for Windows PowerShell.

   ```powershell
   py -m venv .venv
   .\.venv\Scripts\python.exe -m pip install ipykernel requests feedparser beautifulsoup4 nltk pandas
   ```

3. Open [IR_InvertedMatrix_Workshop.ipynb](IR_InvertedMatrix_Workshop.ipynb) and select the `.venv` Python kernel.
4. Run the workshop cells in order. The RSS feed and the NLTK stop-word download require internet access.
5. Use the final course submission cell when your team is ready to submit.