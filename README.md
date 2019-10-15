<p align="center">
  <img src="nugit-logo.png">
</p>

<p align="center">
  <img src="https://img.shields.io/github/issues/c272/nugit">
  <img src="https://img.shields.io/badge/status-active-green">
  <img src="https://img.shields.io/github/forks/c272/nugit">
</p>

<i align="center">
   A community curated NuGet source, available through GitHub.
</i>

## Introduction
This repository contains the source for the NuGit package feed, a mirror for user requested packages from [the official NuGet Gallery.](nuget.org) To add this as a source for a Visual Studio version, add the following URL to the NuGet sources under "Manage NuGet Packages".

```
https://c272.org/nugit/v3/
```

This will then give you access to all the currently mirrored content available through NuGit. If you wish to contribute, you can read the guide below for more details.

## Contributing
To contribute to NuGit, you will need the [Sleet](https://github.com/emgarten/Sleet) NuGet feed management tool, which will allow you to update, delete and add packages to the repository's main source. You can get a pre-built executable from NuGet, [here.](https://www.nuget.org/packages/Sleet/)

Once this is installed and added to PATH, you can clone the repository and add your requested NuGet packages to the `/docs/packages` folder, in the `.nupkg` format. More information on packaging your own projects in the NuGet package format is available [on the Microsoft docs.](https://docs.microsoft.com/en-us/nuget/create-packages/creating-a-package)

If you're on Windows, you can then run `update.bat` from the main repository location to update the package list. Otherwise, you can run `sleet push ./packages --source NuGit --config ../sleet.json --force` from the `/docs` directory.

Once this is done, simply pull request into this repository, and the package will be reviewed and added within a couple of days.
