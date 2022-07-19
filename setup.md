# General Development Setup

## Assumptions

These instructions, and to some extent the build scripts for each project, assume you are on an Apple Silicon Mac and you are doing work to set up a system to compile for both Apple Silicon and Intel. In some or all cases it may be possible to do the opposite (compile for both from an Intel platform) but it may be more difficult.

## Xcode
Install Xcode from the [App Store](https://apps.apple.com/us/app/xcode/id497799835?mt=12). 

## Homebrew
On an Apple Silicon machine, Homebrew must be installed twice, once for Apple Silicon and once for Intel. The Homebrew developers have designed with this in mind. 

Homebrew for Apple Silicon puts everything in 

```
/usr/local
```

Homebrew for Intel puts everything in 

```
/opt/Homebrew/
```

**If you are on an Apple Silicon Mac (preferred)**:

Install Homebrew with the following command

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Then fire off the two commands it instructs you to in order to add Homebrew to `PATH`

```
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/(username)/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

Then install a second time for Intel. 

```
arch --x86_64 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```


Then make an alias to be able to fire off the Intel version easily. I go with the alias `ibrew` to tell the differences (the "i" is for Intel). Edit `~/.zshrc` in `vi` to include:

```
alias ibrew='arch --x86_64 /usr/local/Homebrew/bin/brew'
```

**If you are on an Intel Mac**

The first install command for Homebrew above will install the Intel version, but there is not a way to install the Apple Silicon version (that I know of). Most of the build scripts assume the Apple Silicon version of Homebrew is present. A workaround is to manually copy over the Apple Silicon version of the Homebrew directory from an Apple Silicon Mac but this still requires access to an Apple Silicon Mac. 

## Install Homebrew dependencies

These are the ones we need in several places

```
brew install dylibbundler pkg-config
```

## Clone MSPScripts

The [MSPScripts repo](https://github.com/MacSourcePorts/MSPScripts) has all of the scripts we use to build apps, sign, notarize, etc. 

It needs to be cloned into a directory named `MSPScripts` which is parallel to other repos (i.e., `vkQuake`, etc.)

It also needs a file called `signing_values.local`. A template of the contents of this file is in the comments of `sign_and_notarize.sh` but the file itself is excluded from source control for security reasons. The values must match the certificate.

## Import certificate

The easiest way to do this is to export a Certificate/Private Key pair from a working Mac. The one we're looking for is the "Developer ID Application" one. Once you import it on the new system correctly it will display as a certificate/key pair under "My Certificates" in "Keychain Access

Note that it is not enough to just download the certificate from the Apple Developer site, it won't come with the private key that way and the process of redoing that is complicated.

## Set up application specific password. 

Set up an application password in Keychain Access. Currently I'm using the one named `notarize-app` and it's setup is on the [Apple ID](https://appleid.apple.com/account/manage) site as an App-Specific Password (the "app" in this case is our notarization process)

## Reset Xcode

For whatever reason, `altool`, the thing we currently use to notarize apps doesn't get found until we run 

```
xcode-select -r
```
So do that

## On first run

On first run of a full build or notarize you should be prompted by the process to allow `codesign` to use the certificate in Keychain Access and, for notarization, to allow `altool` to use the `notarize-app` password. This is notmal, and you should choose "Always Allow" to streamline it in the future. 