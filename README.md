# Lockdown Privacy (iOS)

Lockdown is an open source firewall that blocks trackers, ads, and badware in all apps. Product details at [lockdownprivacy.com](https://lockdownprivacy.com).

### Feature Requests + Bugs

Create an issue on Github for feature requests and bug reports.

### Openly Operated

Lockdown achieves the highest level of transparency for both client and server via the Openly Operated standard. It has also been audited multiple times, the latest audit in July 2020. See the full reports here: [Audit Kits](https://openlyoperated.org/report/confirmedvpn)

### Contributing

Pull requests are welcome - please document any changes and potential bugs.

### Build Instructions

1. `pod install`***

2. `carthage update --no-use-binaries --platform iOS` or for XCode 12 `./wcarthage update --no-use-binaries --platform iOS` (workaround for [this Carthage issue](https://github.com/Carthage/Carthage/issues/3019)) 

3. Open `LockdowniOS.xcworkspace`

To sign the app for devices, you will need an Apple Developer account.

-------------------

***Note (1)***: When running `pod install` if you receive a error relating to `cocoapods-acknowledgements`, try the following:

1. Install rbenv
```zsh
brew install rbenv
echo 'eval "$(rbenv init -)"' >> ~/.zshrc
source ~/.zshrc
```

2. Install & set ruby version == 2.7.3
```zsh
rbenv install 2.7.3

# Make sure you are in the correct directory!!
cd Lockdown-iOS/

rbenv local 2.7.3 
```

3. Restart terminal & verify ruby version
```zsh
# This should output 2.7.3
ruby -v
```

4. Install `cocoapods` and `cocoapods-acknowledgements`; *not* with *sudo* or *homebrew*.
```zsh
gem install cocoapods cocoapods-acknowledgements
```

5. Restart terminal & try installing again:
```zsh
pod install
```

***Note (2)***: When running the `carthage` command, and you recieve a *Task failed with exit code 65* (or a different error), try using the carthage.sh script I've included.

1. Run script
```zsh
sh carthage.sh update --no-use-binaries --platform iOS
```

-------------------

### Limitations to Building Locally

If you build Lockdown locally, you will not be able to access Secure Tunnel, because that requires a Production app store receipt. We will soon enable a DEV environment for Secure Tunnel with limited capacity and regions, designed only for testing.

To use Secure Tunnel, you must download Lockdown from the [App Store](https://lockdownprivacy.com).

### Contact

[team@lockdownprivacy.com](mailto:team@lockdownprivacy.com)

### License

This project is licensed under the GPL License - see the [LICENSE.md](LICENSE.md) file for details.



