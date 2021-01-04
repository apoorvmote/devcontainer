# AWS CDK

[![MIT License](https://badgen.now.sh/badge/License/MIT/blue)](https://github.com/apoorvmote/devcontainer/blob/master/License.md)

We start with Ubuntu 20.04

Then install [NodeJS LTS](https://nodejs.org/en/) for CDK, [Task](https://taskfile.dev/#/) for automating regular tasks like git commits, [golang](https://golang.org/dl/) for writing lambda function in go, aws cli v2 for accessing aws credentials. And npm install aws-cdk at the end. You can remove golang and task if you don't use it.

I am doing volume mount of ssh keys and aws credentials. If you don't use ssh keys then you can delete this part.

I use following plugins 

1. "dbaeumer.vscode-eslint": Eslint plugin for linting typescript
1. "sodatea.velocity": This is for VTL (velocity template language) used for graphql resolvers. You can remove it if you don't write custom VTL templates.
1. "wix.vscode-import-cost": This is fun one :partying_face:. It tells you the size of the package. It doesn't work 100% of the time and when it works then is not 100% accurate but its fun :tada:. This is irrelevant in CDK so feel free to remove it.
1. "steoates.autoimport": This will automatically import variables and packages. I would highly recommend you keep this one.
1. "streetsidesoftware.code-spell-checker": This checks for spelling mistake in code. This is almost as equally important as typescript type checking. I would highly recommend you keep this one.
1. "vscode-icons-team.vscode-icons": This is only for aesthetic reasons. It will choose file/folder icon based on name and extension. You can omit this one if you don't want.
1. "golang.go": This is for golang linting and error checking. If you don't use go then omit this one.
1. "kumar-harsh.graphql-for-vscode": This is again if you use graphql schema in cdk.  If you don't use graphql in cdk then omit this one.