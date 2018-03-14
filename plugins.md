---
layout: page
title: Plugins
permalink: /plugins/
---

Plugins are executed via the command line by [serverSHARK] and write data to the mongodb.
Each plugin should be available as a tar.gz that [serverSHARK] can install.

## Plugin structure

Basic plugin structure (after decompressing the tar) should be:

- install.sh
- execute.sh
- schema.json
- info.json
- the plugin itself

ServerSHARK executes the **install.sh** to install the plugin and **execute.sh** for normal plugin execution.
The **schema.json** should contain collections and fields the plugin introduces into the mongodb.
The **info.json** should contain general information about the plugin and also the parameters that are required for plugin execution.

## Create plugins

The creation of a plugin is not complicated. It should adhere to the structure described above.
For python plugins there are numerous examples to look at, e.g., [coastSHARK], [issueSHARK].
Additionally, we have one Java plugin, the [refSHARK].

## Currently available plugins for data collection or analysis

The following plugins are currently available.

- [vcsSHARK]: This plugin extracts data from version control systems, e.g., git.
- [mecoSHARK]: Collects software metrics for Java, Phython, C, and C++ projects using [sourcemeter].
- [coastSHARK]: This plugin parses python (via pythons builtin [ast]) and java (via [javalang]) and extracts a bag-of-words vector of the AST node types. The CoastSHARK also extracts every import from every file.
- [issueSHARK]: Collects data from issue tracking systems, e.g., Jira, Bugzilla, and GitHub issues.
- [mailingshark]: Collects data from mailing lists.
- [travisshark]: Collects data from [Travis CI].
- [refshark]: Analyzes Java source code to determine refactorings.
- [labelshark]: Assigns labels (e.g., bugfix, refactoring, documentation) to commits based on the commit message, issue tracking data, and source code changes. 
- [mynboushark]: Creates defect prediction data sets a release of a software version. 
- [identityshark]: Identifies and merges different identities of the same person, e.g., in the issue tracking system and the version control system.
- [memeSHARK]: Compresses stored code entity states without losing information by removing states that did not change in commits. 

[serverSHARK]: https://github.com/smartshark/servershark
[vcsSHARK]: https://github.com/smartshark/vcsshark
[mecoSHARK]: https://github.com/smartshark/mecoshark
[issueSHARK]: https://github.com/smartshark/issueshark
[coastSHARK]: https://github.com/smartshark/coastshark
[pycoshark]: https://github.com/smartshark/pycoshark
[refshark]: https://github.com/smartshark/refshark
[labelshark]: https://github.com/smartshark/labelSHARK
[mynboushark]: https://github.com/smartshark/mynbouSHARK
[identityshark]: https://github.com/smartshark/identitySHARK
[mailingshark]: https://github.com/smartshark/mailingSHARK
[travisshark]: https://github.com/smartshark/travisSHARK
[memeSHARK]: https://github.com/smartshark/memeSHARK
[javalang]: https://github.com/c2nes/javalang
[ast]: https://docs.python.org/3/library/ast.html
[sourcemeter]: https://www.sourcemeter.com/
[Travis CI]: https://travis-ci.org/
