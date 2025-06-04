# Usage
## Domain Manager

Complete CRUD Operations:
- Add/remove/list groups
- Add/remove/list brands
- Add/remove/list domains
- Import/export from/to CSV

```bash
# Add a new group
python domain_manager.py group add "Gaming"

# Add a brand to a group
python domain_manager.py brand add "Steam" "Gaming"

# Add a domain to a brand
python domain_manager.py domain add "steampowered.com" "Steam"

# List all groups with their counts
python domain_manager.py group list

# List brands filtered by group
python domain_manager.py brand list --group "Gaming"

# List domains filtered by brand
python domain_manager.py domain list --brand "Steam"

# Import domains from a CSV file
python domain_manager.py csv import domains.csv

# Export filtered domains to a CSV file
python domain_manager.py csv export export.csv --group "Gaming"

# Remove a domain
python domain_manager.py domain remove "steampowered.com"

# Remove a brand (will prompt for confirmation if it has domains)
python domain_manager.py brand remove "Steam"

# Remove a group (will prompt for confirmation if it has brands/domains)
python domain_manager.py group list "Gaming"
```

## Useful Scripts

- Update cron jobs
```bash
sudo crontab -u ubuntu -l
sudo crontab -u ubuntu -e
```

- Run in background
```bash
nohup /home/ubuntu/domain_checker/.venv/bin/python /home/ubuntu/domain_checker/test_bot.py >> /home/ubuntu/domain_checker/log/bot.log 2>&1 &
```

- List all running processes
```bash
ps -ef | grep checker.py
```

- Kill 1 process
```bash
kill -9 [process_id]
```