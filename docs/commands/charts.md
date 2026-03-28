# Charts & Stats

---

## /progress_chart

Generate a cumulative fan progression chart for all members in a club this month.

| Parameter | Required | Description |
|---|---|---|
| `club` | Yes | Target club |

The chart shows one line per active member with dates on the X-axis and cumulative fans on the Y-axis. Members who joined mid-month will only have data from their join date onward.

**Data sources (in priority order):**
1. Uma.moe API — full month history (requires `circle_id`)
2. Database fallback for ChronoGenesis clubs

> On day 1 of the month, the chart falls back to previous month data since the current month hasn't populated yet.

---

## /previous_month

View last month's final fan totals for all members, ranked by performance.

| Parameter | Required | Description |
|---|---|---|
| `club` | Yes | Target club |

Shows each member's total fans earned last month. Members who joined mid-month are indicated.

---

## /stats

View bot-wide statistics including total clubs, members, active bombs, and uptime.

**Restricted to the bot author only.**

No parameters.
