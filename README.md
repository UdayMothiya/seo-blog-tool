# SEO Blog Writer

Run this local browser app with Python 3.10 or newer. It uses the Gemini API and does not require Ollama.

## Start on your Mac

Unzip the download. Open Terminal in the extracted `seo-blog-tool` folder and run:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m streamlit run app.py --server.address 127.0.0.1
```

Create an API key in [Google AI Studio](https://aistudio.google.com/apikey) and enter it in the app sidebar. You can also set the `GEMINI_API_KEY` environment variable before starting the app. The default is Gemini 3.8 Flash, which Google lists with free standard input and output. Free access and quotas depend on your project. Use a project without billing enabled if you want to avoid charges. If the default model is unavailable, enter a model that your AI Studio project lists as available on its free tier. [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)

## Write and revise a blog

1. Upload a UTF-8 TXT or Markdown file, a PDF up to 10 MB, or a Word DOCX. For Apple Pages sources, export to PDF or Word first.
2. Enter the target audience, purpose and word count. Add a keyword or further instructions if you have them.
3. Select **Generate review draft**. The app makes four Gemini requests for source analysis, drafting, editorial review, and rewriting.
4. Download the DOCX for feedback. Paste the requested edits into the app and select **Apply feedback**. Each successful revision uses one request. You can revise up to three times per draft.
5. Download the current version as a plain-text TXT file whenever you are satisfied.

The SEO review covers on-page content such as search intent, headings, keyword use, the SEO title and meta description. It uses no live search or keyword-volume data. Check the draft's claims and word count before publishing. The draft and revision history are held in the current browser session. Download your work before closing or reloading the tab. Source content and revision feedback are sent to Google Gemini.
