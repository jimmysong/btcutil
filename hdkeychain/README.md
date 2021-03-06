hdkeychain
==========

[![Build Status](https://travis-ci.org/conformal/btcutil.png?branch=master)]
(https://travis-ci.org/conformal/btcutil)

Package hdkeychain provides an API for bitcoin hierarchical deterministic
extended keys (BIP0032).

A comprehensive suite of tests is provided to ensure proper functionality.  See
`test_coverage.txt` for the gocov coverage report.  Alternatively, if you are
running a POSIX OS, you can run the `cov_report.sh` script for a real-time
report.  Package hdkeychain is licensed under the liberal ISC license.

## Feature Overview

- Full BIP0032 implementation
- Single type for private and public extended keys
- Convenient cryptograpically secure seed generation
- Simple creation of master nodes
- Support for multi-layer derivation
- Easy serialization and deserialization for both private and public extended
  keys
- Support for custom networks by registering them with btcnet
- Obtaining the underlying EC pubkeys, EC privkeys, and associated bitcoin
  addresses ties in seamlessly with existing btcec and btcutil types which
  provide powerful tools for working with them to do things like sign
  transations and generate payment scripts
- Uses the btcec package which is highly optimized for secp256k1
- Code examples including:
  - Generating a cryptographically secure random seed and deriving a
    master node from it
  - Default HD wallet layout as described by BIP0032
  - Audits use case as described by BIP0032
- Comprehensive test coverage including the BIP0032 test vectors
- Benchmarks

## Documentation

[![GoDoc](https://godoc.org/github.com/conformal/btcutil/hdkeychain?status.png)]
(http://godoc.org/github.com/conformal/btcutil/hdkeychain)

Full `go doc` style documentation for the project can be viewed online without
installing this package by using the GoDoc site here:
http://godoc.org/github.com/conformal/btcutil/hdkeychain

You can also view the documentation locally once the package is installed with
the `godoc` tool by running `godoc -http=":6060"` and pointing your browser to
http://localhost:6060/pkg/github.com/conformal/btcutil/hdkeychain

## Installation

```bash
$ go get github.com/conformal/btcutil/hdkeychain
```

## Examples

* [NewMaster Example]
  (http://godoc.org/github.com/conformal/btcutil/hdkeychain#example-NewMaster)  
  Demonstrates how to generate a cryptographically random seed then use it to
  create a new master node (extended key).
* [Default Wallet Layout Example]
  (http://godoc.org/github.com/conformal/btcutil/hdkeychain#example-package--DefaultWalletLayout)  
  Demonstrates the default hierarchical deterministic wallet layout as described
  in BIP0032.
* [Audits Use Case Example]
  (http://godoc.org/github.com/conformal/btcutil/hdkeychain#example-package--Audits)  
  Demonstrates the audits use case in BIP0032.

## License

Package hdkeychain is licensed under the [copyfree](http://copyfree.org) ISC
License.
