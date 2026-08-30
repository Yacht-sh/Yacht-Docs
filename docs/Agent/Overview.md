---
id: agent-overview
title: Yacht Agent
sidebar_label: Overview
---

The Yacht Agent is a lightweight remote runtime that lets Yacht manage Docker hosts without exposing the Docker API directly.

## What it does

- Registers with a Yacht server using a shared enrollment token
- Heartbeats status and host metadata
- Syncs inventory: containers, images, volumes, networks, and compose projects
- Executes queued jobs: container actions and compose actions

## Why use it

- Keeps Docker sockets off the network
- Centralizes control through Yacht
- Preserves existing workflows with remote Docker hosts
