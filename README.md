# internal-kb-assistant

A small **Streamlit** demo for an internal knowledge assistant: upload documents, build an index, ask questions, and get answers with **inline citations** and visible source snippets.

Bundled sample docs under `demo_docs/` are **synthetic** demo text. See `demo_docs/README.md` and `demo_docs/manifest.json` for categories, provenance, and example questions.

## Setup

```bash
brew install uv   # optional but recommended
uv sync --group dev

cp .env.example .env
# add OPENAI_API_KEY (and optional ANTHROPIC_API_KEY)
```

Without `uv`:

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## Run

```bash
uv run streamlit run streamlit_app.py
```

## Tests

```bash
uv run pytest
```

## Demo flow

1. Open the app in the browser.
2. Choose **Sample docs** in the sidebar.
3. Click **Build index**.
4. Use an example question from the expander or type your own.
5. Click **Ask** and show citations + source cards.

**Talk track:** *I built a small internal knowledge assistant that retrieves relevant documents and answers with citations, which is a safer pattern for enterprise AI adoption.*
