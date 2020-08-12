---
layout: page
title: Architecture
permalink: /architecture/
---


## Plugins

SmartSHARK consists of different plugins. Each plugin is executed via serverSHARK (although command line execution is possible for each plugin) and writes results into a mongodb.
The plugins are mainly written in python and make use of the models defined in the [pycoshark] library.


## Orchestration

Plugins are orchestrated with [serverSHARK].
In its normal mode it runs jobs on an HPC cluster but it also supports local execution via a worker process and redis.


[serverSHARK]: https://github.com/smartshark/servershark
[pycoshark]: https://github.com/smartshark/pycoshark



## Database

<img src="/assets/database_design3.png" />
