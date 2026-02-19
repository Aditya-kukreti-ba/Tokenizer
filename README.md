# NLTK Tokenizer — Interactive NLP Lab

> **Live Demo → [https://tokenizer-beta.vercel.app/](https://tokenizer-beta.vercel.app/)**

An interactive, browser-based playground for exploring **NLTK tokenization methods**. Paste any text and watch it get tokenized in real time — no Python installation required. Every result panel includes the exact Python/NLTK code to reproduce the output.

---

## Features

| Feature | Description |
|---|---|
| **Word Tokenize** | Mirrors `nltk.word_tokenize()` with color-coded token types |
| **Sentence Tokenize** | Punkt-style sentence boundary detection via `sent_tokenize()` |
| **RegexpTokenizer** | Live regex pattern matching with built-in presets |
| **Compare All** | Side-by-side comparison of all tokenization methods |
| **Learn** | Theory cards + a full Python/NLTK cheatsheet |

---

## Demo

[![Live on Vercel](https://img.shields.io/badge/Live%20Demo-tokenizer--beta.vercel.app-6ee7f7?style=for-the-badge&logo=vercel&logoColor=black)](https://tokenizer-beta.vercel.app/)

Open the app in your browser and try any of the five tabs:

1. **Word Tokenize** — type text, toggle stopword/punctuation filters, and inspect per-token classifications (word, punctuation, number, stopword)
2. **Sentence Tokenize** — paste a paragraph and see sentence boundaries detected with stats (count, average words/sentence, longest sentence)
3. **RegexpTokenizer** — choose a preset pattern (`\w+`, hashtags, numbers, capitalized words…) or write your own regex
4. **Compare All** — run all methods on the same input simultaneously
5. **Learn** — read concept cards and copy the ready-to-run NLTK cheatsheet

---

## Python Equivalents

Every result in the app corresponds directly to NLTK Python code. Here's a quick reference:

```python
import nltk
from nltk.tokenize import word_tokenize, sent_tokenize, RegexpTokenizer
from nltk.corpus import stopwords

# One-time setup
nltk.download('punkt')
nltk.download('punkt_tab')
nltk.download('stopwords')

text = "Dr. Smith's lab isn't open today. Let's try again tomorrow!"

# Word tokenization
tokens = word_tokenize(text)
# → ['Dr.', 'Smith', "'s", 'lab', "isn't", 'open', 'today', '.', ...]

# Sentence tokenization
sentences = sent_tokenize(text)
# → ["Dr. Smith's lab isn't open today.", "Let's try again tomorrow!"]

# Regex tokenization — words only
tokenizer = RegexpTokenizer(r'\w+')
tokens_re = tokenizer.tokenize(text)
# → ['Dr', 'Smith', 's', 'lab', 'isn', 't', 'open', 'today', ...]

# Remove stopwords
stop_words = set(stopwords.words('english'))
filtered = [w for w in tokens if w.lower() not in stop_words]

# Token frequency
from nltk import FreqDist
fdist = FreqDist(tokens)
fdist.most_common(5)
```

---

## Token Color Legend

| Color | Type | Example |
|---|---|---|
| 🔵 Cyan | Regular word | `hello`, `NLTK`, `running` |
| 🟠 Orange | Punctuation | `.` `,` `!` `?` `"` |
| 🟣 Purple | Number | `42`, `3.14`, `2023` |
| 🟢 Green | Stopword | `the`, `is`, `a`, `it` |

---

## NLTK Tokenizers Covered

### `word_tokenize()`
Uses the **Punkt tokenizer** trained on English. Handles contractions (`don't` → `do` + `n't`), abbreviations (`Dr.`, `U.S.`), and punctuation intelligently. This is the most commonly used tokenizer in NLTK.

### `sent_tokenize()`
Uses NLTK's **Punkt Sentence Tokenizer**. Handles tricky cases like `"Dr. Smith"` vs. an end-of-sentence period. Language models are available for 17+ languages.

### `RegexpTokenizer`
Allows fully custom tokenization via regular expressions. Can match tokens or gaps. Great for domain-specific text like social media, medical notes, or source code.

**Built-in presets in the app:**

| Pattern | Matches |
|---|---|
| `\w+` | All word characters |
| `[A-Z][a-z]+` | Capitalized words |
| `\d+` | Numbers only |
| `[a-zA-Z0-9]+` | Alphanumeric tokens |
| `\w+(?:[-']\w+)*` | Words with hyphens/apostrophes |
| `[#@]\w+` | Hashtags & mentions |

---

## Tech Stack

- **Frontend:** Vanilla HTML, CSS, JavaScript — zero dependencies, zero build step
- **Fonts:** [Syne](https://fonts.google.com/specimen/Syne) + [Space Mono](https://fonts.google.com/specimen/Space+Mono) via Google Fonts
- **Hosting:** [Vercel](https://vercel.com)
- **NLP Reference:** [NLTK 3.8](https://www.nltk.org/) (Python)

---

## Local Development

Since the app is a single HTML file with no build process, just open it:

```bash
# Clone the repo
git clone https://github.com/your-username/nltk-tokenizer.git
cd nltk-tokenizer

# Open directly in browser
open nltk_tokenizer.html

# Or serve locally
npx serve .
# → http://localhost:3000
```

---

## Deploying to Vercel

The live site runs at **[https://tokenizer-beta.vercel.app/](https://tokenizer-beta.vercel.app/)**.

To deploy your own instance:

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Or connect your GitHub repo at vercel.com for automatic deployments
```

---

## Resources

- [NLTK Official Documentation](https://www.nltk.org/)
- [NLTK Book — Chapter 3: Processing Raw Text](https://www.nltk.org/book/ch03.html)
- [NLTK Tokenize API Reference](https://www.nltk.org/api/nltk.tokenize.html)
- [RegexpTokenizer Docs](https://www.nltk.org/api/nltk.tokenize.regexp.html)

---

## License

MIT — free to use, modify, and distribute.
