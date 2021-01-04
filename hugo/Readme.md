# Hugo

[![MIT License](https://badgen.now.sh/badge/License/MIT/blue)](https://github.com/apoorvmote/devcontainer/blob/master/License.md)

We start with Ubuntu 20.04

Then install [NodeJS LTS](https://nodejs.org/en/) for CDK, [Task](https://taskfile.dev/#/) for automating regular tasks like git commits, [golang](https://golang.org/dl/) because Hugo is written in golang so to test some go native features, aws cli v2 for accessing aws credentials. And lastly hugo extended version. You can remove golang and task if you don't use it.

I am doing volume mount of ssh keys, aws credentials and local time zone. By default containers do not set system time but use UTC time instead. Hugo creates new posts based on system time. So local time zone is very important. If you don't use ssh keys then you can delete this part.

I use following plugins 

1. "streetsidesoftware.code-spell-checker": This checks for spelling mistake in code. This is almost as equally important as typescript type checking. I would highly recommend you keep this one.
1. "naumovs.color-highlight" & "anseki.vscode-color": these are color plugins for css and scss. The default vscode is also pretty good but this does it better. These are optional.
1. "budparr.language-hugo-vscode": Hugo specific snippets. It does pretty descent job. You can also manually type it and skip this plugin. 
1. "kisstkondoros.vscode-gutter-preview": Shows very small image preview right in the gutter with any image url in the code. Its optional.
1. "vscode-icons-team.vscode-icons": This is only for aesthetic reasons. It will choose file/folder icon based on name and extension. You can omit this one if you don't want.
1. "ritwickdey.liveserver": Allows you to serve static files over localhost with single click. So if you want to see hugo website after building then you can test with live server.
1. "golang.go": This is for golang linting and error checking. If you don't use go then omit this one.
1. "davidanson.vscode-markdownlint": Linting for markdown. If you write lots of markdown then I would highly recommend you keep this one.