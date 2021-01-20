---
layout: page
title: Data Releases
permalink: /dbreleases/
---


As part of SmartSHARK, we have already collect large amount of data, that we already used in our publications. 
Since we are still incrementally updating and improving our database, we decided to organize our usage of the database in release from here on out and try to include
the releases we already used in publications. An increase of the minor version means that more that for the existing projects was added. With major version we also always add more projects. We list the known issues with the data at the bottom of this page. 

If you want to know how to use the releases, our [usage examples repository](https://github.com/smartshark/usage-examples) contains everything you need. 

## List of Releases

### SmartSHARK MongoDB Release 2.0

| Field | Value |
|---|---|
| Short description | Extension of the database with data for 28 additional Java Projects. The data for the new projects does not contain any manual validations. The labels were extended with a better automated bugfix label that uses a machine learning model for issue type prediction. The inducing changes were extended to also determine the inducing changes for this label, as well as to utilize the manually validated lines of bug fixing commits, where they are available. |
| Download Link | TODO |
| Size | Data Size: TBD Gigabyte<br>Backup Size: TBD Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.4.2 |
| jSHARK Version | 2.0.5 |
| Citation | [See citation guide](citation.md) |

### SmartSHARK MongoDB Release 1.2

| Field | Value |
|---|---|
| Short description | Release 1.2 updates release 1.0 with manually validated lines for bug fixing commits. This release is a bugfix release for 1.1 which should not be used, because a small percentage of manually labeled may have been affected by a bug that we now corrected. |
| Download Link | TODO |
| Size | Data Size: 172.9 Gigabyte<br>Backup Size: 36.2 Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.4.2 |
| jSHARK Version | 2.0.5 |
| Citation | [See citation guide](citation.md) |

### SmartSHARK MongoDB Release 1.1

This release contains a bug. Release 1.2 is the replacement that contains the correction of the bug. 

### SmartSHARK MongoDB Release 1.0

| Field | Value |
|---|---|
| Short description | This is the first major release of the SmartSHARK MongoDB and data for 38 Java Apache projects. For each project, the data contains the issue tracking data, mailing list data, and version control data, including software metrics, PMD warnings, change type analysis, automated refactoring detection, links between commits and issues, commit labels, and inducing changes. The type of the linked bug issues and the issue links of these data sets were manually validated. |
| Download Link | [https://doi.org/10.5281/zenodo.4071448](https://doi.org/10.5281/zenodo.4071448) |
| Size | Data Size: 172.9 Gigabyte<br>Backup Size: 36.2 Gigabyte |
| MongoDB Version | 4.0 |
| PycoSHARK Version | 1.2.7 |
| jSHARK Version | 2.0.5 |
| Citation | [See citation guide](citation.md) |

**Known Issues with the Data:**

These issues affect all releases 1.x releases of the SmartSHARK MongoDB. We currently plan to fix the issues with the 2.x releases. We will not fix these issues in the 1.x releases, to ensure reproducibility of our results. The validity of results should not be affected due to the small number of issues. 

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

