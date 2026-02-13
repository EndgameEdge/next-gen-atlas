# Atlas Proposal Review Rules

This document defines the complete and exclusive validation scope for
automated PR review.

The reviewer MUST evaluate Pull Request changes strictly according to
the rules defined in this file.

------------------------------------------------------------------------

# 1. Language Quality Validation

The reviewer must evaluate the language quality of the changes
introduced in the Pull Request.

## Scope

Only the content introduced or modified in the PR must be evaluated.

## The reviewer MUST detect and report:

-   Grammatical errors
-   Typographical errors
-   Incorrect word usage
-   Broken or unclear sentence structure
-   Semantic ambiguity that reduces clarity
-   Incomplete or malformed sentences

## Out of Scope

-   Minor stylistic preferences
-   Subjective rewording suggestions
-   Improvements that do not affect clarity or correctness

## Clarification

If the Pull Request improves grammar or clarity compared to the forum
proposal, this MUST be treated as a valid improvement and MUST NOT be
flagged as inconsistency.

------------------------------------------------------------------------

# 2. Forum Consistency Validation (Semantic Source of Truth)

The forum proposal defines the intended meaning and required technical
changes.

The reviewer MUST validate that the Pull Request correctly implements
the semantic intent of the proposal.

## The forum is the source of truth for:

-   Parameters
-   Numerical values
-   Percentages
-   Blockchain addresses
-   Identifiers
-   Logical meaning of the change
-   Required actions

## The forum is NOT the source of truth for:

-   Grammar
-   Spelling
-   Typographical issues
-   Stylistic formatting differences

## The reviewer MUST detect and report:

-   Missing required parameters
-   Incorrect values
-   Incorrect percentages
-   Incorrect or mismatched blockchain addresses
-   Incomplete implementation of the described change
-   Changes that contradict the intended semantic meaning

## Case Handling

Differences in capitalization or casing must NOT be treated as
inconsistencies unless casing has explicit technical meaning.

Parameter values should be treated as case-insensitive by default unless
explicitly defined otherwise.

The reviewer must compare semantic intent, not literal phrasing, except
when validating technical values.

------------------------------------------------------------------------

# 3. Structural and Internal Consistency Validation

The reviewer MUST verify that newly added or modified content maintains
structural and formatting consistency with the existing document.

This rule ensures internal coherence between the new content and the
document's established structure.

## The reviewer MUST evaluate:

-   Consistency of numeric representation
-   Consistency of parameter formatting
-   Consistency of headings and section structure
-   Consistency of list formatting and indentation
-   Consistency of units, symbols, and value precision
-   Alignment with existing document conventions

The reviewer must detect inconsistencies that break the established
structural pattern of the document.

This rule concerns internal structural coherence only.
It does NOT evaluate grammar (Rule 1) or semantic correctness relative
to the forum (Rule 2).
