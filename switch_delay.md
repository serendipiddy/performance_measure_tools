Measuring Openflow Delay Setup
==============================

## Overview

### What's being measured

### Network Topology

* Time keeper host

### Capturing the Time

#### Hardware Timestamps

#### PF-Ring

##### Lock buffer Mod

##### Processing Results

#### TCPDump

##### Processing The results

### The Controller

### Tmux orchestration


## Suggestion For performing the action delay measurements

### Ryu Application
Remember to keep one packet in network at a time (remove queueing delay)

#### List of actions
Tuple of actions, have an index variable to select the current action. Use *sed* to change the action being selected.
Restart the controller each run.
Doesn't require measuring the time to match increasing number of rules.

####  Multiple Rules at once
Different match fields to select different OFP actions.
Insert all OFP rules at once.
Send batches of traffic for each one (not concurrently performing each test)

## List of Scripts