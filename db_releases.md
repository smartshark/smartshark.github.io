---
layout: page
title: Data Releases
permalink: /dbreleases/
---


As part of SmartSHARK, we have already collect large amount of data, that we already used in our publications. 
Since we are still incrementally updating and improving our database, we decided to organize our usage of the database in release from here on out and try to include
the releases we already used in publications. An increase of the minor version means that more that for the existing projects was added. With major version we also always add more projects. We list the known issues with the data at the bottom of this page. 



If you want to know how to use the releases, our [usage examples repository](https://github.com/smartshark/usage-examples) contains everything you need. 

## License

All release are published under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license. In addition to this homepage, this license is also part of the metadata of the DOI citable long-term archives of the releases (e.g., Zenodo, Figshare).

## List of Releases

### SmartSHARK MongoDB Release 2.2

| Field | Value |
|---|---|
| Short description | Extension of the database with data for 21 additional Java Projects. The data for the new projects does not contain any manual validations.<br><br>Due to the size of the static analysis results, we also provide a smaller version of this release. The smaller version contains all data, except the code entity states, the code group states, and the clone instances.|
| Download Link | Full Version: DOI to be announced <br> Small Version: DOI to be announced <br> Full Version Alternative Download: [smartshark_2_2.agz](http://141.5.100.155/smartshark_2_2.agz)<br>Small Version Alternative Download: [smartshark_2_2_small.agz](http://141.5.100.155/smartshark_2_2_small.agz)|
| Size | Data Size (Full/Small): X Gigabyte / X Gigabyte<br>Backup Size: 246 Gigabyte / 37 Gigabyte |
| MongoDB Version | 4.4 |
| PycoSHARK Version | 1.4.5 |
| jSHARK Version | 2.0.6 |
| Projects | Apache projects: activemq, **ant-ivy**, *archiva*, avro, bigtop, *calcite*, *cayenne*, **commons-bcel**, **commons-beanutils**, **commons-codec**, **commons-collections**, **commons-compress**, **commons-configuration**, **commons-dbcp**, **commons-digester**, commons-imaging, **commons-io**, **commons-jcs**, **commons-jexl**, **commons-lang**, **commons-math**, **commons-net**, **commons-scxml**, **commons-validator**, **commons-vfs**, **curator** cxf-fediz, *deltaspike*, derby, directory-fortress-core, directory-kerby, directory-studio, *eagle*, falcon, fineract, flume, freemarker, **giraph**, **gora**, helix, httpcomponents-client, httpcomponents-core, jackrabbit, james, jena, *jspwiki*, juddi, kafka, karaf-cellar, *knox*, *kylin*, *lens*, *mahout*, *manifoldcf*, maven, maven-archetype, maven-doxia, maven-scm, maven-surefire, maven-wagon,   mina-sshd, nifi, *nutch*, oozie, openjpa, openwebbeans, **opennlp**, oodt, **parquet-mr**, pdfbox, phoenix, pig, portals-pluto, qpid-jms, ranger, reef, roller, samza, **santuario-java**, sis, storm, streams, struts, *systemml*, tapestry-5, tez, *tika*, uima-ducc, usergrid, velocity-engine, velocity-tools, **wss4j**, xerces2-j, xmlgraphics-batik, zeppelin, zookeeper |
| Data | version control history, software metrics, PMD warnings, refactorings, change types, bug fix labels, bug inducing changes, issue tracking data from Jira and GitHub, mailing lists, continuous integration data from Travis CI, pull request and code review data from GitHub. |
| Manual validations | Issue types and links from commits to issues for 38 projects (italic or boldface). Lines that contribute to bug fixes for the 23 projects marked boldface. |
| Citation | [See citation guide](citation.md) |

### SmartSHARK MongoDB Release 2.1

| Field | Value |
|---|---|
| Short description | Extension of the database with data for 28 additional Java Projects. The data for the new projects does not contain any manual validations. Data for pull requests from GitHub and Travis CI was added for all projects that used these systems. The labels were extended with a better fully automated bugfix label that uses a machine learning model for issue type prediction. The inducing changes were extended to also determine the inducing changes for this label, as well as to utilize the manually validated lines of bug fixing commits, where this data is available.<br><br>Due to the size of the static analysis results, we also provide a smaller version of this release. The smaller version contains all data, except the code entity states, the code group states, and the clone instances.|
| Download Link | Full Version: [https://doi.org/10.25625/7OZ1SP](https://doi.org/10.25625/7OZ1SP) <br> Small Version: [https://doi.org/10.25625/PHV2VX](https://doi.org/10.25625/PHV2VX) <br> Full Version Alternative Download: [smartshark_2_1.agz](http://141.5.100.155/smartshark_2_1.agz)<br>Small Version Alternative Download: [smartshark_2_1_small.agz](http://141.5.100.155/smartshark_2_1_small.agz)|
| Size | Data Size (Full/Small): 510 Gigabyte / 40 Gigabyte<br>Backup Size: 198 Gigabyte / 11 Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.4.2 |
| jSHARK Version | 2.0.6 |
| Projects | Apache projects: activemq, **ant-ivy**, *archiva*, bigtop, *calcite*, *cayenne*, **commons-bcel**, **commons-beanutils**, **commons-codec**, **commons-collections**, **commons-compress**, **commons-configuration**, **commons-dbcp**, **commons-digester**, commons-imaging, **commons-io**, **commons-jcs**, **commons-jexl**, **commons-lang**, **commons-math**, **commons-net**, **commons-scxml**, **commons-validator**, **commons-vfs**, **curator** cxf-fediz, *deltaspike*, derby, directory-fortress-core, directory-kerby, directory-studio, *eagle*, falcon, fineract, flume, freemarker, **giraph**, **gora**, helix, httpcomponents-client, httpcomponents-core, jackrabbit,  jena, *jspwiki*, kafka, *knox*, *kylin*, *lens*, *mahout*, *manifoldcf*, maven, mina-sshd, nifi, *nutch*, oozie, openjpa, openwebbeans, **opennlp**, **parquet-mr**, pdfbox, phoenix, pig, ranger, roller, samza, **santuario-java**, storm, streams, struts, *systemml*, tez, *tika*, **wss4j**, xerces2-j, xmlgraphics-batik, zeppelin, zookeeper |
| Data | version control history, software metrics, PMD warnings, refactorings, change types, bug fix labels, bug inducing changes, issue tracking data from Jira and GitHub, mailing lists, continuous integration data from Travis CI, pull request and code review data from GitHub. |
| Manual validations | Issue types and links from commits to issues for 38 projects (italic or boldface). Lines that contribute to bug fixes for the 23 projects marked boldface. |
| Citation | [See citation guide](citation.md) |

### SmartSHARK MongoDB Release 2.0

| Field | Value |
|---|---|
| Short description | Extension of the database with data for 28 additional Java Projects. The data for the new projects does not contain any manual validations. Data for pull requests from GitHub and Travis CI was added for all projects that used these systems. The labels were extended with a better fully automated bugfix label that uses a machine learning model for issue type prediction. The inducing changes were extended to also determine the inducing changes for this label, as well as to utilize the manually validated lines of bug fixing commits, where this data is available.<br><br>Due to the size of the static analysis results, we also provide a smaller version of this release. The smaller version contains all data, except the code entity states, the code group states, and the clone instances.|
| Download Link | Full Version: [https://doi.org/10.6084/m9.figshare.13651346.v1](https://doi.org/10.6084/m9.figshare.13651346.v1)<br>Small Version: [https://doi.org/10.5281/zenodo.4462750](https://doi.org/10.5281/zenodo.4462750) |
| Status | **Superseded by 2.1 - should not be used for new projects!** |
| Size | Data Size (Full/Small): 440 Gigabyte / 37 Gigabyte<br>Backup Size: 173 Gigabyte / 10 Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.4.2 |
| jSHARK Version | 2.0.5 |
| Projects | Apache projects: activemq, **ant-ivy**, *archiva*, bigtop, *calcite*, *cayenne*, **commons-bcel**, **commons-beanutils**, **commons-codec**, **commons-collections**, **commons-compress**, **commons-configuration**, **commons-dbcp**, **commons-digester**, commons-imaging, **commons-io**, **commons-jcs**, **commons-jexl**, **commons-lang**, **commons-math**, **commons-net**, **commons-scxml**, **commons-validator**, **commons-vfs**, *deltaspike*, derby, directory-fortress-core, *eagle*, falcon, flume, **giraph**, **gora**, helix, httpcomponents-client, httpcomponents-core, jackrabbit, jena, *jspwiki*, *knox*, *kylin*, *lens*, *mahout*, *manifoldcf*, mina-sshd, *nutch*, oozie, **opennlp**, **parquet-mr**, pdfbox, phoenix, pig, ranger, roller, samza, **santuario-java**, storm, streams, struts, *systemml*, tez, *tika*, **wss4j**, xerces2-j zookeeper |
| Data | version control history, software metrics, PMD warnings, refactorings, change types, bug fix labels, bug inducing changes, issue tracking data from Jira and GitHub, mailing lists, continuous integration data from Travis CI, pull request and code review data from GitHub. |
| Manual validations | Issue types and links from commits to issues for 38 projects (italic or boldface). Lines that contribute to bug fixes for the 23 projects marked boldface. |
| Citation | [See citation guide](citation.md) |

### SmartSHARK MongoDB Release 1.3

| Field | Value |
|---|---|
| Short description | Release 1.2 updates release 1.0 with manually validated lines for bug fixing commits. This release is a bugfix release for 1.1 which should not be used, because a small percentage of manually labeled may have been affected by a bug that we now corrected. |
| Status | Superseded by 2.x releases. Should only be if only manually validated data is considered. |
| Download Link | [https://doi.org/10.25625/MUZPSF](https://doi.org/10.25625/MUZPSF)<br/>Alternative Download: [smartshark_1_3.agz](http://141.5.100.155/smartshark_1_3.agz) |
| Size | Data Size: 173 Gigabyte<br>Backup Size: 36 Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.4.2 |
| jSHARK Version | 2.0.5 |
| Projects | Apache projects: *ant-ivy*, archiva, calcite, cayenne, *commons-bcel*, *commons-beanutils*, *commons-codec*, *commons-collections*, *commons-compress*, *commons-configuration*, *commons-dbcp*, *commons-digester*, *commons-io*, *commons-jcs*, *commons-jexl*, *commons-lang*, *commons-math*, *commons-net*, *commons-scxml*, *commons-validator*, *commons-vfs*, deltaspike, eagle, *giraph*, *gora*, jspwiki, knox, kylin, lens, mahout, manifoldcf, nutch, *opennlp*, *parquet-mr*, *santuario-java*, systemml, tika, *wss4j* |
| Data | version control history, software metrics, PMD warnings, refactorings, change types, bug fix labels, bug inducing changes, issue tracking data from Jira. |
| Manual validations | Issue types and links from commits to issues for all 38 projects. Lines that contribute to bug fixes for the 23 projects marked italic. |
| Citation | [See citation guide](citation.md) |

### SmartSHARK MongoDB Release 1.2

| Field | Value |
|---|---|
| Short description | Release 1.2 updates release 1.0 with manually validated lines for bug fixing commits. This release is a bugfix release for 1.1 which should not be used, because a small percentage of manually labeled may have been affected by a bug that we now corrected. |
| Download Link | [https://doi.org/10.5281/zenodo.4462720](https://doi.org/10.5281/zenodo.4462720) |
| Status | **Superseded by 1.3 release. Should not be used for new projects.** |
| Size | Data Size: 173 Gigabyte<br>Backup Size: 36 Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.4.2 |
| jSHARK Version | 2.0.5 |
| Projects | Apache projects: *ant-ivy*, archiva, calcite, cayenne, *commons-bcel*, *commons-beanutils*, *commons-codec*, *commons-collections*, *commons-compress*, *commons-configuration*, *commons-dbcp*, *commons-digester*, *commons-io*, *commons-jcs*, *commons-jexl*, *commons-lang*, *commons-math*, *commons-net*, *commons-scxml*, *commons-validator*, *commons-vfs*, deltaspike, eagle, *giraph*, *gora*, jspwiki, knox, kylin, lens, mahout, manifoldcf, nutch, *opennlp*, *parquet-mr*, *santuario-java*, systemml, tika, *wss4j* |
| Data | version control history, software metrics, PMD warnings, refactorings, change types, bug fix labels, bug inducing changes, issue tracking data from Jira. |
| Manual validations | Issue types and links from commits to issues for all 38 projects. Lines that contribute to bug fixes for the 23 projects marked italic. |
| Citation | [See citation guide](citation.md) |

### SmartSHARK MongoDB Release 1.1

This release contains a bug. Release 1.3 is the replacement that contains the correction of the bug. 

### SmartSHARK MongoDB Release 1.0

| Field | Value |
|---|---|
| Short description | This is the first major release of the SmartSHARK MongoDB and data for 38 Java Apache projects. For each project, the data contains the issue tracking data, mailing list data, and version control data, including software metrics, PMD warnings, change type analysis, automated refactoring detection, links between commits and issues, commit labels, and inducing changes. The type of the linked bug issues and the issue links of these data sets were manually validated. |
| Status | **Superseded by 1.3 release. Should not be used for new projects.** |
| Download Link | [https://doi.org/10.5281/zenodo.4071448](https://doi.org/10.5281/zenodo.4071448) |
| Size | Data Size: 173 Gigabyte<br>Backup Size: 36 Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.2.7 |
| jSHARK Version | 2.0.5 |
| Projects | Apache projects: ant-ivy, archiva, calcite, cayenne, commons-bcel, commons-beanutils, commons-codec, commons-collections, commons-compress, commons-configuration, commons-dbcp, commons-digester, commons-io, commons-jcs, commons-jexl, commons-lang, commons-math, commons-net, commons-scxml, commons-validator, commons-vfs, deltaspike, eagle, giraph, gora, jspwiki, knox, kylin, lens, mahout, manifoldcf, nutch, opennlp, parquet-mr, santuario-java, systemml, tika, wss4j |
| Data | version control history, software metrics, PMD warnings, refactorings, change types, bug fix labels, bug inducing changes, issue tracking data from Jira. |
| Manual validations | Issue types and links from commits to issues for all 38 projects. |
| Citation | [See citation guide](citation.md) |

**Known Issues with the Data:**

These issues affect all releases 1.x releases of the SmartSHARK MongoDB. We currently plan to fix the issues with the 3.x releases. We will not fix these issues in the 1.x or 2.x releases, to ensure reproducibility of our results. The validity of results should not be affected due to the small number of issues. 

- The commit 1f62431ebcbc1fb9654151c999349bf0204c465c is unrelated to the issue VALIDATOR-276, even though this is explicitly linked through the commit message.
- The commit e883181ff49d3fa76853e88d4eae1633e0cc383d is unrelated to the issue LANG-100. This was a false positive for SZZ that was not corrected through our manual validation.
- The issue TIKA-889 is not a bug and marked as Cannot Reproduce.
- The issue NET-74 is not a bug because the problem is caught elsewhere. 
- The fix for NET-270 is not in the commit that references the issue. The linked commit only documents the fix in the change log. The actual fix is in the parent commit (which nis not tangled). 
- The issue MATH-832 is not a bug and was marked as invalid. 
- The the issue DBCP-128 was fixed as a side effect of fixing DBCP-198. The commit that references DBCP-128 only adds tests to confirm this. 
- The commit c03da1c2113a09e06104aba58e7e99ece5950f64 is unrelated to the issue JSPWIKI-2, even though this is explicitly linked through the commit message.
- The commit 340b7b69145a03a9702019627cad3071d5d67ef5 is unrelated to the issue JCS-1. This was a false positive for SZZ that was not corrected through our manual validation.
- The commit 059c67079ad0edfb785215578d575dcdcc1daa21 is unrelated to the issue JCS-1. This was a false positive for SZZ that was not corrected through our manual validation.
- The commit 4ff963b47fd82cb1ca8394027518a9183f39176e is unrelated to the issue EAGLE-700. The issue is referenced through the branch name from which the commit was merged and the false positive could only be detected by analyzing the actual code change.

