# eblocker-bootstrap

This package prepares a Debian system for the eBlocker software:

* Install initial network interface configuration
* Remove existing Debian repositories
* Configure eBlocker repository and certificates
* Add user `icapd` for running `eblocker-icapserver`

## Build

Select an architecture:

* `armbian` for Banana Pi M2+ boards
* `raspbian` for Raspberry Pi boards
* `amd64` for AMD and Intel systems

Select a release:

* `buster`

Optionally append an environment:

* `stage`
* `test`

The combination of the above is a profile ID, for example:

* `armbian-buster`
* `raspbian-buster-stage`
* `amd64-buster-test`

Build the package with maven, setting the profile ID with option `-P`,
for example:

    mvn -Pamd64-buster clean package

The Debian package can be found in the `target` directory.
