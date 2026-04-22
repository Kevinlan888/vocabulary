# Vocabulary Cards

A static website for learning English vocabulary with interactive flip cards.

## Features

- **Flip Cards** — Click to flip between word and definition
- **Detail Modal** — "More details" button shows full info (verb forms, collocations, synonyms, antonyms, word family)
- **CEFR Filter** — Filter words by difficulty level (A1–C2)
- **Search** — Real-time word search
- **Lazy Loading** — Detail data loaded on demand, lightweight index for fast initial load

## Data Structure

```
words/
├── index.json          ← Lightweight index for listing/filtering
├── breed.json          ← Full detail per word
├── campsite.json
└── ...
```

Each word file follows this schema:

```json
{
  "word": "flinch",
  "pronunciation": "/flɪntʃ/",
  "cefrLevel": "C1",
  "entries": [
    {
      "partOfSpeech": "verb",
      "transitivity": "intransitive",
      "verbForms": {
        "base": "flinch",
        "past": "flinched",
        "pastParticiple": "flinched",
        "presentParticiple": "flinching",
        "thirdPersonSingular": "flinches"
      },
      "definition": "...",
      "exampleSentence": "...",
      "collocations": ["flinch at", "flinch away", "barely flinch"],
      "synonyms": ["wince", "recoil", "shrink"],
      "antonyms": ["confront", "face"]
    }
  ],
  "wordFamily": ["flinchingly"]
}
```

## Local Development

```bash
# Python
python -m http.server 3000

# Node.js
npx serve -l 3000
```

Then open http://localhost:3000

## Deploy

### Vercel

```bash
npm i -g vercel
vercel
```

### GitHub Pages

Push to GitHub → Settings → Pages → Source: `main` branch

### Netlify

Drag the project folder to [app.netlify.com](https://app.netlify.com)
