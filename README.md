# XYZ

##What's XYZ?
XYZ is a simple tool to generate automatically **several** platform-dependent resource files from a **single** RESX file.

##Installation

###from the nuget package
* add the nuget package XYZ to your common project which contains the RESX file

###from the binaries
* downlaod the latest binaries here and unzip the content into your common project which contains the RESX file

##Resource Generation
* modify the Generate.sh and/or the Genearte.bat files under the *Localization* folder to target your resx file and the correct path for your iOS and Android projects
* execute the script

##Usage

XYZ.exe [-t] [-a] [-m] [-d] [-b]

Options: 
-t|target : ios or android (required)
-a|amp : common resx file (optional), if you have a resx file containnning default values etc. Those values will be overrided if they exist in the main resx file (see below)
-m|master : main resx file (required)
-d|destination : destination and file name to be genearetd (required)
-b|backup : backup file (optional)

Example:

`XYZ.exe -t=android -a="Common.resx" -m="MyApp.resx" -d="..\..\MyApp.Droid\Resources\Values\Strings.xml"` 
`XYZ.exe -t=ios -a="Common.resx" -m="MyApp.resx" -d="..\..\MyApp.iOS\en.lproj\Localizable.strings"`

##Know limitations

##But... it doesn't support XZY or it has a bug
Don't hesitate to create an [issue](https://github.com/apcurium/amp-tool/issues) or better, fork it and send us a pull request!