# Result Status

Every public evidence record should use one exact status.

## PASSED_UNDER_PROTOCOL

The source audit passed, enough stations or points were eligible, enough windows
were eligible, and the candidate passed the frozen acceptance gate.

Allowed claim: only the narrow protocol-bound claim written in the evidence
record.

## NEGATIVE_RESULT_UNDER_PROTOCOL

The source audit passed, but the candidate did not pass the frozen acceptance
gate.

Required interpretation: no positive performance claim.

## BLOCKED_SOURCE

The source could not be used under the protocol because access, rights,
coverage, metadata or source-lineage requirements were not satisfied.

Required interpretation: no empirical pass/fail claim.

## INSUFFICIENT_COVERAGE

The source was identified, but coverage was too sparse or too uneven for the
pre-registered test.

Required interpretation: no positive claim.

## REPRODUCED_OUTCOME

An independent rerun reproduced the result status and gate-level outcome.

## REPRODUCED_OUTCOME_WITH_SOURCE_BYTE_DRIFT

An independent rerun reproduced the result status and gate-level outcome, but
fresh source payload bytes differed from the original payload bytes.

Required interpretation: do not claim raw-byte reproduction.
