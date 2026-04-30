# Data Policy

This repository commits public code, documentation, tests, protocols and
sanitized evidence summaries.

It does not commit raw source payloads.

## Raw Payloads

Raw source files must stay outside the repository. The public record should
contain:

- official source URL;
- access date;
- source rights or attribution note;
- SHA-256 hashes;
- row counts or coverage summaries;
- command log;
- sanitized report summary;
- claim boundary.

## Why Raw Payloads Stay Outside

Keeping raw payloads outside the repository avoids accidental redistribution,
large files, private paths and source-rights ambiguity.

## Manifest Expectations

Every real-source run should publish a sanitized manifest with:

```json
{
  "source": "official public source name",
  "access_date": "YYYY-MM-DD",
  "raw_payload_committed": false,
  "raw_payload_sha256": "sha256 value or external manifest reference",
  "coverage_summary": "domain-specific coverage summary",
  "source_eligibility": "ELIGIBLE / BLOCKED_SOURCE / INSUFFICIENT_COVERAGE"
}
```

## Commit Guard

The test suite rejects common raw-payload suffixes and raw-payload directory
names. Reviewers should still inspect release candidates manually.
