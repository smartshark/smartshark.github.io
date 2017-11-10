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

## Currently available plugins

The following plugins are currently available.

### [VCSShark]

This plugin extracts data from version control systems, e.g., git.

### [MecoSHARK]

todo

### [IssueSHARK]

todo

### [RefSHARK]

todo

### [CoastSHARK]

This plugin parses python (via pythons builtin [ast]) and java (via [javalang]) and extracts a bag-of-words vector of the AST node types.
It uses the AST to also extract every import from every file.


[serverSHARK]: https://github.com/smartshark/servershark
[vcsSHARK]: https://github.com/smartshark/vcsshark
[mecoSHARK]: https://github.com/smartshark/mecoshark
[issueSHARK]: https://github.com/smartshark/issueshark
[coastSHARK]: https://github.com/smartshark/coastshark
[pycoshark]: https://github.com/smartshark/pycoshark
[refshark]: https://github.com/smartshark/refshark
[javalang]: https://github.com/c2nes/javalang
[ast]: https://docs.python.org/3/library/ast.html