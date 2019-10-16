---
layout: page
title: Tutorial for Python Plugins
exclude: true
permalink: /plugin/tutorial/python
---

# How to create a plugin for SmartSHARK
This tutorial explains how to create a python plugin for SmartSHARK. We explain how you can create a simple plugin for SmartSHARK using the minimal working example [pymweSHARK](https://github.com/smartshark/pymweSHARK). The first section will provide you with the basic information. More advanced information will be outlined for each file in the files section.

## Get started
1. Modify the content of the setup.py and the info.json with your information
2. Create a new folder, with the name of the plugin
3. This folder is your workspace. Add any python files here.
4. The main.py contains the main method and start point of the plugin. It automatically setups some logging parameters and start the timing of the execution. 
5. Parse additional parameters and start your plugin

## Command Line Parameters

### Get a parameter
All parameters are automatically parsed in the main.py routine. 
Example:
```
parser.add_argument('--output', help='Output Folder', required='true')
args = parser.parse_args()
output_folder = args.output # Get the parameter
```

### Add a parameter
To add a parameter follow these steps:
1. Add the parameter to the info.json
2. Add the parameter to the execute.sh in the plugin_packaging folder. Add the parameter to COMMAND and decide, if the parameter is optional. Be careful that you have the same position as in your info.json.
3. Add the parameter to the parser in the main.py
4. Read your parameter in the main.py

## Reading and Writing Data

### Create a database connection
It is possible to create a database connection with [mongoengine](http://mongoengine.org/) library. The following code creates an uri from the connection arguments and connects to the database.
```
uri = create_mongodb_uri_string(user, password, host, port, authentication, ssl)
connect(database, host=uri)
```

### Reading Data
You are able to read data from the database with an active database connection. Just use the [mongoengine](http://mongoengine.org/)  syntax. For example:
```
project_id = Project.objects.get(name=self.args.project_name).id
```

### Writing Data
You are able to modify the database with an active database connection. Any added or modified collection should be stated in the schema.json.
Example:
```
{
   "fields":[
      {
         "type":"ObjectIdType",
         "logical_type":"OID",
         "field_name":"_id",
         "desc":"Identifier of the document."
      },
      {
         "sub_type":"StructType",
         "type":"ArrayType",
         "field_name":"induces",
         "logical_type":"List",
         "desc":"List of file actions this file action induces.",
         "fields":[
            {
               "desc":"Reference to the file action this file action induces.",
               "field_name":"change_file_action_id",
               "logical_type":"RID",
               "reference_to":"file_action",
               "type":"ObjectIdType"
            },
            {
               "type":"StringType",
               "logical_type":"Name",
               "field_name":"szz_type",
               "desc":"SZZ type for this inducing file action as per the original algorithm (weak_suspect, hard_suspect, partial_fix, inducing)"
            },
            {
               "type":"StringType",
               "logical_type":"Name",
               "field_name":"label",
               "desc":"SmartSHARK label for this inducing file action."
            }
         ]
      }
   ],
   "desc":"",
   "collection_name":"file_action"
}
```

## Build and Installation
Execute the following command to build the plugin and create an archive for uploading to the [ServerSHARK](https://github.com/smartshark/serverSHARK) Server.
```
./plugin-packaging/build_plugin.sh
```

## Add external libraries
You are able to add any external library to the array 'install_requires' in the setup.py. 
Example:
```
install_requires=['pycoshark>=1.0.28', 'pygit2==0.26.2', 'networkx>=2.2'],
```

Additional information can be found in the documentation of python [here](https://docs.python.org/3.7/distutils/setupscript.html).

# Files
In this section, we will provide detailed information about any file of the minimal working example. 
* .travis.yml
File for the Travis-Build System. 
* main.py
Main python script file. The template already contains some helper function for parsing and timining setup.
* setup.py
Additional information about the setup.py can be found in the documentation from python [here](https://docs.python.org/3.7/distutils/setupscript.html).
* build_plugin.sh
Script for creating a zip archive file of the plugin that can be used by the [ServerSHARK](https://github.com/smartshark/serverSHARK). 
* execute.sh
The plugin is executed with this script file. You may add here some additional parameters for your plugin.
* info.json
Contains important meta information about the plugin. This file is readed by the [ServerSHARK](https://github.com/smartshark/serverSHARK) to ensure that the requirements to execute the plugin are given. 
* install.sh
Install-Script: Usually, you do not need to change anything here. The template executes the normal python installation with the setup.py file. 
* schema.json
Contains information about collections and fileds that may be modified in the database by this plugin.



