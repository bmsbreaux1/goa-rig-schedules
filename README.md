# goa-rig-schedules

Rig schedules for the US Gulf, rebuilt from public BSEE data.

Private jackups and platform rigs publish no fleet status report. BSEE's eWell Well Activity Reports (WAR) do the job instead: every well has a rig name, a start date, an end date and a block.

> This repo is a showcase of the method and the output. No private data is involved; the source is public.

## Source

| Dataset | What it gives |
|---|---|
| eWell WAR (Well Activity Reports) | Rig name, start and end date, operator, water depth, lease / area / block per well. About 369,000 rows, back to 2008. |
| eWell APD (permits) | Rig name and approval date: a forward signal |
| BSEE Rig ID register | Cumulative rig list (a register, not an active list) |

Source: https://www.data.bsee.gov/Well/eWellWAR/Default.aspx

## What it produces

- A rig schedule per unit: where it worked, for whom, and when
- A rig leaderboard for the US side of the Gulf
- Liftboat demand by operator. WAR logs liftboat and coil-tubing work as the "rig", but never names the vessel, so demand is operator-level only.

## Known limits

- The eWell page is a DevExpress ASP.NET app. A scripted POST ignores the date filter and returns every row, and the CSV button returns HTML. Filter and export in a browser.
- The reporting lag on current-year rows is not verified.
- US side only. Mexican waters are out of scope.

## Where it is used

GOA Markets, a market desk with producers, active rigs and a rig schedule: https://claude.ai/artifact/5eFRMmLh1iSmkwq2MsE25P

## Contact

Britt Breaux · britt@breauxoffshore.com · Houston, TX
