---
id: agent-deployment
title: Deployment
sidebar_label: Deployment
---

## Quick Start

```bash
cp agent/.env.example agent/.env
# edit agent/.env with your Yacht server URL and enrollment token
docker compose -f agent/docker-compose.yaml up -d
```

## Environment Variables

| Variable | Required | Description |
| --- | --- | --- |
| `YACHT_SERVER_URL` | Yes | Base URL of your Yacht server |
| `YACHT_AGENT_ENROLLMENT_TOKEN` | Yes | Enrollment token from Yacht server settings |
| `YACHT_AGENT_NAME` | No | Display name for the agent host |
| `YACHT_AGENT_VERIFY_SSL` | No | Set `false` for self-signed certs |
| `YACHT_AGENT_HEARTBEAT_INTERVAL` | No | Heartbeat interval in seconds |
| `YACHT_AGENT_JOB_POLL_INTERVAL` | No | Job poll interval in seconds |
| `YACHT_AGENT_VERSION` | No | Agent version string |

## Docker Socket

The agent requires access to the local Docker socket.

```yaml
volumes:
  - /var/run/docker.sock:/var/run/docker.sock
```
