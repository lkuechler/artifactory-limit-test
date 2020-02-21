# artifactory-limit-test

This repository is intended to reproduce a bug where only the last 100 releases of a repository are visible inside the github artifactory.

For this bug to appear it does not matter if these releases are a major, minor or patch version jump.

If you look at the releases on the github overview you can see all releases. Version 1.0.0 to 105.0.0.
https://github.com/lkuechler/artifactory-limit-test/packages/133740/versions

But if you get the releases with npm or yarn you will get the last 100 versions. Version 6.0.0 to 105.0.0.
`npm info @lkuechler/artifactory-limit-test versions`

The versions 1.0.0 to 5.0.0 can not be reached anymore. They can also not be installed when they are mentioned in a package.json