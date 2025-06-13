# OnionFruit™ Development Assets (for macOS)

## Overview
Running OnionFruit on macOS requires a helper service and some native libraries to control system settings and show some UI elements.
This project provides prebuilt copies of native libs/binaries for when a developer doesn't want to change native functionality and doesn't want to use Xcode to build the files.

### What's provided?

- `libonionfruit` - Native library that performs communication on behalf of the main application. It is **required** and should be copied to `./DragonFruit.OnionFruit.Core.MacOS/Native`
- `onionfruitd` - A launch daemon used in production binaries, don't use in development as it's restricted to official builds only
- ServiceLoader - Application used to load a development copy of `onionfruitd`, that can be used in OnionFruit debug builds

## Quick-Start
You'll need at least the ServiceLoader and `libonionfruit` to run a debug copy of OnionFruit. If changes are required to be made to either the library or daemon, they'll need to be modified and rebuilt from the Xcode project:

1. Download and install ServiceLoader to /Applications, follow setup process to install the service (you'll need to manually approve the installation, but you need to on the main app anyways).
2. Download and copy libonionfruit.dylib to `DragonFruit.OnionFruit.Core.MacOS/Native`.
