#!/usr/bin/env groovy

/**
    This script deletes all offline nodes
*/
for (aSlave in hudson.model.Hudson.instance.slaves) {
  println('Checking Node ' + aSlave.name);
  if(aSlave.getComputer().isOffline() == true) {
    println('Removing Node ' + aSlave.name);
    aSlave.getComputer().setTemporarilyOffline(true,null);
    aSlave.getComputer().doDoDelete();
  }
}
