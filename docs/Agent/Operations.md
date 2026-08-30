---
id: agent-operations
title: Operations
sidebar_label: Operations
---

## Logs

```bash
docker logs -f yacht-agent
```

Successful startup shows:
- registration accepted
- heartbeat accepted
- inventory sync accepted

## Upgrading

Pull a newer image, then restart the container. The agent preserves state in `/config/agent-state.json`.

## Token Rotation

Rotate the agent bearer token via the server API without re-enrolling.
