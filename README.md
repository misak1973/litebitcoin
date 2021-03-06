Litebitcoin Core integration/staging tree
=====================================

[![Build Status](https://travis-ci.org/litebitcoins/litebitcoin.svg?branch=master)](https://travis-ci.org/litebitcoins/litebitcoin)

https://lbtc.info

What is Litebitcoin?
-------------------

Litebitcoin is an experimental digital currency that enables instant payments to
anyone, anywhere in the world. Litebitcoin uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Litebitcoin Core is the name of open source
software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of
the Litebitcoin Core software, see [https://lbtc.info](https://lbtc.info).

License
-------

Litebitcoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/litebitcoins/litebitcoin/tags) are created
regularly to indicate new official, stable release versions of Litebitcoin Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).



Specifications
--------------

Name: LiteBitcoin

Ticker: LBTC

PoW Algorithm: Scrypt

Block Reward: 500 LBTC

Address letter: 2

Multisig Address letter: 4

Maturity: 20 blocks

Difficulty Re-target: Every block

P2P Port: 19037

RPC Port: 19038

Total coin supply: 1 Billion Lite-Bitcoins



Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/qa) of the RPC interface, written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/qa) are installed) with: `qa/pull-tester/rpc-tests.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and OS X, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.
