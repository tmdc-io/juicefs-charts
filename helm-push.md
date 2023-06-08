# Steps to package and push Helm Chart to AWS ECR

## Automated Steps

Run ```sh make git-push ``` from root directory.

It will automatically trigger the the github action pipeline with automated versioning.

**NOTE:** If you want to update **CHART VERSION** of helm chart, please updated the ```sh VERSION ``` variable manually 
in release.yaml file (don't touch the suffix(-d..)it will be automatically taken care by script).
```sh
VERSION=0.14.2-d2
```


## Manual Steps
Once you are ready with your changes in charts - 

Run **git tag** command from root directory

First, please check the previous tag and use the incremental version of that.
Create git tag in local

```shell
git tag 0.14.2-d2
```
Push the tag to the remote repo

```shell
git push origin 0.14.2-d2
```
It will trigger the **TMDC Helm chart push workflow to AWS ECR** github action pipeline.
**juicefs-csi-driver** helm chart will be created with the **TAG** pushed to github and same will be pushed to AWS ECR

**NOTE:** Always maintain the semantic version (major.minor.patch) fixed and provide a suffix **-d** with it.
Tag will be incremental like ```shell major.minor.patch-d(+1 increment)```

ex ```shell 0.14.2-d1, 0.14.2-d2, 0.14.2-d3 ... ``` like that

We can update and push the **major.minor.patch** section of the tag once there in a release with official repo with same major/minor/patch version and also if we merge the changes to our repo.

ex: Lets say 0.14.3 or 0.15.1 version released . Once changes have been merged to our repo we will use tag 0.14.3-d(+1) or 0.15.1-d(+1).

**Please update the 'version' in Chart.yaml once there is a change in major/minor/patch version**