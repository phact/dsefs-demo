---
title: Architecture
menu:
  main:
      parent: Scripts 
      identifier: architecture
      weight: 201
weight: 6
---

This section details the architecture demonstrated in this reference field asset.

### Architecture Diagram

<div title="rendered dynamically" align="middle">

graph LR
B--"Checkpointing"-->E
C["Client"]
A["Queue"]--"Streaming Ingest"-->B["DSE Streaming Analytics"]
B--"microbatches"-->C["DSE Cassandra"]
E["DSEFS"]--"Load"-->C
C--"Unload"-->E

</div>

### Architecture

Uses for DSEFS include:

- Loading and Unloading data into DSE Core (Cassandra)
- Checkpointing during Spark streaming jobs
- Spark analytics application processing scratchpad (puts and gets) 

This demo will visit each of these use cases.
