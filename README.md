# Lobotomy

Lobotomoy is an Android security toolkit that will automate different Android assessments and reverse engineering tasks.  The goal of the Lobotomy toolkit is to provide a console environment, which would allow a user to load their target Android APK once, then have all the necessary tools without needing to exit that environment.  Lobotomy leverages and provides wrappers around other popular tools such as **Androguard**, **apktool**, **Dex2Jar**, and **Frida**.  

## Features

- APK decompilation
- APK conversion with Dex2Jar
- Convert APK to a debuggable APK
- APK Profiler
- Enumerate attack surface:
  - Intent Filters
  - URL Schemes
  - Exported Components
- Enumerate application components:
  - Activities 
  - Broadcast Receivers
  - Services
  - Content Providers
- Enumerate application permissions
- Map permissions to API usage
- Bowser toolkit:
  - Enumerates methods: 
    - parseUri() 
    - loadUrl() 
    - addJavascriptInterface()
  - Triggers parseUri()
- Logcat wrapper
- Instrumentation with Frida
- Web UI and Services

## Installation

- Lobotomy was developed on Homebrew's Python 2.7.*, but should still work on other flavors of NIX.
- Building the apktool requires Java
-
### OS X

Download Hombrew:  

```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" ```

Download Python: 

```brew install python ```

Run Setup: 

```./setup.sh ```

## Issues 

Androguard's current MASTER seems to have internal broken import paths.  This unfortunately breaks the ability to use it within Lobotomy as the core functionality for loading an APK.  We have included the working build in this repository so that Lobotomy can still remain stable and will upate accordingly if any fix is identified.

