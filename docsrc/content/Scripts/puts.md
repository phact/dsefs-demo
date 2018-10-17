---
date: 2017-04-10T14:21:00-05:00
title: Puts and Gets
menu:
  main:
      parent: Scripts 
      identifier: puts
      weight: 201
weight: 2 
---

DSEFS implements the hadoop API's to allow for simple puts and gets to and from the distributed file system.

The demo is scripted for you in the ./dsefs-put-demo executable file. The demo script logs you into DSEFS, creates a "test" directory in DSEFS and puts a file (iris.csv) from the current OS local directory into DSEFS. From there it gets the same file out of DSEFS into the local OS directory naming it foo.csv. After the put and the get then the script logs you out of DSEFS.

### GIF 

Enjoy this animated gif of the functionality in the demo:

![puts](/Scripts/put-demo.gif)
