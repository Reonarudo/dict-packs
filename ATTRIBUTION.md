# Attribution & source credits

The Dict dictionary data is compiled from the open-licensed sources below and is
itself released under **CC-BY-SA 4.0** (see [`LICENSE-DATA`](LICENSE-DATA)). When you
redistribute the data (e.g. `dict.pack`), keep this attribution with it.

**Modifications made.** The source data was downloaded, parsed/extracted, normalized
(accent-folded merge keys, part-of-speech mapping), merged and de-duplicated across
sources, split into same-spelling homographs, and — for entries lacking a native
Italian definition or etymology — **machine-translated into Italian** (recorded as
`traduzione automatica`). Verb conjugation tables are derived from the source
inflection data plus generated compound tenses. The result is a transformation of
the originals, not a verbatim copy.

## Sources included in the build

| Source | Contributes | License | Link |
|---|---|---|---|
| **Wiktionary** — Italian & English editions, via **kaikki.org** (wiktextract, © Tatu Ylönen) | definitions, IPA, part of speech, inflected forms, verb conjugation, etymology, examples, synonyms/antonyms | **CC-BY-SA 4.0** / GFDL | <https://www.wiktionary.org/> · <https://kaikki.org/> |
| **Tatoeba** | example sentences | **CC-BY 2.0 FR** | <https://tatoeba.org/> |
| **Open Multilingual Wordnet** — ItalWordNet | synonyms and some Italian definitions | **CC-BY 3.0** | <https://omwn.org/> |
| **itWaC frequency lists** — `franfranz/Word_Frequency_Lists_ITA` (itWaC/WaCky-derived) | corpus frequency ranks | **MIT** | <https://github.com/franfranz/Word_Frequency_Lists_ITA> |
| **Machine translations** (`translations.jsonl`, `etymologies.jsonl`) | residual Italian definitions/etymologies, translated from the English Wiktionary entries | **CC-BY-SA 4.0** (derivative of en.wiktionary) | — |

Credit to **Wiktionary and its contributors**; the original content is available
under CC-BY-SA at the respective `wiktionary.org` sites. Please also cite the
Open Multilingual Wordnet / ItalWordNet publications when using WordNet-derived data.

## License notices

### itWaC frequency lists

The lists in `franfranz/Word_Frequency_Lists_ITA` are published under the MIT
License (the repository's `LICENSE`, unchanged since its initial commit
`2c5bfe3`). The lists count word forms in the itWaC corpus (Baroni, Bernardini,
Ferraresi & Zanchetta, 2009); the build uses only the lemma ranks derived from
them. The notice, as that license requires:

```
MIT License

Copyright (c) 2020 franfranz

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Not included

- **Morph-it!** (Zanchetta & Baroni, Università di Bologna) — CC-BY-SA / LGPL. Its host
  currently returns HTTP 402, so it is **skipped** in the default build and the
  distributed data contains none of it. If you enable it (by placing `morph-it_048.txt`
  in the cache), credit it and observe its license.

*This file documents data-source attribution. Third-party software libraries used by
the code are listed in [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md).*
