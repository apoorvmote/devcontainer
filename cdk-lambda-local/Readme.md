# Invoke CDK lambda inside docker

So this dev environment is for running docker inside docker and settings for installing homebrew inside docker.

If you are deploying lambda via CDK and you want to test lambda locally before deploying then you need this setup.

Currently SAM Cli can only be installed with homebrew so we are forced to install homebrew but the alternative method for install is coming soon. I will update this repo then.

To install SAM Cli type 

```bash
brew tap aws/tap
brew install aws-sam-cli
```

After install check `sam --version`

If it says sam not found then do install again `brew install aws-sam-cli` and check `sam --version`. Works after 2 install.