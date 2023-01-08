0. Preface

Thank you for your contribution to TuGraph. We sincerely hope that more students from the community will join in and build a better graph database project together.

Before contributing code, please take a little time to understand the process of contributing code to TuGraph, and read the "Contributor License Agreement". Participating in the contribution is deemed to agree to the above agreement.

Individual Contributor License Agreement: [6.individual_cla.md]

Corporate Contributor License Agreement: [7.corporate_cla.md]

1. What to contribute

We always welcome any contribution, be it simple typo fixes, bug fixes or new features. Feel free to ask questions or make PRs. We also value documentation and integration with other open source projects and welcome contributions in this regard. For any modification, especially the more complex modification, it is recommended to create an issue and fill it out according to the BUG or PR template.

2. Preparations

Before contributing code, you need to understand the use of git tools and the use of the GitHub website.

3. Contribution code process

3.1 Submit an issue

Whether you're fixing a bug in TuGraph or adding a feature to TuGraph, before you commit to code, file an issue on TuGraph's GitHub describing the problem you want to fix or the feature you want to add. Doing so has several benefits:

No duplication of effort due to conflicts with other developers or their plans for the project.
The maintainers of TuGraph will discuss the bugs or new features you raised to determine whether the modification is necessary, whether there is room for improvement or a better way.
After reaching an agreement, develop and submit the code, which reduces the cost of communication between the two parties and also reduces the rejection of pull requests.
3.2 Get the source code

To modify or add new features, after raising an issue, fork a copy of TuGraph Master code to your code repository.

3.3 Pull branch

All modifications of TuGraph are made on the branch. After the modification, a pull request is submitted, and the project maintainer Merge to the Master after the Code Review. So, after getting the source code steps explained, you need to:

Download the code locally. You can choose the git/https method in this step. In recent years, the permission requirements of github have become stricter. For example, the git method requires a more complex ssh key (https://docs.github.com/en/authentication/connecting-to -github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent), https method cannot directly use username and password authentication, please follow the guidelines for authorization. git clone https://github.com/your account name/tugraph-db
Pull the branch to modify the code: git branch add_xxx_feature
After executing the above command, your code repository will switch to the corresponding branch. Execute the following command to see your current branch: git branch -a
If you want to switch back to Master, execute the following command: git checkout -b master
If you want to switch back to the branch, execute the following command: git checkout -b "branchName"
3.4 Configure Github information

Execute git config --list on your machine to view git's global username and email. Check if the displayed user.name and user.email match your github username and email.

If the company has its own gitlab or uses other commercial gitlab, there may be a mismatch. At this time, you need to set the username and email address separately for the tugraph-db project. Please refer to the official github documentation for how to set the username and email address.

3.4 Submit the modified code to the local

After pulling the branch, you can modify the code.

**Notes on modifying the code **

The code format is consistent: TuGraph uses cpplint to keep the code format consistent, and the IDE can configure the style through .clang. Before submitting the code, be sure to check the code style locally, otherwise ACI will report an error.

Supplementary unit test code: new changes should pass existing unit tests. New unit tests should be provided to prove that the previous code has bugs, and the new code has resolved these bugs. You can run all tests with the following command: ./unit_test It can also be run through an IDE.

**Other Notes**

Please keep the original format of the code you edited, especially whitespace wrapping etc. For useless comments, please delete them directly. Add comments where logic and functionality are not easily understood. Keep documentation up to date. After modifying the code, please execute the command in the following format to submit all the changes to the local: git commit -am '(feat) add xx function' git commit -am '(fix) fix xx problem'`

3.4 Submit the code to the remote repository

After the code is submitted to the local, the next step is to synchronize the code with the remote repository. Execute the following command to submit local changes to github: git push origin "branchname"

If you did it by fork, the origin here is push to your repository, not TuGraph's repository.

Submit a request to merge code to Master After your code is submitted to GitHub, you can send a request to merge your modified code into the TuGraph Master code. At this point, you need to enter your corresponding repository on GitHub and press the pull request button in the upper right corner. Select the target branch, usually master, the system will notify the TuGraph staff, and the TuGraph staff will review your code. After meeting the requirements, it will be merged into the trunk and become a part of TuGraph.

3.5 Code Review

After you submit the code, your code will be assigned to the maintainer for Review, please be patient. If after two working days, there is still no response to your submission, you can leave a message under the PR and @ the corresponding person.

Comments on the code review will be directly remarked to the corresponding PR or Issue. If you think the suggestions are reasonable, please also update these suggestions to your code.

3.6 Merge code to Master

After the code review is passed, it will be merged into the master by the TuGraph maintainer. During this process, the maintainer may designate a new reviewer, and put forward new comments that need to be modified. Generally, you do not need to participate in this step. After the code is merged, you will receive a prompt that the merge is successful.