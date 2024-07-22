# TestProject

This project was created as a proof of concept for the issue described here galasa-dev/projectmanagement#1926 .

With a limited knowledge of java/gradle my observations are as follows:-
1) Created a sample Java/Gradle project that just does a Hello World starting with the version 0.1.0-SNAPSHOT
2) Created a basic workflow that attempts to publish this project to the GitHub Packages Maven Registry

   I tried using `-dev` instead of `-SNAPSHOT` but the following builds with the same version number failed with a conflict error, while they were succesful with `-SNAPSHOT` tag
4) Created a second sample project in the same repository that has a dependency on the first project, but the version specified is 0.1.0 
5) Tested that the second project can find the first project as a dependency even without the suffix

   The second project failed to fetch the dependency with just 0.1.0 suffix, while it succeeded with `0.1.0-SNAPSHOT` and `0.1.0+` .

The succesful workflow run can be viewed [here](https://github.com/jaydee029/TestProject/actions/runs/10034907413)
