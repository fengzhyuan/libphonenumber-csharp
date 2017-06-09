
# Overview

# Note for this version
Modified the `csharp/PhoneNumbers.sln` to make it compatible on .Net 4.0 plateform;

removed `PhoneNumbers.Test` from solution; 

Use 3rd party lib `ReadOnlyCollectionsExtensions`, `ReadOnlyCollectionsInterfaces`, available via NuGet (in `csharp/packages`
Or the compiled DLL can be used directly at `lib/PhoneNumbers.dll` with namespace `PhoneNumbers`, built with VS 2010 (Version 10.0.40219.1 SP1)

Please refer original WIKI for more information.

# Original README -->

# libphonenumber-csharp
Clone of original C# port [here](https://bitbucket.org/pmezard/libphonenumber-csharp/wiki/Home).

All I've ever done is pull updated metadata from Google's project.

# From the original WIKI
## Conversion Notes

C# port of Google's [libphonenumber library](https://github.com/googlei18n/libphonenumber).

  The code was rewritten from the Java source mostly unchanged, please refer to the original documentation for sample code and API documentation.

  The original Apache License 2.0 was preserved.

  See [this](https://github.com/aidanbebbington/libphonenumber-csharp/blob/master/csharp/README.txt "csharp/README.txt") for details about the port.

## Features

  * Parsing/formatting/validating phone numbers for all countries/regions of the world.
  * GetNumberType - gets the type of the number based on the number itself; able to distinguish Fixed-line, Mobile, Toll-free, Premium Rate, Shared Cost, VoIP and Personal Numbers (whenever feasible).
  * IsNumberMatch - gets a confidence level on whether two numbers could be the same.
  * GetExampleNumber/GetExampleNumberByType - provides valid example numbers for 218 countries/regions, with the option of specifying which type of example phone number is needed.
  * IsPossibleNumber - quickly guessing whether a number is a possible phonenumber by using only the length information, much faster than a full validation.
  * AsYouTypeFormatter - formats phone numbers on-the-fly when users enter each digit.
  * FindNumbers - finds numbers in text input 

## HowTo Update

  * checkout the latest release from https://github.com/googlei18n/libphonenumber/releases
  * synchronize all contained folders with this repository
  * copy PhoneNumberMetaDataForTesting.xml PhoneNumberMetaData.xml PhoneNumberAlternateFormats.xml from /resources to /csharp/PhoneNumbers
  * optional run /csharp/lib/makeprotobuf.bat
  * modify AssemblyVersion and AssemblyFileVersion in /csharp/PhoneNumbers/Properties/AssemblyInfo.cs and /csharp/PhoneNumbers.Test/Properties/AssemblyInfo.cs
  * make /csharp/PhoneNumbers.sln

## ToDo

7.7.4 changes the organization of metadata https://groups.google.com/forum/#!topic/libphonenumber-discuss/GlS11RdyocQ
This should be checked.

Available on NuGet as package [`libphonenumber-csharp`](https://www.nuget.org/packages/libphonenumber-csharp).

