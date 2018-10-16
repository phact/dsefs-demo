---
title: Build and Run
menu:
  main:
      parent: Scripts
      identifier: buildandrun
      weight: 201
weight: 5
---

Example for using this DSEFS demo

## Startup Script

This Asset leverages
[simple-startup](https://github.com/jshook/simple-startup). To start the entire
asset run `./startup all` for other options run `./startup`

In this demo the simple startup script automatically cycles through the demo steps (e.g. ./startup <step>). The steps are:

- load - goes through the load / unload demo
- put - goes through the get / put demo
- spark-streaming-checkpointing-job - this demo is a little more involved and requires opening up two terminal windows. One to provide data (./startup move-files) and the other to demonstrate the checkpointing (./startup spark-streaming-checkpointing-job)

Alternatively there are commands that also perform the above.

- dsefs-load-unload 
- dsefs-put-demo
- dsefs-checkpoint with dsefs-stream, each initiated from different terminals

All commands including the startup command is in the /tmp/dsefs-demo directory.
