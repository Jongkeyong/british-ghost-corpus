# British Ghost Corpus, 1764–1913

**Version 0.3 · 318 active texts · Research corpus · 2026**

This repository documents the construction, curation, and methodological use of the **British Ghost Corpus**, developed by Jong-Keyong Kim for the dissertation *Gothic Ontography: Changing Materialism in British Ghost Story, 1764–1913*.

The corpus is not presented as a neutral or exhaustive archive of British ghost fiction. It is a researcher-constructed collection produced through successive acts of retrieval, screening, repair, expansion, exclusion, and deduplication. The repository makes those decisions inspectable and preserves the distinction between a literary work, a digital textual witness, a bibliographic record, and a computational representation.

## Current release

- **Corpus version:** 0.3
- **Active textual units:** 318
- **Nominal historical range:** 1764–1913
- **Identifier range:** BGH001–BGH320
- **Excluded identifiers:** BGH018 and BGH213
- **Primary file format:** UTF-8 plain text
- **Repository status:** private, committee-facing research release

The uploaded corpus package has been checked against the identifier sequence. It contains 318 active text files and no active files for the two excluded identifiers.

## Research purpose

The corpus supports Chapter 4 of the dissertation and its account of **computational ontography**: a method for examining how ghosts become perceptible and causally effective through relations among spectral entities, perceivers, objects, documents, buildings, atmospheres, economic instruments, and technologies.

The project does not equate statistical outlierness with literary significance. Computational measures rank texts for further inspection; close reading determines whether a deviation is historically, formally, ontologically, or methodologically consequential.

## Corpus genealogy

The active corpus emerged through several documented stages:

1. a 175-text auditable discovery corpus;
2. a screened expansion to 237 texts;
3. a researcher-directed gender-recovery pass to 285 texts;
4. a diversity and transmission-route expansion to 317 texts;
5. a canonical and boundary expansion to 320 records; and
6. duplicate and alternate-translation review, yielding 318 active texts.

The recovery passes corrected visible imbalances in the available collection but did not make the corpus demographically or bibliographically complete.

## Operational scope

Eligible units may include short fiction, novels, novellas, poetry, drama, essays, testimony-like anecdotes, folklore records, English translations, hoaxes, ambiguous apparitions, animal ghosts, and other substantial postmortem presences. Chapters mechanically extracted from a unitary novel are not treated as independent works. Vampires, demons, doubles, fairies, werewolves, and metaphor-only specters are ordinarily excluded when they are the sole supernatural agent.

See [`CORPUS_SCOPE.md`](CORPUS_SCOPE.md) and [`METHODOLOGY.md`](METHODOLOGY.md) for the fuller boundary and construction statements.

## Repository contents

- [`metadata/`](metadata/) — manifest, exclusion, duplicate, and translation records
- [`docs/`](docs/) — methodological and reproducibility documentation
- [`scripts/`](scripts/) — auditing and analysis code as it is deposited
- [`results/`](results/) — derived tables, figures, and interpretive outputs
- [`corpus/`](corpus/) — access and rights guidance for primary-text witnesses
- [`DATA_STATEMENT.md`](DATA_STATEMENT.md) — bias, quality, rights, and responsible-use statement
- [`CITATION.cff`](CITATION.cff) — machine-readable citation metadata
- [`CHANGELOG.md`](CHANGELOG.md) — corpus version history

## Manifest and textual integrity

Each active text is assigned a stable BGH identifier. The working manifest records the preserved filename, normalized creator and title labels where available, word count, byte count, and SHA-256 checksum. Bibliographic dates, source repositories, translation histories, OCR conditions, and redistribution rights remain explicitly marked for review when they have not been independently verified.

A checksum identifies a particular digital witness; it does not certify the accuracy of its transcription, attribution, date, or edition.

## Rights and access

The full primary-text corpus is not yet deposited in this repository. Public-domain status of an original literary work does not automatically establish the redistribution status of a modern edition, translation, transcription, OCR derivative, or repository export. Until source-specific review is complete, the repository prioritizes metadata, provenance, methods, and derived results over unrestricted redistribution.

## Related project: Ghost Story Lens

**Ghost Story Lens** is an explainable, corpus-grounded literary analysis application developed from the dissertation’s genre adjudications and ghost–mediator–seer model. It places submitted texts on a revisable ghost-story spectrum, identifies textual evidence, distinguishes adjacent supernatural entities, and maps pathways of manifestation and perception. The application repository and public URL will be linked here after deployment.

## Citation

Until a DOI-backed release is created, cite the corpus as:

> Kim, Jong-Keyong. *British Ghost Corpus: Deduplicated Translations*. Version 0.3, 318 active texts, 2026, GitHub, github.com/Jongkeyong/british-ghost-corpus.

For individual corpus texts, include the author, title, corpus title, version, and BGH identifier when known.

## Contact and scholarly status

This is a dissertation research repository under active bibliographic and technical review. Questions about inclusion, attribution, provenance, or reuse should be directed to the repository owner. Claims based on the corpus should preserve its version number and acknowledge its documented limitations.
