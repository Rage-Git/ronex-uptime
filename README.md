# ronex-uptime

Outside uptime monitor for the Ronex system. A GitHub Actions job checks the app (and its database) and the public
website every 5 minutes from GitHub's servers. When a check fails twice in a row it opens an incident on the Ronex
System Health page and fails the run (GitHub emails the owner); when it passes again the incident is closed with its
exact duration.

The webhook key is the repository secret `INCIDENT_HOOK_KEY`. Nothing private is stored in this repository.
