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

ONLY content that appears in the PR diff (added or modified lines) must
be evaluated. The reviewer MUST NOT flag errors found in lines that were
not modified by this PR, even if those errors exist in the surrounding
context.

## The reviewer MUST detect and report:
- Grammatical errors
- Typographical errors
- Incorrect word usage
- Broken or unclear sentence structure
- Semantic ambiguity that reduces clarity
- Incomplete or malformed sentences

## Out of Scope
- Errors in lines not touched by the PR diff
- Minor stylistic preferences
- Subjective rewording suggestions
- Improvements that do not affect clarity or correctness

## Clarification
If the Pull Request improves grammar or clarity compared to the forum
proposal, this MUST be treated as a valid improvement and MUST NOT be
flagged as inconsistency.

------------------------------------------------------------------------
# 2. Forum Consistency Validation (Semantic Source of Truth)

The forum proposal defines the intended meaning and required technical
changes. The reviewer MUST validate that the Pull Request correctly
implements the semantic intent of the proposal.

## The forum is the source of truth for:
- The logical meaning and intent of the change
- Required actions and their scope
- Technical values such as parameters, identifiers, addresses, and
  numerical quantities interpreted semantically

## The forum is NOT the source of truth for:
- Grammar, spelling, or typographical style
- The specific format or notation in which values are expressed
- Which parameters or fields are structurally required by the document
- Formatting, units, or conventions used to represent values

## Validation Approach
The reviewer MUST evaluate whether the PR faithfully implements the
semantic intent of the forum proposal. When comparing values or
parameters, the reviewer MUST assess meaning and intent, not literal
phrasing or format.

If a parameter or value mentioned in the forum is absent or expressed
differently in the PR, the reviewer MUST first determine whether the
difference is semantic (a real deviation from intent) or representational
(a formatting or structural convention). Only semantic deviations MUST
be flagged.

If a parameter mentioned in the forum does not appear in the PR because
the document structure does not require it, this MUST NOT be flagged as
a missing requirement. The structural expectations of the document are
governed by Rule 3, not by the forum.

## The reviewer MUST detect and report:
- Changes that contradict the intended semantic meaning of the proposal
- Missing content that is semantically required by the proposal and
  structurally expected by the document
- Values or parameters whose meaning deviates from the forum intent

## Case Handling
Differences in capitalization or casing MUST NOT be treated as
inconsistencies unless casing has explicit technical meaning for that
specific type of value.

------------------------------------------------------------------------
# 3. Structural and Internal Consistency Validation

The reviewer MUST verify that newly added or modified content maintains
structural and formatting consistency with the existing document.

## Peer Reference Methodology
To validate structure and formatting, the reviewer MUST identify peer
elements: existing elements of the same structural type within the same
document that are NOT being modified by this PR. These peer elements
serve as the structural reference baseline.

The reviewer MUST derive expectations exclusively from these peers,
including but not limited to: which fields are present, how values are
expressed, what conventions are used, and how content is organized.

If multiple peers exist, the reviewer MUST look for consensus across
them. A single outlier peer MUST NOT override the pattern established
by the majority.

## The reviewer MUST evaluate:
- Whether the structure and fields of the new or modified content match
  those of peer elements
- Whether values and parameters follow the same representational
  conventions used by peers
- Whether headings, sections, lists, and indentation follow the same
  pattern as peers
- Whether any convention used in the PR deviates from what peers
  establish as the norm

## Scope Limitation
This rule concerns internal structural coherence only.
It MUST NOT re-evaluate grammar (Rule 1) or semantic correctness
relative to the forum (Rule 2). A finding under this rule must be
exclusively structural.

## False Positive Prevention
If the format or convention used in the PR matches the pattern
established by the majority of peer elements of the same type, the
reviewer MUST NOT flag it as a structural inconsistency, even if it
differs from how the forum expressed the same information.
