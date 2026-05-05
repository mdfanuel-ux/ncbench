# NCBench — Agricultural Instruction Tuning Benchmark

An interactive web page for the NCBench project: a domain-specific instruction tuning dataset for agricultural LLMs, targeting soybean and sweet potato farming in the United States.

## Live Demo

Visit the live page: [https://YOUR_USERNAME.github.io/ncbench/](https://YOUR_USERNAME.github.io/ncbench/)

## What's Here

| File | Description |
|------|-------------|
| `index.html` | Main page (same as `one.html`) |
| `one.html` | Working copy of the page |
| `topic_index.json` | Pre-built index of top-20 QA pairs per topic (305 KB) |

## Data Files (not deployed — too large for GitHub Pages)

These files live in the parent directory and are used by the build script:

- `Rice Closed Book (42,951-Q&A-pairs).json` — Rice QA dataset
- `Corn Closed Book (25,259 Q&A pairs).json` — Corn QA dataset
- `Rice Open Book (2,430 Q&A pairs).json` — Rice open-book QA
- `Corn Open Book (3,202 Q&A pairs).json` — Corn open-book QA

## Scripts

- `build_index.py` — Builds `topic_index.json` from the full datasets using weighted lexical scoring
- `generate_qa.py` — NCBench QA generation pipeline (requires LLM API key + source PDFs)

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `ncbench`)
2. Push the contents of the `NC/` folder to the `main` branch
3. Go to Settings → Pages → Source: "Deploy from a branch" → Branch: `main` → Folder: `/ (root)`
4. Your site will be live at `https://YOUR_USERNAME.github.io/ncbench/`

## Authors

- Dr. Shaohu Zhang — North Carolina A&T State University
- Dr. Mesafint Fanuel — North Carolina A&T State University
- Dr. Crystal Cook Marshall — North Carolina A&T State University
- Dr. Mahmoud Nabile Mahmoud — University of Alabama

## Built On

The [CROP dataset](https://github.com/) methodology by Zhang et al. (2024), Shanghai AI Laboratory.
