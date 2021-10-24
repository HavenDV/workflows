# Using
```yaml
name: Build, test and publish
on: [ push ]

jobs:
  build-test-publish:
    name: Build, test and publish
    uses: HavenDV/workflows/.github/workflows/dotnet_build-test-publish.yml@main
    secrets:
      nuget-key: ${{ secrets.NUGET_KEY }}
    with:
      files: |
        src/installers/UpworkPdfGenerator.Installers.Wpf.NetFramework/UpworkPdfGenerator.msi
```

# Explanation
## [Build, test and publish](.github/workflows/dotnet_build-test-publish.yml)
This workflow is for developing and releasing a NuGet package by a small number of people on the same branch.  
It is based on the [Conventional Commits specification](https://www.conventionalcommits.org/) and 
will only release new releases if they contain fix/feat/perf commit types.  
It automatically generates a build number (BUILD_NUMBER environment variable).  
It also automatically generates Package Release Notes based on the latest commits (PACKAGE_RELEASE_NOTES environment variable).  
Requires a nuget-key secret that will be able to load your NuGet packages.  

### Inputs
| name                                        | type    | default             |
|---------------------------------------------|---------|---------------------|
| dotnet-version                              | string  | '6.0.x'             |
| include-prerelease                          | boolean | true                |
| os                                          | string  | 'ubuntu-latest'     |
| fetch-depth                                 | number  | 50                  |
| conventional-commits-publish-conditions     | boolean | true                |
| build-with-msbuild                          | boolean | false               |
| vs-prerelease                               | boolean | true                |
| run-tests                                   | boolean | true                |
| files                                       | string  | ''                  |
   
### Secrets
| name                                        | type    | default             |
|---------------------------------------------|---------|---------------------|
| nuget-key                                   | string  | ''                  |

# Contacts
* [mail](mailto:havendv@gmail.com)
