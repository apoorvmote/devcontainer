# React or NextJS

[![MIT License](https://badgen.now.sh/badge/License/MIT/blue)](https://github.com/apoorvmote/devcontainer/blob/master/License.md)

We start with Ubuntu 20.04

Then install [NodeJS LTS](https://nodejs.org/en/) for react, [Task](https://taskfile.dev/#/) for automating regular tasks like git commits, aws cli v2 for accessing aws credentials. You can remove task if you don't use it.

I am doing volume mount of ssh keys and aws credentials. If you don't use ssh keys then you can delete this part.

I use following plugins 

1. "dbaeumer.vscode-eslint": Eslint plugin for linting typescript
1. "wix.vscode-import-cost": This tells you the size of the package. It doesn't work 100% of the time and when it works then is not 100% accurate but its fun :tada:. This is optional.
1. "steoates.autoimport": This will automatically import variables and packages. I would highly recommend you keep this one.
1. "streetsidesoftware.code-spell-checker": This checks for spelling mistake in code. This is almost as equally important as typescript type checking. I would highly recommend you keep this one.
1. "vscode-icons-team.vscode-icons": This is only for aesthetic reasons. It will choose file/folder icon based on name and extension. You can omit this one if you don't want.
1. "blanu.vscode-styled-jsx": This is not maintained plugin for styled-jsx but its still the most popular version. Its optional.
1. "naumovs.color-highlight" & "anseki.vscode-color": these are color plugins for css and scss. The default vscode is also pretty good but this does it better. These are optional.
1. "kumar-harsh.graphql-for-vscode": This is again if you use graphql schema.  If you don't use graphql then omit this one.