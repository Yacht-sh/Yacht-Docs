---
id: agent-protocol
title: Agent Protocol
sidebar_label: Protocol
---

This document describes the protocol between the Yacht server and `yacht-agent`.

## Base URL

The agent uses the Yacht server's `/api` prefix. Set `YACHT_SERVER_URL` to the base server URL; the agent appends `/api` if missing.

## Endpoints

### Register

```http
POST /agents/register
Header: X-Yacht-Agent-Enrollment-Token: <token>
Body: registration payload
```

Response includes `host_id`, `agent_id`, `agent_token`, and `heartbeat_interval`.

### Heartbeat

```http
POST /agents/heartbeat
Header: X-Yacht-Agent-Token: <agent_token>
Body: heartbeat payload
```

### Inventory Sync

```http
POST /agents/sync
Header: X-Yacht-Agent-Token: <agent_token>
Body: inventory payload
```

### Job Polling

```http
GET /agents/jobs/next
Header: X-Yacht-Agent-Token: <agent_token>
```

### Job Result

```http
POST /agents/jobs/{job_id}/result
Header: X-Yacht-Agent-Token: <agent_token>
Body: result payload
```

## Job Types

- `container_action`: start, stop, restart, kill, remove
- `compose_action`: up, down, pull
