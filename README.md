
# eblocker-bootstrap

This package prepares a Debian system for the eBlocker software:

* Install initial network interface configuration
* Remove existing Debian repositories
* Configure eBlocker repository and certificates
* Add user `icapd` for running `eblocker-icapserver`

## Build

Select an architecture:

* `raspios` for 64bit Raspberry Pi boards
* `amd64` for AMD and Intel systems

Select a release:

* `bookworm`

Optionally append an environment:

* `stage`
* `test`

The combination of the above is a profile ID, for example:

* `raspios-bookworm`
* `amd64-bookworm-test`

Build the package with maven, setting the profile ID with option `-P`,
for example:

    mvn -Praspios-bookworm clean package

The Debian package can be found in the `target` directory.
