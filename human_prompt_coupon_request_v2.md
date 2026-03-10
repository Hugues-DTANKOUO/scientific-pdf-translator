# HUMAN PROMPT — COUPON CALCULATION REQUEST

---

## Accrual Period Parameters

| Parameter              | Value                      | Notes                                              |
|------------------------|----------------------------|----------------------------------------------------|
| `payment_date`         | {payment_date}             | ISO 8601 (YYYY-MM-DD)                              |
| `accrual_start_date`   | {accrual_start_date}       | ISO 8601 — use adjusted date if applicable         |
| `accrual_end_date`     | {accrual_end_date}         | ISO 8601 — use adjusted date if applicable         |
| `coupon_period_number` | {coupon_period_number}     | Integer (1 = first coupon); required for step notes |
| `currency_notional`    | {currency_notional}        | Outstanding notional for this period (post-amortization if applicable) |
| `min_denomination`     | {min_denomination}         | Minimum / Calculation Amount; null if not applicable |
| `range_n`              | {range_n}                  | Accrual days in range; null if not a range accrual  |
| `range_m`              | {range_m}                  | Total observation days; null if not a range accrual |
| `rate_1_name`          | {rate_1_name}              | System identifier — agent must map to document      |
| `rate_1_value`         | {rate_1_value}             | Numeric value (verify unit: % or decimal in document) |
| `rate_2_name`          | {rate_2_name}              | null if no second rate                              |
| `rate_2_value`         | {rate_2_value}             | null if no second rate                              |

> **Null convention**: pass `null` (or `None`) for any parameter that does not
> apply to this note. Do not pass `0` as a substitute for "not applicable" —
> it would alter the calculation.

---

## Document

The term sheet / pricing supplement is provided below.

[DOCUMENT]
