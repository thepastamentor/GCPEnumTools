# GCP Enumeration Tools

Simple tools for enumerating Google Cloud Platform and Google Workspace configurations.

These are largely pulled from the pwnedlabs.com GCP boot camp.

## Tools

### gcpdomaincheck
Check if a domain uses Google Workspace or Gmail.
```bash
./gcpdomaincheck example.com
```

**Requirements:** `curl`, `jq`

### gcpcalcheck
Check if email addresses have public Google Calendars.
```bash
# Single email
./gcpcalcheck user@example.com

# Multiple emails
./gcpcalcheck user1@example.com user2@example.com

# From file
./gcpcalcheck emails.txt

# From stdin
cat emails.txt | ./gcpcalcheck
```

**Requirements:** `python3`, `requests`

## Installation
```bash
chmod +x gcpdomaincheck gcpcalcheck
pip3 install requests
```

## Output

- **gcpdomaincheck:** Indicates if domain uses Google Workspace/Gmail
- **gcpcalcheck:** Prints emails with public calendars (asterisk `*` indicates HTTP 200)
