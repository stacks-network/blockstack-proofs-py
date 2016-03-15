# Blockstack Proof Checker

[![CircleCI](https://img.shields.io/circleci/project/blockstack/blockstack-proofchecker.svg)](https://circleci.com/gh/blockstack/blockstack-proofchecker)
[![PyPI](https://img.shields.io/pypi/v/blockstack-proofchecker.svg)](https://pypi.python.org/pypi/blockstack-proofchecker/)
[![PyPI](https://img.shields.io/pypi/dm/blockstack-proofchecker.svg)](https://pypi.python.org/pypi/blockstack-proofchecker/)
[![PyPI](https://img.shields.io/pypi/l/blockstack-proofchecker.svg)](https://pypi.python.org/pypi/blockstack-proofchecker/)
[![Slack](http://slack.blockstack.org/badge.svg)](http://slack.blockstack.org/)

A python library for verifying identity proofs in blockstack profiles / blockchain IDs.

Proof types supported:

- Twitter
- Facebook
- GitHub
- Domain names

### Installation

```bash
$ pip install blockstack-proofchecker
```

### Getting Proofs from a Profile

To get the proofs for a blockchain ID, pass in the profile and username for the ID as shown below.

```python
>>> from proofchecker import profile_to_proofs
>>> proofs = profile_to_proofs(profile, username)
>>> print proofs
[{'identifier': 'naval', 'proof_url': 'https://twitter.com/naval/status/486609266212499456', 'service': 'twitter', 'valid': True}, {'identifier': 'navalr', 'proof_url': 'https://facebook.com/navalr/posts/10152190734077261', 'service': 'facebook', 'valid': True}, {'identifier': 'navalr', 'proof_url': 'https://gist.github.com/navalr/f31a74054f859ec0ac6a', 'service': 'github', 'valid': True}]
```
