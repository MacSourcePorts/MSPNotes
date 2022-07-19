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


Then make an alias to be able to fire off the Intel version easily. I go with the alias `ibrew` to tell the differences (the "i" is for Intel)

```
alias ibrew='arch --x86_64 /usr/local/Homebrew/bin/brew'
```

**If you are on an Intel Mac**

The first install command for Homebrew above will install the Intel version, but there is not a way to install the Apple Silicon version (that I know of). Most of the build scripts assume the Apple Silicon version of Homebrew is present. A workaround is to manually copy over the Apple Silicon version of the Homebrew directory from an Apple Silicon Mac but this still requires access to an Apple Silicon Mac. 