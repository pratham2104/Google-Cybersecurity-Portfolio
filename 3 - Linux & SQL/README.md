# Linux & SQL

**Scenario:** Acting as Linux administrator for a research team, managing file access and investigating security events via SQL.

**What I did:**
- Audited and corrected file permission strings across a shared `projects` directory, removing unauthorized write access and locking down a drafts folder
- Provisioned a new user (`useradd`, `usermod`, `chown`) and assigned group/file ownership
- Used `grep` and `find` to search logs and locate files by name pattern
- Wrote SQL filters (`WHERE`, `OR`) against a login-attempts table to isolate after-hours failed logins and activity on specific dates
- Wrote SQL `INNER JOIN` queries across an employees and machines table to cross-reference device ownership

**Key finding:** SQL filtering surfaced 19 failed login attempts after business hours; the JOIN query matched 185 employee-device records for asset tracking.

**Files:** `3.1` through `3.6`
