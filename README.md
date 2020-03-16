# Yarn v2 Nested Workspaces/Worktree Example

#### The basics covered in this example are nested Worktrees and Workspaces where one of the nested Workspaces is dependent on a top level Workspace (a common library used amongst many Workspaces)

### Requirements

- Yarn v1 (globally installed)
    - Check to make sure by entering `yarn -v` in a directory outside of this project in your command line
    - Inside this project the result of `yarn -v` should result in something like _2.0.0-rc.30_

### Things to Note

- You can test to make sure everything is working by running the following command from anywhere in the project directory: <br /> <br />
  `yarn workspace @workspaces/dashboard-client start`

  - ⚠️ If you try to run the command `node dashboard/client/index.js` from the root directory it will say it was unable to find the _@workspaces/common_ package because node by itself doesn't know how to resolve the `workspace:` protocol in the package.json. You must use `yarn` to run your package

- Yarn v2 is utilized via __.yarnrc.yml__ file

- The root __package.json__ doesn't need to identify each nested Workspace. Instead you can list the Worktree that those nested Workspaces are contained in, and it will know about the nested Workspaces through the `"workspaces"` property in the Worktree package.json like __dashboard/package.json__

##### Please let me know if this was helpful for you 🙏
