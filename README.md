# zerossl-ip-cert &middot; [![License](https://img.shields.io/hexpm/l/plug?logo=Github&style=flat)](https://github.com/feranydev/zerossl-ip-cert/blob/master/LICENSE) [![Go Report Card](https://goreportcard.com/badge/github.com/feranydev/zerossl-ip-cert)](https://goreportcard.com/report/github.com/feranydev/zerossl-ip-cert) [![Build workflow](https://github.com/feranydev/zerossl-ip-cert/actions/workflows/build.yml/badge.svg)](https://github.com/feranydev/zerossl-ip-cert/actions/workflows/build.yml)

zerossl-ip-cert is an automation tool for issuing ZeroSSL IP certificates.

* Use ZeroSSL [REST API](https://zerossl.com/documentation/api/)  to implement certificate issuing.
* Mainly made for **IP** certificates (ipv4 only for now).
* Call external program for automatically verification.
* Painless certificate renewal.
* Cross platform (Linux/Macos/Windows).

## Installation

* Package zerossl-ip-cert contains ZeroSSL [REST API](https://zerossl.com/documentation/api/) client, one can
  just `go get github.com/feranydev/zerossl-ip-cert` and import it to use the client.
* To build static executables, clone this repository and `make release` , or you can make your desire target binary, just take a look at the [Makefile](https://github.com/feranydev/zerossl-ip-cert/blob/master/Makefile).

## Usage

zerossl-ip-cert rely on configuration file to run. To archive the goal of issuing certificate automatically, you need do some additional work, saying the external hook.

### Usage Info

```
Version: 1.0.0-beta.1

Usage: zerossl-ip-cert [ -renew ] -config CONFIG_FILE

  -config string
        Config file
  -renew
        Renew existing certs only
```

### Configuration File

You can find a sample configuration file [here](https://github.com/feranydev/zerossl-ip-cert/blob/master/exec/sample-config.yaml), with enough comments in it.

 And also a sample  state record file [here](https://github.com/feranydev/zerossl-ip-cert/blob/master/exec/sample-current.yaml), just for troubleshooting.

## License

[Apache-2.0](https://github.com/feranydev/zerossl-ip-cert/blob/master/LICENSE)
