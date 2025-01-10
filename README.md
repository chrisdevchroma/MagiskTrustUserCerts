# Magisk Trust User Certs
This module makes all installed user certificates part of the system certificate store, so that they will automatically be used when building the trust chain. This module makes it unnecessary to add the network_security_config property to an application's manifest.

### Installation
1. Install [Magisk](https://github.com/topjohnwu/Magisk)
2. Zip files `pushd AlwaysTrustUserCerts; zip -r AlwaysTrustUserCerts.zip ./*; popd`
3. Install in Magisk (or flash through TWRP)
4. Install client certificates through settings->security
5. Restart your device. Certificate copying happens during boot.
6. The installed user certificates can now be found in the system store.

### Adding certificates
Install the certificate as a user certificate and restart the device.

### Removing certificates
Remove the certificate from the user store through the settings, and restart the device.

### Changelog

#### v0.5.0
* Properly support Magisk v20.4+ (tested v28.1)

#### v0.4.1
* Supports Android 10
* Updated Module to be compatible with latest Magisk module template (v20.4+)

#### v0.3
* The module now removes all user-installed certificates from the system store before copying them over, so that user certificates that were removed will no longer be kept in the system store.

#### v0.2
* Fixed directory creation bug
* Updated Module to be compatible with latest Magisk module template (v15+)

#### v0.1
* Initial release
