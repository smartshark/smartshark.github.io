---
layout: page
title: Tutorial Plugin Java
permalink: /plugin/tutorial/java
---

# How to create a plugin for SmartSHARK
This tutorial explains how to create a Java plugin for SmartSHARK. We explain how you can create a simple plugin for SmartSHARK using the minimal working example [jmweSHARK](https://github.com/smartshark/jmweSHARK). The first section will provide you with the basic information. More advanced information will be outlined for each file in the files section.

## Get started
1. Modify the content of the build.gradle (for dependencies) and the plugin_packaging/info.json with your information
2. Rename the source package of your Java application to pluginnameSHARK
3. The JmweShark.java is the main application of the Java plugin. It contains the Java main method and is therefore the start point. 
4. In the example Java class, is some code to parse additional arguments (command line parameters) and setup the logging, the database connection and time measurements. 
## Command Line Parameters
### Get a parameter
All parameters are automatically parsed in the main method.
Example:
```
Parameter param = Parameter.getInstance();
param.init(args);
```
### Add a parameter
To add a parameter follow these steps:
1. Add the parameter to the info.json
2. Add the parameter to the execute.sh in the plugin_packaging folder. Add the parameter to COMMAND and decide, if the parameter is optional. Be careful that you have the same position as in your info.json.
3. Read your parameter in the Java main method
## Reading and Writing Data
### Create a database connection
It is possible to create a database connection with [morphia](https://github.com/MorphiaOrg/morphia) library. The following code creates an uri from the connection arguments and connects to the database.
```
client = new MongoClient(Parameter.getInstance().getDbHostname(), Parameter.getInstance().getDbPort());
datastore = morphia.createDatastore(client,Parameter.getInstance().getDbName());
```
### Reading data 
You are able to read data from the database with an active database connection. Just use the [morphia](https://github.com/MorphiaOrg/morphia) syntax. For example:
```
Query<Project> projects = datastore.createQuery(Project.class);
for (Project project : projects) {
  System.out.println(project.getName());
}
```
### Writing data
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
Execute the following commands to build the plugin and create an archive for uploading to the [ServerSHARK](https://github.com/smartshark/serverSHARK) Server.
```
./gradlew build
./plugin-packaging/build_plugin.sh
```

## Add external libraries
You are able to add any external library to the build.gradle file in the root folder.
Additional information can be found in the documentation of gradle [here](https://gradle.org/).

## Files
In this section, we will provide detailed information about any file of the minimal working example. 
* .travis.yml
File for the Travis-Build System. 
* JmweSHARK.java
The Java main class of the plugin. The main method is automatically called by execution of the plugin.
* build.gradle
The gradle build file for the project; additional information about the build.gradle file can be found in the documentation from gradle [here](https://docs.gradle.org/current/userguide/tutorial_using_tasks.html).
* build_plugin.sh
Script for creating a zip archive file of the plugin that can be used by the [ServerSHARK](https://github.com/smartshark/serverSHARK). 
* execute.sh
The plugin is executed with this script file. You may add here some additional parameters for your plugin.
* info.json
Contains important meta information about the plugin. This file is readed by the [ServerSHARK](https://github.com/smartshark/serverSHARK) to ensure that the requirements to execute the plugin are given. 
* install.sh
Install-Script: Usually, you do not need to change anything here. 
* schema.json
Contains information about collections and fileds that may be modified in the database by this plugin.



