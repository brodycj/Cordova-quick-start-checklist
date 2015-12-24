# Cordova app quickstart checklist

LICENSE: CC0 (public domain) ref: http://creativecommons.org/publicdomain/zero/1.0/

Inspiration:
- [jessemonroy650 / top-phonegap-mistakes](https://github.com/jessemonroy650/top-phonegap-mistakes)
- [litehelpers / Cordova-sqlite-storage / issues](https://github.com/litehelpers/Cordova-sqlite-storage/issues)

FUTURE TBD:
- cover both `cordova` CLI and `phonegap` CLI *and test*
- Document the actual shell commands for the steps below

## Purpose

TBD

## Prerequisite(s)

- Cordova CLI installed
- Ability use the Cordova CLI to:
  - create an app (using the default template);
  - run it with no plugins;
  - run it on any desired target platform(s)

NOTE: These steps are very well documented (TBD add some links)

FUTURE TBD for consideration: add section to cover this

FUTURE TBD: how to add a new target platform

## Initial checklist

Outline:
- Ability to run on desired target platform(s) (new platforms may be added in the future)
- All desired target platform(s) are supported by all plugin(s) needed
- Verify that cordova-plugin-console is installed
- Verify ability to add a `console.log` statement to Javascript

## Add a simple plugin

Goal: ability to use Cordova CLI to add a plugin and get it working before dealing with complexity of plugins such as Cordova File API and/or sqlite

- Recommendation: start with a very simple plugin such as cordova-plugin-dialogs
- add to project
- add to `onDeviceReady` function in Javascript
- `cordova prepare` command
- test on all desired target platform(s)

## Adding sqlite plugin

- add to project
- add quick installation test code to the `onDeviceReady` function in Javascript
- verify that it works on all desired target platform(s)

## Whitelist/security

- DEFAULT: no external requests, no navigation outside `file://` URL(s), no external URL intents (such as opening maps)
- configure as documented at: https://github.com/apache/cordova-plugin-whitelist
- intent whitelist (as documented at: https://github.com/apache/cordova-plugin-whitelist)
- IMPORTANT: Content Security Policy (as documented at: https://github.com/apache/cordova-plugin-whitelist)

