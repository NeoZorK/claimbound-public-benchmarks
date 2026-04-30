# NOAA CO-OPS D-131 Negative Result

Status: `NEGATIVE_RESULT_UNDER_PROTOCOL`

## Summary

The NOAA CO-OPS D-131 run used official NOAA CO-OPS Data Retrieval API payloads
under a frozen protocol. The source audit passed, but the statistical acceptance
gate did not pass.

This is a negative result. It must not be presented as accepted evidence.

## Source Scope

```text
Official source: https://api.tidesandcurrents.noaa.gov/api/prod/datagetter
Observed product: hourly_height
Prediction product: predictions
Prediction interval: h
Datum: MLLW
Time zone: gmt
Units: metric
Format: json
Period: 2018-01-01..2024-12-31
Stations: 8518750, 9414290, 8638610
Raw payload committed: no
```

## Outcome

```text
Source audit: passed
Eligible stations: 3
Eligible windows: 11
overall_go_no_go: false
result_status: NEGATIVE_RESULT_UNDER_PROTOCOL
```

Report SHA-256:

```text
87d4d51f134f88c558235efaa3499e8b8bbac1cfc7051189f4954302c61295b6
```

External payload manifest SHA-256:

```text
cd46899966ec855bc91b5c575d4713c068f320d41cb07e9c1a91b5190cbe4a67
```

## Failed Gates

Recorded failure modes:

- seasonal hour-of-year residual control was not beaten;
- event rate fell below the minimum in one window;
- event rate exceeded the maximum in one window.

## Allowed Claim

```text
NOAA CO-OPS D-131 was executed on official NOAA CO-OPS data under a frozen
protocol and recorded as NEGATIVE_RESULT_UNDER_PROTOCOL.
```

## Forbidden Claims

Do not claim:

- D-131 passed;
- coastal-warning performance was proven;
- universal forecasting edge;
- deployment readiness;
- superiority over all statistical methods.
