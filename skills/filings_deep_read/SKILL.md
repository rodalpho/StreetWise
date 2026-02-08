---
name: filings-deep-read
description: Retrieve and analyze targeted sections from SEC filings before broad extraction.
---

# Filings Deep Read

## Trigger
Use when the user asks about risks, guidance, material events, accounting policy, segment detail, or management commentary.

## Checklist
1. Identify target company and likely filing type (10-K, 10-Q, 8-K).
2. Retrieve recent filing metadata.
3. Select specific sections relevant to the question.
4. Read selected sections first.
5. Expand to full filing only if targeted sections are insufficient.
6. Extract direct evidence, dates, and management statements.
7. Synthesize answer with clear citations.

## Section Mapping
1. Risk factors -> 10-K Item 1A or 10-Q Part II Item 1A
2. Business overview -> 10-K Item 1
3. MD&A -> 10-K Item 7 or 10-Q Part I Item 2
4. Financial statements -> 10-K Item 8 or 10-Q Part I Item 1
5. Material event -> 8-K

## Guardrails
1. Do not claim a filing said something unless text was retrieved.
2. Prefer newest relevant filing unless user asked otherwise.
3. Include accession/date in evidence summary when available.

## Output
1. Direct answer.
2. Evidence bullets with filing section/date.
3. Any unresolved ambiguity and next-best source path.
