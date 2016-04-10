# iOS_resign_scripts
Scripts for resign iOS App (With Framework and dylib included). Only works on Mac OS X

## Requirement

Xcode command line tool

## Usage

* ios_resign_from_app_to_ipa

Assume folder app-extracted is the folder that created by running `unzip app.ipa -d app-extracted`
```
$ ls app-extracted
META-INF             Payload              iTunesArtwork        iTunesMetadata.plist
```

Then it should be use like below:
```
$ ios_resign_from_app_to_ipa app-extracted $Developer_code_sign $mobileprovision $target_ipa_related_path
```

example:
```
$ ios_resign_from_app_to_ipa app-extracted "iPhone Developer: hengjie chen (XXXXXXXX)" embedded.mobileprovision Testerhome-resigned.ipa
```

* ios_resign_with_app

Usage:
```
$ ios_resign_with_app $source_app_file $Developer_code_sign $mobileprovision $target_app_related_path
```

Example:
```
$ ios_resign_with_app Testerhome.app "iPhone Developer: hengjie chen (XXXXXXXX)" embedded.mobileprovision Testerhome-resigned.app
```

* ios_resign_with_ipa

Usage:
```
$ ios_resign_with_ipa $source_ipa_file $Developer_code_sign $mobileprovision $target_app_related_path
```

Example:
```
$ ios_resign_with_ipa Testerhome.ipa "iPhone Developer: hengjie chen (XXXXXXXX)" embedded.mobileprovision Testerhome-resigned.ipa
```

# Thanks

Thanks http://www.xgiovio.com/blog-photos-videos-other/blog/resign-your-ios-ipa-frameworks-and-plugins-included/ . I created these scripts beyond it.
