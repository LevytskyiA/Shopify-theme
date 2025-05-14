# Boiler Plate 

✅ \***\*This theme is connected to Shopify via Github.\*\***

## Setting up 👷🏿‍♀️

- Prerequisites:
  - GIT CLI or GIT GUI
    > [https://git-scm.com/downloads](https://git-scm.com/downloads)
  - Yarn CLI
    > [https://classic.yarnpkg.com/en/docs/install/#windows-stable](https://classic.yarnpkg.com/en/docs/install/#windows-stable)
  - Shopify CLI 3.0
    > [https://shopify.dev/themes/tools/cli](https://shopify.dev/themes/tools/cli)
- Setup your development branch:
  - Clone the GIT repo `git clone https://github.com/noticeddlv/<REPO NAME>`.
  - To checkout to your new branch, within the clickup ticket select the github relationship option and copy the branch name

  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_10.png?v=1683206839)

  - Once you checkout to the branch name then proceed to the next step
  - Push your local branch back up to the remote repository `git push -u origin <your branch name>`

- Connect your development branch to the development theme on Shopify:
  - Under themes, select add theme and choose connect from Github

  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_9.png?v=1683206839)

  - Find your repository and connect the branch that you just pushed in the previous step

## Repository Setup 📂

- **Prettier Setup**
  - Install the two extensions below in your code editor

   ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_8.png?v=1683206839)

  - Add your liquid prettier extension by adding it to the repo or globally (preferrably globally)
  ```jsx
  # with yarn
  yarn add --dev prettier @shopify/prettier-plugin-liquid
  ```
  - Once that is complete, Open the command palette (either with  or ++)
    Ctrl +Shift + P
  - Type *"open settings"*
  - You are presented with a few options¹, choose **Open User Settings (JSON)**

  ![https://i.stack.imgur.com/haQf1.png](https://i.stack.imgur.com/haQf1.png)

  - Once you have the settings.json file opened, copy these settings over
  ```
  "[javascript]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[json]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[html]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[css]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[scss]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "editor.formatOnSave": true,
    "[liquid]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode",
      "editor.formatOnSave": true
    },
  ```
  - This should now start formatting your code using prettier in all the primary file types

## Development 💻

- Run `yarn start` to start up the local server for development
- Once development is completed you can push your changes up to the branch which will automatically update the Shopify theme it is connected to. The general 3 step commands are as below:
  `git add .`
  `git commit -m "<change message>"`
  `git push`
- The next step will be creating the pull request to get it merged into the live theme/master branch.

## Pull requests 🤝🏼

- **Creating the pull request**
  - Visit the Github repository page under your branch
  - Select the “Open pull request” button

  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled.png?v=1683206218)
  - Fill out the details in the pull request template populated in the description
  
  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/pr-template.png?v=1683206425)

  - Assign a reviewer
  
  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_1.png?v=1683206588)

  
- **Testing & Issues**
  - The reviewer will follow the test steps inputted into the PR description
  - Any issues found during testing will be created as a github issue which will then be linked to the pull request.

  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_11.png?v=1683207284)
  - Once the issue is resolved, mark it as closed

  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_3.png?v=1683206839)
  - Any issues found during testing will be created as a github issue which will then be linked to the pull request.

## Merge into Master

- Pull Request Approval
  - Once the PR is tested and ready for the merge, select the Merge Pull Request button within the github PR.
  
  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_4.png?v=1683206839)

## Merge conflicts ❌

- When a merge conflict is present in the PR (usually due to master being updated), select the command line option and follow the steps.

  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_5.png?v=1683206839)
  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_6.png?v=1683206839)

## Roll Back

- If an issue occurs or is found after the pull request is merged
  - Visit the Github repository page under your merged pull request
  - Select the “Revert” button
  - Merge the pull request and that will roll you back to the state before the merged changes.
  - You will have to create a new pull request to merge the updated changes afterwards

  ![Untitled](https://cdn.shopify.com/s/files/1/0631/6199/1389/files/Untitled_7.png?v=1683206839)

## Closing the merged Branch

- Once the PR is merged successfully we will close the branch the next business day to reduce theme and branch clutter in the repo and Shopify environments

## Resources

- [https://yarnpkg.com/cli/install](https://yarnpkg.com/cli/install)
- [https://shopify.dev/apps/tools/cli](https://shopify.dev/apps/tools/cli)
- [https://git-scm.com/downloads](https://git-scm.com/downloads)
