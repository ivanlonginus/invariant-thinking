# Limitations and Failure Modes

## 1. False invariance

A practitioner may incorrectly classify a changing property as invariant because the transformation was underspecified.

**Mitigation:** require transformation, boundary, and break condition.

## 2. Over-abstraction

A model may become so general that it explains everything and predicts nothing.

**Mitigation:** require task-relevant properties and concrete analogy breaks.

## 3. Expertise bias

Experts can map new systems too quickly onto familiar categories and miss genuinely new mechanisms.

**Mitigation:** make the Test stage adversarial and preserve unknowns.

## 4. Vocabulary substitution

Replacing vendor terminology with generic terminology can create the illusion of understanding.

**Mitigation:** Decompose behavior and mechanisms, not words alone.

## 5. Scale discontinuities

A mechanism that behaves one way at small scale may require qualitatively different architecture at large scale.

**Mitigation:** include scale in the invariant boundary.

## 6. Context dependence

A useful invariant in one domain may be irrelevant in another.

**Mitigation:** avoid universal wording when the actual claim is local.

## 7. Tacit operational knowledge

Structural understanding does not automatically provide proficiency with tooling, debugging, deployment, ergonomics, or ecosystem conventions.

**Mitigation:** treat operational learning as part of the Learning Delta when it affects real work.

## 8. Unvalidated learning-efficiency claim

ITF proposes that explicit structural transfer can reduce unnecessary relearning, but version 0.1 does not provide controlled evidence establishing the size or reliability of that effect.

**Mitigation:** keep empirical claims in `RESEARCH.md` as hypotheses until tested.

## 9. Invariance-information trade-off

Seeking invariance can discard information that matters for a downstream task. Related work in invariant representation learning demonstrates that invariance and predictive information can be competing objectives.

**Mitigation:** use the Lossy Abstraction Principle and define the reasoning task before deciding what variation is irrelevant.
