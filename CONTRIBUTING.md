# Contributing

Contributions are welcome, especially those that make the framework harder to misuse.

## Good contributions

- worked Invariant Maps;
- counterexamples;
- failed mappings;
- terminology corrections;
- prior-art references;
- empirical study designs or results;
- domain applications outside software;
- arguments that narrow or falsify a framework claim.

## Requirements for an Invariant Map

A submitted map should include:

1. a clearly bounded subject;
2. the transformation being analyzed;
3. the invariant boundary;
4. candidate invariants;
5. changed properties;
6. at least one analogy break or boundary condition;
7. a Learning Delta;
8. unknowns or low-confidence claims;
9. sources where factual claims depend on external evidence.

"X is basically Y" is not sufficient.

## Framework changes

Changes to normative concepts should use an RFC under `rfcs/`.

An RFC should explain:

- current problem;
- proposed change;
- alternatives;
- compatibility impact;
- counterexamples;
- prior art.

## Translations

English is the canonical language of the Invariant Thinking Framework.

Translations exist to improve accessibility and MUST preserve:

- the framework version being translated;
- section numbering where the canonical document uses it;
- defined terminology and conceptual relationships;
- normative meaning;
- examples where practical; and
- links back to the canonical source.

Translations MUST NOT:

- introduce new normative requirements;
- silently remove qualifications, boundaries, or failure conditions;
- make stronger scientific or novelty claims than the canonical source; or
- alter project authorship or attribution.

If a translation exposes an ambiguity or error in the canonical framework, the canonical English document should be corrected first and the translation updated afterward.

A translated normative document should clearly identify itself as a translation and state that the English source takes precedence in case of semantic disagreement.

## Authorship and attribution

Project authorship and citation metadata are governed by `CITATION.cff`. Contributions do not imply co-authorship of the framework unless the project owner explicitly changes that metadata.

## Style

- Prefer precise claims over slogans.
- Separate observation, inference, and hypothesis.
- Avoid novelty claims unless supported by a prior-art search.
- Prefer examples that expose limitations rather than examples designed only to make ITF look correct.

## Versioning

Normative changes are recorded in `CHANGELOG.md`. Pre-1.0 versions may contain breaking conceptual changes.
