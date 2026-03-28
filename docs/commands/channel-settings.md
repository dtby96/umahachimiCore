# Channel Settings

These commands are restricted to server admins.

---

## /set_report_channel

Set the channel where daily quota reports are posted.

| Parameter | Required | Description |
|---|---|---|
| `channel` | Yes | Discord text channel |
| `club` | Yes | Target club |

---

## /set_alert_channel

Set the channel where alerts (bombs, kicks) are posted.

| Parameter | Required | Description |
|---|---|---|
| `channel` | Yes | Discord text channel |
| `club` | Yes | Target club |

---

## /channel_settings

View the current report and alert channel configuration for a club.

| Parameter | Required | Description |
|---|---|---|
| `club` | Yes | Target club |

---

## /post_monthly_info

Post the monthly info board to a channel. This embed automatically updates whenever quota changes are made.

| Parameter | Required | Description |
|---|---|---|
| `club` | Yes | Target club |
| `channel` | No | Channel to post in (defaults to report channel) |

---

## /update_monthly_info

Manually refresh the monthly info board embed.

| Parameter | Required | Description |
|---|---|---|
| `club` | Yes | Target club |
