# Optional COMP4122 graphics examples

Read only for relevant graphics/matrix teaching or when matching the user's COMP4122 note style. These examples illustrate the general workflow, not rules to impose on every subject.

## Existing course and style references

Resolve the COMP4122 Course and example notes from [workspace configuration](workspace.md). Look up the actual relation for other courses.

Read only relevant excerpts when useful; do not fetch both entire notes for each explanation.

## Explain the step that caused confusion

- With column vectors, show the full equation v′ = T R S v to distinguish matrix writing order from application order (scale, rotate, translate).
- Explain an inverse as undoing a transformation before presenting an inverse formula. For rotation, a concrete axis matrix may make the relationship clearer than an unexplained identity.
- Inverse = transpose requires an orthogonal matrix; do not apply it to arbitrary scaling/shearing transforms.
- Verify handedness, horizontal versus vertical FOV definitions, and clip/NDC ranges against the lecture/API convention. Do not silently switch conventions or treat old assistant explanations as mathematical evidence.

## Keep concepts and derivations organized

A rendering chapter can introduce frustum geometry, compare orthographic/perspective concepts, and then present projection matrices and parameter derivations in separate subsections. Merging repeated slide titles is useful, but must not delete generalized/symmetric matrix distinctions, FOV derivations, or clipping conditions that the source teaches.

When the user asks to save a clearer explanation, preserve the key clarification in a concise standalone paragraph/equation rather than copying all exploratory dialogue.
