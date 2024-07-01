###Git Branch default Naming: main vs master

Since October 1, 2020, GitHub has set the default branch to "main" for new repositories, while many existing repositories still use "master". This change is part of an effort to use more inclusive language and avoid terms with negative historical connotations, opting for a more neutral term. "Main" is considered a better choice because it is short, easy to remember, and translates well across languages.
On the other hand, Git, the underlying version control system, is an open-source project maintained by a diverse community. Changes in Git require consensus from contributors and users to ensure broad agreement and compatibility across various workflows and tools. As of now, the default branch name in Git remains "master" because changing it involves a complex and slower process compared to a single platform like GitHub. While discussions about changing the default branch name in Git have occurred, reaching a consensus in open-source projects takes time.
As a result, many organizations and individuals have chosen to rename the default branch from "master" to "main" or some other neutral term. This change is not a requirement, but rather a choice made by individual users or organizations based on their values and preferences.
Upon investigating, I learned the previous exposure above and this experience highlighted the importance of staying informed about industry updates and platform-specific changes. It also underscored broader discussions in the tech community regarding terminology and inclusivity in software development practices.
Moving forward, adjusting to GitHub's default settings improved my project integration and enhanced my understanding of Git workflows. If you encountered similar challenges with Git, I will detail what I did to resolve the issue:
I renamed the local branch via the following line command:
git branch -m master main
I pushed the renamed branch to the remote repository:
git push -u origin main
In addiction, and because after the version git 2.28 we can set a global config with the default branch name allowing now and whenever we create a new git local repo using any default branch name, I run the following line command:
git config --global init.defaultBranch main
Here you go. From now on, the branch names in the local and remote repository are the same, preventing pushes and pulls from going to a different repository than expected.
