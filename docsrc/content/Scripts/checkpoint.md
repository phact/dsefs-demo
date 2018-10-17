---
title: Checkpointing
menu:
  main:
      parent: Scripts 
      identifier: checkpoint
      weight: 201
weight: 2
---

The most common use case for DSEFS is spark streaming checkpointing. In this demo you have two scripts that will be used. The dsefs-checkpoint script and the dsefs-stream script. Both should be ran in separate terminal windows. The dsefs-stream script is simple, it prompts the user to hit the enter key and from there it copies our iris.csv file to three files in the stream directory. Then it prompts the user to hit enter again, creating three more files.

Since dsefs-checkpoint relies on the files in the stream directory to exist, expect some errors to be thrown at first. The dsefs-checkpoint script deletes the contents of the "/tmp/dsefs-demo/stream" directory and then creates a checkpoint, then reading the files in the "/tmp/dsefs-demo/stream" directory, displaying the count of individual species records. Of course this will be blank at first until the dsefs-stream script is ran to populate the "/tmp/dsefs-demo/stream" directory. This cycles every 2 seconds for 10 executions and it does this twice. The checkpoint information is written into DSEFS under the "checks" subdirectory. 

**Tip:** Kickoff the dsefs-checkpoint script first, wait until it compiles and starts logging. In another terminal window kick off the dsefs-stream script. You will notice the totals increase as the files are written to the "/tmp/dsefs-demo/stream" directory. Logon to DSEFS and list the checkpoints that have been created in the "checks" directory.

### GIF

Enjoy this animated gif of the functionality in the demo:

![checkpointing](/Scripts/checkpoint-demo.gif)
