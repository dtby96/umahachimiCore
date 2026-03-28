# Data Sources

UmaCore supports two data sources for fetching member fan counts.

---

## Uma.moe API (Recommended)

The primary data source. Fast and reliable.

**Requires:** `circle_id` set on the club (see below)

**What it provides:**
- Full month history per member
- Daily cumulative fan counts
- Club ranking data

**Finding your Circle ID:**
1. Go to [uma.moe/circles](https://uma.moe/circles/)
2. Search for your club
3. Copy the numeric ID from the URL
   - Example: `https://uma.moe/circles/860280110` → use `860280110`
4. Set it with `/add_club circle_id:860280110` or `/edit_club circle_id:860280110`

**Timing notes:**
- Data updates around 15:10 UTC daily
- On day 1 of the month, the bot fetches the previous month (current month hasn't populated yet)
- If today's data isn't ready yet, the bot falls back to yesterday's data automatically

---

## ChronoGenesis Scraper (Fallback)

Used when a club has no `circle_id`, or when `USE_UMAMOE_API=false` is set in `.env`.

**Requires:** Chrome/Chromium installed on the host machine

**Limitations:**
- Slower than the API
- Dependent on ChronoGenesis page structure (may break if the site changes)
- Less reliable overall

The bot automatically falls back to ChronoGenesis if the Uma.moe API fails.

---

## Switching Data Sources

To use Uma.moe API globally (default):
```env
USE_UMAMOE_API=true
```

To force ChronoGenesis globally:
```env
USE_UMAMOE_API=false
```

Per-club: if a club has no `circle_id` set, it always uses ChronoGenesis regardless of the global setting.
