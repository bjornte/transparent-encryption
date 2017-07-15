(Proposed UX specification for https://phynti.com)

# Phynti

_Keep your digital assets safe by trusting your friends._

<button>Create a free account</button>

## It's human to forget. By trusting your closest friends, you can still retrieve your passwords.

A situation may occur that makes you unable to recall your passwords. With Phynti, a vault for passwords & digital assets, that's OK. Using industry standard [secret sharing][], fragments of a *master passphrase* is distributed among your closest friends.

## Keep yourself safe from hackers.

Your passwords & assets are protected by [the industry's best encryption][], a master passphrase of your choice, and optionally redundant [two factor authentication][]. We don't keep a copy of the master passphrase, so even if we are breached, there's nothing to steal. Our code is open source, so you can perform full due diligence on our procedures.

## Set up a free account in three clicks...

The basic setup is _three_ key fragments of which _any two_ will uncover your master passphrase (when combined with a single-use SMS code sent to your phone). The fragments are distributed among your three most trusted friends or family members. 

[Click here][basic] to get going, and you're done in 90 seconds.

## ...or design your own vault

* I want `three ▼` key fragments to distribute among friends. 
* Any `two ▼` of these are required to assemble the master passphrase. 
* In addition I want `no ▼` mandatory fragments. (These can be shared with selected third parties, such as affiliated [banks][] and [NGOs][])
* I'll use `SMS messages ▼` for [two factor authentication][]. Other, redundant options are available and recommended.
* When [safe rooms][] becomes available, my preferred [NGO key holder(s)][] are `Amnesty International and the Norwegian Bar Association ▼` 
* My encryption scheme is `SHA-512 enveloped in SHA-3 ▼`.

[Click here][custom] to finish setting up your tailored Phynti.

## Safe rooms

Phynti plans to offer [safe rooms][] where scans for safety threats can happen while otherwise protecting the users' privacy.

[Secret sharing]: encryption-scheme
[the industry's best encryption]: encryption-scheme
[two factor authentication]: https://en.wikipedia.org/wiki/Multi-factor_authentication
[basic]: basic
[custom]: custom
[banks]: phyntis-encryption-scheme#mandatory-key-holders
[NGOs]: non-government-key-holders
[NGO key holder(s)]: non-government-key-holders
[safe rooms]: safe-rooms
