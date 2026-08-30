---
id: agent-troubleshooting
title: Troubleshooting
sidebar_label: Troubleshooting
---

## Registration fails

- Verify `YACHT_SERVER_URL` is reachable.
- Verify the enrollment token matches the server.
- Check server logs for enrollment errors.

## Heartbeat rejected

- The agent automatically re-registers on 401/403/404.
- If this loops, verify the host was not deleted or revoked in Yacht.

## Compose jobs fail

- Ensure the Docker Compose plugin is installed in the agent image.
- Ensure `working_dir` contains a valid compose file.
- Check agent logs for command failures.
