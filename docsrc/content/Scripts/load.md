---
date: 2017-04-10T14:21:00-05:00
title: Load / Unload
menu:
  main:
      parent: Scripts 
      identifier: load
      weight: 201
weight: 3
---

DSEFS can be used to load or unload data to and from Cassandra, as well as DSEFS. In this demo we create a keyspace (test), a table (iris) and a class (Iris) and inserts the data from the iris.csv file into Cassandra. Then we create json files on DSEFS, under the test directory, to hold this same data. From there the two json files are read from DSEFS and joined together displaying the first three rows.

### GIF 

Enjoy this animated gif of the functionality in the demo:

![loadunload](/Scripts/load-demo.gif)
