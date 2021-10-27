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
      asset-path1: src/installers/UpworkPdfGenerator.Installers.Wpf.NetFramework/UpworkPdfGenerator.msi
      asset-name1: UpworkPdfGenerator.msi
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
| os                                          | string  | 'ubuntu-latest'     |
| dotnet-version                              | string  | '6.0.x'             |
| additional-dotnet-version                   | string  | ''                  |
| include-prerelease                          | boolean | true                |
| workloads                                   | string  | ''                  |
| windows-sdk-version                         | string  | ''                  |
| generate-build-number                       | boolean | true                |
| fetch-depth                                 | number  | 50                  |
| conventional-commits-publish-conditions     | boolean | true                |
| project-path                                | string  | ''                  |
| configuration                               | string  | 'Release'           |
| use-msbuild                                 | boolean | false               |
| vs-prerelease                               | boolean | true                |
| run-tests                                   | boolean | true                |
| asset-path1                                 | string  | ''                  |
| asset-path2                                 | string  | ''                  |
| asset-path3                                 | string  | ''                  |
| asset-name1                                 | string  | ''                  |
| asset-name2                                 | string  | ''                  |
| asset-name3                                 | string  | ''                  |
| asset-content-type1                         | string  | 'application/x-msi' |
| asset-content-type2                         | string  | 'application/x-msi' |
| asset-content-type3                         | string  | 'application/x-msi' |
| deploy-web-assembly-path                    | string  | ''                  |
| deploy-web-assembly-repo                    | string  | ''                  |
   
### Secrets
| name                                        | type    | default             |
|---------------------------------------------|---------|---------------------|
| nuget-key                                   | string  | ''                  |
| personal-token                              | string  | ''                  |

# Contacts
* [mail](mailto:havendv@gmail.com)
