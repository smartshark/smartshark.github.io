---
layout: page
title: MSR2020 Registered Report
permalink: /msr20_registered_report/
---

Thank you for your interest in the participation in our study on the manual labeling
of bug fixing lines that is [registered with the OSF](https://osf.io/acnwk) and part
of the MSR 2020 registered reports track. 

Our goal is to provide a large corpus of bug fixing commits, where we know for each
changed line whether it contributed to the bugfix or not. You can watch this short
video on YouTube to see how the validation works. 

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/VWvDlq4lQC0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

If you are interested in participating, please first read the [registration protocol 
at the OSF](https://osf.io/acnwk). If you contribute manual validations for at least 200 commits, you can
become a co-author of the resulting manuscript, which already as an In Principle
Acceptance (IPA) for publication in the
[Empirical Software Engineering](https://www.springer.com/journal/10664) journal. 


Please fill in the following form and send it via Email to herbold@cs.uni-goettingen.de.
We need the full form including the consent statement and the information regarding data
privacy due to the GDPR. We will than contact you with all information regarding how to proceed. 

```
Registration Form

Contact Details

Name:
Email: 
Experience: 
Desired pseudonym: 

With the submission of this form via Email to herbold@cs.uni-goettingen.de you
give your consent for the storage and handling of your personal data as described below. 

Information regarding required data and data privacy:

Please use an official university or company address if possible, or any other address
that we can use to validate your identity. If this is not possible, we will try to work
out a different way to confirm your identity.

Please indicate your experience such that we can see if you meet one the following
criteria: “1) an under-graduate degree majoring in computer science or a closely related
subject; or 2) at least one year of programming experience in Java, demonstrated either
by industrial programming experience using Java or through contributions to Java open
source projects.” In case you contributed to open source projects, please provide links. 

The pseudonym will be the name of your account and cannot be changed afterwards. The 
pseudonym is also used to identify which lines you labeled and how you labelled them. 
The pseudonym will become part of the publicly shared data set. If you select the
pseudonym such that it may be used to identify yourself (e.g., sherbold), we
see this as consent for sharing this pseudonym publicly within the data set as described above. 
In case you do not provide a pseudonym, we will generate a random pseudonym for you which 
will provide you anonymity in the data set. We note that it may be possible to
de-anonymize the pseudonyms in case you become a co-author of the manuscript, because 
the author order depends on the labeled data. 

This form will be stored encrypted and is only accessible by Steffen Herbold. The form will
be deleted upon acceptance of the manuscript that describes our study. Your email address
and pseudonym will be shared with Alexander Trautsch and only be used by him to send you the
credentials for the data labeling platform. Steffen Herbold may also contact you via your
Email address with information relevant for the study, e.g., the current progress, or in case
you meet the criteria for authorship and are invited to contribute to the manuscript. 
```

**Deviations from the Registration:**

- The timeframe of the public labeling period is changed to May 18th-September 31st due to the move of MSR, ICSE, and the ongoing pandemic. 

**FAQ**

**Q:** In the tutorial video, you simple label all lines in a test file as test. What if there are documentation lines or whitespaces in such files. Should we label this or is simply labeling everything as test sufficient?

**A:** Simply labeling everything as test is sufficient, because our focus is on bug fixes. For this data, recognizing that a file is part of the tests is important, now whether the lines are whitespaces or documentations. We will count all lines in test files positively for your consensus, unless there is strong reason not to, e.g., because you labelled the test changes as bugfix. 

**Q:** For some issues, I only see changes to tests. The discussion says that the bug was already fixed earlier and that only tests were added to confirm this. What should I do?

**A:** This is okay, just label the tests and tests and you have an easy commit. The issue is correctly labeled as bug, because the bug was in the software in the prior release. The link is also correct, because the developers confirmed that the bug was fixed. There just is nothing to fix anymore. You also do not have to search for the actual bug fixing commit. This will actually lead to interesting data. 

**Q:** What if a line contributes both to the bugfix and contains an unrelated improvement or comment?

**A:** You should label the line as bugfix, because this is the more important label. Labeling on the character level is out of scope of our study. While this may mean there there is some noise in our data, this noise should be very low and also irrelavant for many applications. 

**Q:** Why can I not skip issues, e.g., if I find them too difficult?

**A:** Because this would lead to multiple problems and is not allowed according to our registered study design, that states that the commits we are showing you are randomly sampled from the project you selected. We decided for this for two reasons. First, skipping issues could reduce the validity of the results for our second research question, i.e., how good we actually are at labeling bugfixes at this level of granularity, because the sample could be skewed towards simpler bugfixes. Second, this could lead to cherry picking, i.e., participants who skip commits until they find particularly easy commits. This would be unfair for the other participants. 

**Q:** Help! I am stuck labelling because the editor does not allow me to mark all files. What can I do?

**A:** Nobody is perfect, and our system is certainly not perfect as well. Please contact us via Email, or create a GitHub issue with the description. We are currently aware of one very annoying issue that seems to affect very few commits, but was now reported twice. In case only the last line of a file was deleted, but not the second to last line, it can happen that this line cannot be marked and labelled. If all lines from the file are, e.g., unrelated, test, or bugfix, this is not a big issues: you can use the buttons on top of the file to assign the same labels to all lines. If you need multiple labels for the file, please contact us. 

**Known Issues with the Data:**

- The commit 1f62431ebcbc1fb9654151c999349bf0204c465c is unrelated to the issue VALIDATOR-276, even though this is explicitly linked through the commit message.
- The commit e883181ff49d3fa76853e88d4eae1633e0cc383d is unrelated to the issue LANG-100. This was a false positive for SZZ that was not corrected through our manual validation.
