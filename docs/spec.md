# Audience — General reader — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates
it in CI. The prose headings are hand-owned — everything between `tl:*` markers is
injected from the YAML items, so the published spec can never drift from the graph.

This source is the **audience axis** for one level: a **general** (lay) reader with no
special knowledge of the field. It governs how the writing is *calibrated* to the
reader's expertise — assumed knowledge, terminology, depth, orientation and examples —
not universal readability, spelling, punctuation, register, purpose, medium or brand
voice, each of which is its own throughline source. Audience levels are mutually
exclusive: **expert**, **practitioner** and **general** are sibling sources and a
consumer composes exactly one under the `audience` namespace. Every principle is a
`user_requirement`; every rule is a `system_requirement` that `implements` its
principle. The throughline UIDs are this source's own and immutable — a consumer cites
a rule as `audience:SR-0001`.

It carries
<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles and
<!-- tl:count type == 'system_requirement' -->
10
<!-- tl:end --> rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Text is pitched for a general reader** — `intent`, status `approved`

> A general reader has no special knowledge of the field. They need everything explained in everyday terms, with full orientation to what the subject is and why it matters to them, and only the depth required to understand and act. This axis governs how the writing is calibrated to the reader's expertise — assumed knowledge, terminology, depth and orientation — not universal readability, spelling, register or purpose, each of which is a separate source. Audience levels are mutually exclusive: a consumer composes exactly one of the expert, practitioner or general sibling sources.

**source_ref**: TBS Audience — General reader
<!-- tl:end -->

## 1. Assume no prior knowledge of the field

<!-- tl:item UR-0001 -->
**UR-0001 — Assume no prior knowledge of the field** — `user_requirement`, status `approved`

> Take nothing about the subject for granted; build understanding from the ground up.

*Derives from:* INT-0001

**source_ref**: TBS Audience — General reader — Assumed prior knowledge
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0001' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Explain from first principles, assuming no subject knowledge |
| SR-0002 | system_requirement | approved | Do not rely on the reader knowing field-specific acronyms, processes or roles |
<!-- tl:end -->

## 2. Avoid jargon; explain any unavoidable term in plain words

<!-- tl:item UR-0002 -->
**UR-0002 — Avoid jargon; explain any unavoidable term in plain words** — `user_requirement`, status `approved`

> Keep specialist vocabulary out; where a term cannot be avoided, define it in everyday language.

*Derives from:* INT-0001

**source_ref**: TBS Audience — General reader — Terminology and jargon
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0002' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0003 | system_requirement | approved | Avoid specialist terms; explain any unavoidable one in everyday words |
| SR-0004 | system_requirement | approved | Name things by what they do for the reader, not by their technical label |
<!-- tl:end -->

## 3. Give only the depth the reader needs to act

<!-- tl:item UR-0003 -->
**UR-0003 — Give only the depth the reader needs to act** — `user_requirement`, status `approved`

> Include what a general reader needs to understand and act, and leave out specialist depth.

*Derives from:* INT-0001

**source_ref**: TBS Audience — General reader — Depth and detail
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0003' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0005 | system_requirement | approved | Include only the detail needed to understand and act |
| SR-0006 | system_requirement | approved | Focus on what it means for the reader, not how it works internally |
<!-- tl:end -->

## 4. Give full orientation; start from why it matters to them

<!-- tl:item UR-0004 -->
**UR-0004 — Give full orientation; start from why it matters to them** — `user_requirement`, status `approved`

> Open by placing the subject in context and explaining why it matters to the reader.

*Derives from:* INT-0001

**source_ref**: TBS Audience — General reader — Context and orientation
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0004' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0007 | system_requirement | approved | Open by explaining what the subject is and why it matters to the reader |
| SR-0008 | system_requirement | approved | Provide the background needed to make sense of the content |
<!-- tl:end -->

## 5. Use everyday analogies and familiar situations

<!-- tl:item UR-0005 -->
**UR-0005 — Use everyday analogies and familiar situations** — `user_requirement`, status `approved`

> Anchor unfamiliar ideas in examples and reference points from ordinary life.

*Derives from:* INT-0001

**source_ref**: TBS Audience — General reader — Examples and reference points
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0005' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0009 | system_requirement | approved | Illustrate with everyday analogies and situations from ordinary life |
| SR-0010 | system_requirement | approved | Relate figures and concepts to familiar reference points |
<!-- tl:end -->
