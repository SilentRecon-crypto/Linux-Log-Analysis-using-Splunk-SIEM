# SPL Queries

This document contains the SPL (Search Processing Language) queries used to analyze Linux logs imported into Splunk.

---

# 1. View All Events

```spl
index=linux
```

### Purpose:
Displays every event stored in the Linux index.

---

# 2. Total Number of Events

```spl
index=linux | stats count
```

### Purpose:
Returns the total number of indexed events.

---

# 3. Events by Source

```spl
index=linux | stats count by source
```

### Purpose:
Displays the number of events from each imported log file.

---

# 4. Events by Sourcetype

```spl
index=linux | stats count by sourcetype
```

### Purpose:
Shows how Splunk classified the imported logs.

---

# 5. Events by Host

```spl
index=linux | stats count by host
```

### Purpose:
Displays events grouped by host.

---

# 6. Authentication Events

```spl
index=linux authentication
```

### Purpose:
Searches authentication-related events.

---

# 7. Failed Authentication Attempts

```spl
index=linux failed
```

### Purpose:
Displays failed authentication attempts.

---

# 8. Successful Login Sessions

```spl
index=linux session
```

### Purpose:
Finds successful login sessions.

---

# 9. Login Events

```spl
index=linux login
```

### Purpose:
Shows login activity.

---

# 10. Sudo Activity

```spl
index=linux sudo
```

### Purpose:
Displays all sudo-related events.

---

# 11. Password Changes

```spl
index=linux passwd
```

### Purpose:
Shows password-related events.

---

# 12. Package Installations

```spl
index=linux source="dpkg.log"
```

### Purpose:
Displays package installation activity.

---

# 13. Installed Packages

```spl
index=linux install
```

### Purpose:
Searches installation events.

---

# 14. Package Upgrades

```spl
index=linux upgrade
```

### Purpose:
Displays upgrade events.

---

# 15. Service Status

```spl
index=linux status
```

### Purpose:
Shows service status messages.

---

# 16. Event Timeline

```spl
index=linux | timechart count
```

### Purpose:
Displays events over time.

---

# 17. Top Event Sources

```spl
index=linux | top source
```

### Purpose:
Shows the most active log files.

---

# 18. Top Hosts

```spl
index=linux | top host
```

### Purpose:
Displays hosts generating the most events.

---

# 19. Top Sourcetypes

```spl
index=linux | top sourcetype
```

### Purpose:
Shows the most common sourcetypes.

---

# 20. Event Distribution by Source

```spl
index=linux
| chart count by source
```

### Purpose:
Visualizes event distribution across log sources.

# Summary

These SPL queries were used to analyze Linux system logs, investigate authentication activity, review administrative actions, monitor package management, and visualize overall system events using Splunk Enterprise.
