# HERMES_TASK.md: My Rabbit Hole daily edition

## What this task does

Write ONE file: `data/latest.json`, in this repo folder. The website (`index.html`) reads that file and displays it. Do not edit `index.html` or any other file.

Only commit or push to GitHub if the person's message explicitly asks you to. Otherwise, write the file and stop.

## Keep it simple

- Use your web search tool to find stories. Do NOT use RSS feeds. Do NOT write shell loops, scripts, or download files with curl or wget.
- Use as few steps as possible. Do about 6 searches in total (one per topic below), then write the file once.
- Do not test, check, or "verify" sources one by one. If a search returns nothing useful, move on.
- Write `data/latest.json` with your file-writing tool in a single step.

## Finding stories

Write **3 stories** unless told otherwise. Search for today's most important stories on these topics and choose the strongest three overall. Mix the topics, and never pick two stories about the same event.

Topics and preferred outlets (search each one, for example "nytimes technology today" or "economist science and technology"):
- Technology: The New York Times (Technology section), The Economist (Science & technology)
- Design: The New York Times (Art & Design)
- Environment and climate: The New York Times (Climate)
- Economy and world affairs: The Economist (Leaders, Finance & economics)
- French-language news: France 24 (france24.com/fr) and RFI (rfi.fr/fr)

Use at most 1 or 2 stories from any one outlet. Include at least one story from France 24 or RFI if you can find one.

## How to write each story

- The New York Times and The Economist articles are paywalled. Do not try to get around a paywall and do not copy article text. Use only the headline, snippet and any free-to-read text that you can see.
- Write the English `body` yourself, in your own words. Do not invent facts, quotes or numbers. If you only have a headline and a snippet, write a shorter body (2 short paragraphs) rather than padding.
- France 24 and RFI are free to read. Read the article and write a longer original account in English (3 to 5 short paragraphs).
- For a story from a French source, the English `body` is your own English version, and `french.body` is your own French version. Do not copy the French article.
- Always fill in `url` with the link to the original article, so the reader can open it. Only use a link you actually saw in your search results. Never make up a link.
- `body` is a list of short paragraphs, each 2 to 4 sentences, in plain language.
- `dek` is one sentence saying why the story matters.
- `section` is a one-word label, for example Technology, Design, Environment, Economy, World.
- Leave `image`, `image_alt` and `image_credit` as empty strings. The page shows a pixel placeholder. Never invent an image URL.

## French version (collapsible under each story)

- `french.body` is the FULL-LENGTH French version. It must cover everything in the English `body`, paragraph for paragraph, at roughly the same length. It is not a short brief.
- Write it for a learner at level A2 to B1: short clear sentences, common vocabulary. Set `"level": "A2-B1"`.
- `french.headline` is the story headline in French.
- `french.vocab` is 4 to 6 useful words or phrases from the French text, each with its English meaning.
- Use correct accents and apostrophes (é, è, ç, œ, l', d').

## Lesson of the day

Include one short French lesson (`lesson`) at level A2 to B1 on a single point of grammar or usage. Try to reuse a structure that appears in today's French texts. The explanation is in English.

## JSON format

Write valid JSON only (double quotes, no comments, no trailing commas). Do NOT include a `"sample"` field. Use this exact structure:

```json
{
  "site_title": "My Rabbit Hole",
  "date": "YYYY-MM-DD",
  "generated_at": "YYYY-MM-DDTHH:MM:SS+05:30",
  "lesson": {
    "title": "French title of the lesson",
    "explanation": ["One or two short paragraphs in English."],
    "examples": [
      { "fr": "Une phrase en français.", "en": "The same sentence in English." }
    ],
    "exercise": {
      "question": "Complète : ... ___ ...",
      "answer": "the answer"
    }
  },
  "stories": [
    {
      "section": "Technology",
      "headline": "English headline",
      "dek": "One sentence saying why it matters.",
      "source": "The New York Times",
      "url": "https://link-to-the-original-article",
      "image": "",
      "image_alt": "",
      "image_credit": "",
      "body": [
        "First paragraph.",
        "Second paragraph."
      ],
      "french": {
        "headline": "Titre en français",
        "level": "A2-B1",
        "body": [
          "Premier paragraphe.",
          "Deuxième paragraphe."
        ],
        "vocab": [
          { "fr": "un mot", "en": "a word" }
        ]
      }
    }
  ]
}
```

Notes:
- `date` is today's date in India (IST). `generated_at` is the current time in IST (+05:30).
- `stories[0]` is the lead story and is shown biggest, so put the strongest story first.
- Every story must have `headline`, `body`, `url` and a `french` block.

## When you finish

Tell the person in one or two lines: how many stories you wrote and which outlets they came from. Do not list every step you took.
