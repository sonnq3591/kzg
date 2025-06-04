# config/config.yml – System Settings

This file controls the behavior of the domain checker system.

## 🔧 Sections

### telegram
Used to send notifications to a Telegram group using a bot.
- `bot_token`: Telegram bot API token.
- `chat_id`: Group/channel where messages are sent.

### database
Paths for storage and domain list input:
- `monitor.db`: stores domain results.
- `bulk_domains.csv`: list of domains to check.

### timezone_offset
Adjusts log/report time to local time (e.g. +7 for Vietnam/Thailand).

### check_interval_hours
How often the domain checker runs. Default: 1 hour.

### proxies
List of rotating proxy servers used to avoid IP bans. Each proxy has:
- name, IP, port, username, password.

### domain
- `group_order`: Custom labels to organize domains.
- `safe_markers`: List of strings (e.g. HTML tags or JS code) used to identify "safe" or working websites.

### performance
Settings to manage resource load:
- `max_workers`: Number of async workers.
- `retry_attempts`: Retry logic when domains fail.

### batch
Settings for domain batch processing:
- `size`: Number of domains per batch.
- `max_concurrent`: Parallel batches.
- `domain_delay`: Wait time between domain checks.

### proxy_management
If a proxy fails, how long to wait and how many retries.

### headers
Spoof browser request headers to avoid detection.

### error domain recheck
Controls logic for retrying failed domains, using proxies or not.

## 📌 Key Idea
This config enables full control over domain checking without changing the codebase. Ideal for testing, scheduling, or scaling.

