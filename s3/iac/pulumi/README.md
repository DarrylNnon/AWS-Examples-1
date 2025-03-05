# pulumi is an infrastructure as code

# installation

```sh
curl -fsSL https://get.pulumi.com | sh
```

# rerun bash profile by  adding /home/gitpod/.pulumi/bin to my path

It looks like Pulumi was installed successfully, but your system can't find it because the installation directory /home/gitpod/.pulumi/bin is not in your PATH. Try these steps:

- Step 1: Manually Add Pulumi to Your PATH
Run the following command to add Pulumi’s bin directory to your PATH temporarily:

```sh
export PATH=$PATH:/home/gitpod/.pulumi/bin
pulumi version

permamemtly add pulumi to PATH
echo 'export PATH=$PATH:/home/gitpod/.pulumi/bin' >> ~/.bashrc

reload the shell
source ~/.bashrc
pulumi
```

Step i follow :
- pulumi new aws-python --force # for the environment
- create a pulumi token
- project name # s3-simple-sdk
- project description # a python for create a simple s3 project
- stack name : dev (default one)
- aws region: us-east-1 (default)
- the installation of depencies will start
- pulumi up
- click on the link to visualise it
- destroy your  bucket resource: pulumi destroy -s DarrylNnon/s3-simple-sdk/dev
- delete the entire stack: pulumi stack rm DarrylNnon/s3-simple-sdk/dev