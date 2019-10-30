## Bug Bounty Tips

**Tip #1**

Use GIT as a recon tool. Find the target's GIT repositories, clone them, and then check the logs for information on the team not necessarily in the source code. Say the target is Reddit and I want to see which developers work on certain projects.

[Link](https://gist.github.com/EdOverflow/a9aad69a690d97a8da20cd4194ca6596 )

**Tip #2**

Look for GitLab instances on targets or belonging to the target. When you stumble across the GitLab login panel, navigate to `/explore`. Misconfigured instances do not require authentication to view the internal projects. Once you get in, use the search function to find passwords, keys, etc. This is a pretty big attack vector and I am finally revealing it today, because I am sure it will help a lot of you get some critical issues.

**Tip #3**


Bug bounty tip: test applications of a company that costs money or requires manual setup. Chances are only few to none would have tested it leaving it vulnerable. 

**Tip #4**

If you’ve found an IDOR where you’re able to change data of others then don’t jump out of your seat to report it > modify it to XSS payload & if inputs are not sanitized & variables are echo’d without getting escaped then IDOR>XSS>ATO.


**Tip #5**

Look for *hackathon-related* assets. What I mean by this is sometimes companies run hackathons and give attendees special access to certain API endpoints and/or temporary credentials. I have found GIT instances that were set up for Hackathons full of information that allowed me to find more issues in the target several times.



**Tip #6**

Keep all your directory brute force results so when a CVE like Drupalgeddon2 comes out, you can look for previously found instances (cat dirsearch/reports/*/* | grep INSTALL.mysql.txt | grep 200 | less)/



**Tip #7**

When you have a form, always try to change the request method from POST to GET in order to improve the CVSS score.
For example, demonstrating a CSRF can be exploited simply by using \[img\] tag is better than having to send a link to the victim.
