🧠 NLTK Tokenizer — Interactive NLP Lab

🌐 Live Demo:
👉 https://tokenizer-beta.vercel.app/

An interactive, browser-based Natural Language Processing (NLP) playground that demonstrates how NLTK-style tokenization works — including word tokenization, sentence tokenization, and custom regular expression tokenization.

Built with pure HTML, CSS, and JavaScript.
No backend. No server. All processing happens locally in your browser.

📚 Table of Contents

Live Demo

Introduction

Features

Installation

Usage

Tokenization Methods Implemented

Dependencies

Configuration

Examples

Project Structure

Troubleshooting

Future Improvements

Contributors

License

🚀 Live Demo

The project is deployed and publicly accessible here:

🔗 https://tokenizer-beta.vercel.app/

No installation required — open the link and start experimenting instantly.

📖 Introduction

NLTK Tokenizer — Interactive NLP Lab is a visually rich educational tool designed to help users understand how tokenization works in Natural Language Processing.

The application mimics core functionality from Python’s NLTK library, including:

word_tokenize()

sent_tokenize()

RegexpTokenizer

Stopword filtering

Token statistics

Method comparison

It also provides Python code snippets showing how to replicate each result using actual NLTK.

✨ Features
🔤 Word Tokenization

Approximate NLTK word_tokenize() behavior

Handles:

Contractions (don't → do + n't)

Abbreviations (Dr.)

Punctuation

Numbers

Optional filters:

Hide stopwords

Hide punctuation

Lowercase normalization

Token statistics:

Total tokens

Unique tokens

Word tokens

Punctuation tokens

📄 Sentence Tokenization

Punkt-style sentence segmentation

Handles abbreviations properly (Dr. Smith)

Displays:

Sentence count

Average words per sentence

Longest sentence length

🔍 RegexpTokenizer

Fully customizable regex-based tokenization

Preset patterns:

\w+ — words only

\d+ — numbers

Capitalized words

Alphanumeric tokens

Hashtags & mentions

Hyphenated words

Custom regex support

⚖ Compare All Methods

Side-by-side comparison of:

word_tokenize()

sent_tokenize()

Multiple RegexpTokenizer patterns

🚀 Installation

No installation required for use.

To run locally:

Download the repository.

Rename nltk_tokenizer.html → index.html

Open it in your browser.

Optional local server:

python -m http.server 8000


Then open:

http://localhost:8000

🧪 Usage

Visit the live site:
👉 https://tokenizer-beta.vercel.app/

OR

Open the HTML file locally.

Enter text.

Click Tokenize.

Toggle filters or compare methods.

Expand “View Python Code” to see equivalent NLTK implementation.

All processing is done client-side in JavaScript.

📦 Dependencies

Frontend:

HTML5

CSS3

Vanilla JavaScript

Conceptual (Referenced for learning):

NLTK 3.8

Punkt tokenizer

Stopwords corpus

⚠ The deployed version does NOT require Python or NLTK.

📁 Project Structure
.
├── index.html
└── README.md


Single-file application containing:

HTML

CSS

JavaScript

Embedded documentation

🛠 Troubleshooting

Regex shows error

Ensure valid JavaScript regex syntax.

Tokens don’t perfectly match Python NLTK

This is a JavaScript approximation of Treebank & Punkt behavior.

Large text slows rendering

Reduce input size.

🔮 Future Improvements

Real NLTK backend API mode

POS tagging visualization

Lemmatization demo

Token frequency charts

Export tokens as JSON/CSV

Light theme option

👤 Contributors

Your Name — Developer

📄 License

MIT License

❤️ Built for Learning NLP

Explore tokenization visually, experiment with regex patterns, and understand how NLTK processes text — directly in your browser.
