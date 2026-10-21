# Updates the NuGet packages used to build the deployable package by the DevOps pipeline

## Check the Platform and Application verisons for the environment

- Go to the LCS project page
- Open the environment details
- Check Platform release
- Check Application current version

##  Get the comppatible NuGet packages

- Go to the LCS root page
- Go to Shared asset library
- Go to Nuget packages
- Download the necessary "PUxx/10.0.xx - ..." packages acording to the Platform and Application versions you last checked

## Upload to DevOps Artifacts

- Put the downloaded files on a folder with the nuget.config and packages.config used on your pipeline
- Publish the packages with the command:

```
<NugGetPath>\nuget.exe push -Source <PipelineName> -ApiKey <Anything> "<FileLocalPatch>\<PackageFileName>"
```

- When asked for username and password, provide your email as username and a valid PAT for password
