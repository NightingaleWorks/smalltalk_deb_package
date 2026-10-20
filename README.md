# GNU Smalltalk Debian Package

Debian package for installing GNU Smalltalk 3.2.5 (2013-04-08).

Official GNU Smalltalk website:

https://www.gnu.org/software/smalltalk/

## Background

GNU Smalltalk is no longer available in the standard Debian repositories.

The following command does not work on recent Debian releases:

```bash
sudo apt install gnu-smalltalk
```

This package allows GNU Smalltalk 3.2.5 to be installed on Debian-based distributions.

## Installation

```bash
sudo apt install ./smalltalk_3.2.5-1_amd64.deb
```

## Package Verification

The package can be verified using both SHA-256 and OpenPGP signatures.

### Verify SHA-256 Checksum

Calculate the checksum:

```bash
sha256sum smalltalk_3.2.5-1_amd64.deb
```

Expected output:

```text
8d88caf734381fc7079a687beeb88fec8e4df888e29f64735a88466edf0fa82b  smalltalk_3.2.5-1_amd64.deb
```

### Verify OpenPGP Signature

Import the public key:

```bash
gpg --import public-key.asc
```

Verify the package signature:

```bash
gpg --verify smalltalk_3.2.5-1_amd64.deb.asc smalltalk_3.2.5-1_amd64.deb
```

The output should contain:

```text
gpg: Good signature from "NightingaleWorks (Budapest, HU) <szabolcsszlavik@gmail.com>"
```

### Verify the Key Fingerprint

Expected fingerprint:

```text
D356 918E 2027 C2A9 9629 5A25 1513 91E4 27C2 814F
```

Check the imported key:

```bash
gpg --fingerprint NightingaleWorks
```

The fingerprint displayed by GPG must match the fingerprint shown above.

## Files Included in the Release

```text
smalltalk_3.2.5-1_amd64.deb
smalltalk_3.2.5-1_amd64.deb.asc
SHA256SUMS
public-key.asc
```

## Disclaimer

This package is not affiliated with or endorsed by the GNU Project. GNU Smalltalk and all related trademarks belong to their respective owners.

Happy coding in Smalltalk!
