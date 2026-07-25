# throughline-audience-general

The **general-reader level** of the **audience** content axis, expressed as a
[throughline](https://pypi.org/project/throughline/) **source** — a standalone,
grounded requirements graph that a consuming project composes with
[throughline-compose](https://github.com/rhodium-org/throughline-compose).

This repository holds no application code. It is a directory of small YAML items with
permanent UIDs, validated by `tl check`. Consumers import it under a namespace and
reference its rules as `audience:SR-0001` or its principles as `audience:UR-0001`.

## One orthogonal axis, one reader level

The audience axis is *how the writing is calibrated to the reader's expertise* — how
much prior knowledge it assumes, how much field vocabulary it allows, how deep it goes,
how much orientation it gives. This source is **only** the audience axis, and **only**
its **general** level: a lay reader with no special knowledge of the field. It says
nothing about:

- **readability** (word choice, sentence length, active voice) — `throughline-plain-language`
- **conventions** (spelling, punctuation, capitalisation, numbers) — `throughline-conventions-uk`
- **register** (formal, neutral, informal) — `throughline-tone-*`
- **purpose** (inform, instruct, persuade) — `throughline-purpose-*`
- **medium / channel** and **brand voice**

There is a deliberate tension with the readability axis: plain language is *universal*
clarity for any reader, whereas this axis tunes how much the writer may *assume* and
how much domain vocabulary is acceptable for a *specific* reader. They are independent
and a consumer composes both.

Audience levels are **mutually exclusive**: a piece of writing is pitched at an expert
*or* a practitioner *or* a general reader, never several at once. So each level is a
**sibling** source (`throughline-audience-expert`, `throughline-audience-practitioner`)
and a consumer composes exactly one under the `audience` namespace — swapping level is
a one-line `url`/`ref` change. A task like *"a plain, formal, general-reader web page"*
becomes a **compose** of `plain` + `tone-formal` + `audience-general`.

## What's in the graph

<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles as `user_requirement`s, each `derives_from` the root
intent, and
<!-- tl:count type == 'system_requirement' -->
10
<!-- tl:end --> rules as `system_requirement`s, each `implements` its principle. The
published spec is generated from the graph at [`docs/spec.md`](docs/spec.md).

## Source & licensing

The rules are original house content guidance, licensed under
Apache-2.0. They reproduce no third-party standard. Each rule records its audience
level and dimension in `attrs.source_ref` and its owning principle in
`attrs.principle`. See [`NOTICE`](NOTICE).

## Extending the source

Items are hand-authored static YAML — one file per item, one permanent UID per file.
To add a rule, create the next `SR-00NN.yml` by hand (never renumber an existing one)
and link it with `implements` to its principle. Then:

```sh
tl check --strict      # the graph must stay sound
tl docs                # regenerate docs/spec.md + README.md
tl docs --check        # CI gate: docs must match the graph
```
