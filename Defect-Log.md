# Defect and Observation Log — SauceDemo

## Confirmed reproducible defects
**None confirmed in the documented scenarios.**

## OBS-001 — Inconsistent initial locked-out login response (not reproduced)

- **Area:** Login
- **Account:** `locked_out_user`
- **Initial observation:** Generic username/password mismatch message instead of locked-out notification.
- **Expected:** `Epic sadface: Sorry, this user has been locked out.`
- **Retest:** Two attempts in Chrome Incognito displayed the expected locked-out message.
- **Disposition:** Not reproducible; no confirmed bug filed. Retain as an observation for possible future investigation.

## Reporting standard
A confirmed defect should include a reproducible sequence, expected vs. actual results, environment, and evidence. An isolated unreproduced observation is not represented as a confirmed product bug.
