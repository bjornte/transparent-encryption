(Proposed UX specification for https://phynti.com/encryption-scheme)

# Phynti's encryption scheme

## A master passphrase provides access to your content

(To do: Write documentation here.)

## Secure hash algorithms encrypt your content

By default, Phynti employs both [SHA-512 and SHA-3][Secure Hash Algorithms]. Both are Secure Hash Algorithms from a family of cryptographic hash functions. SHA-512 was designed by the NSA in 2001. SHA-3, formerly called Keccak, was designed by non-NSA designers in 2015, and its internal structure differs significantly. Your Phynti passphrase is split in two separate hashes used as passwords for the individual algorithms, and both are used (sequentially) to encrypt all your content.

## Fragments of the passphrase is distributed to key holders

(To do: Write more documentation here.)

An method called [secret sharing][], designed by Adi Shamir and  George Blakley, is employed to split the master passphrase into key fragments. Individually, these fragments provide no clue as to what the master passphrase is. Multiple keys must be collected in order for them to provide any meaning.

The [basic setup][] is *three* key fragments of which *any two* will uncover your master passphrase (when combined with a single-use SMS code sent to your phone). The [custom setup][] allows you to tailor this further, for instance by making your bank a *mandatory key holder*.

### There are three types of key holders

(To do: Write more documentation here.)

* **Friends** make up the default key holders for a basic Phynti account.
* **Mandatory key holders**, such as your bank, may further strengthen the security by requiring formal procedures to provide keys.
* **[Non government key holders][]** safeguard the keys when performing threat monitoring in [safe rooms][].

--> Set up a [free, basic Phynti account][] or [tailor Phynti to your needs][].

[Secure Hash Algorithms]: https://en.wikipedia.org/wiki/Secure_Hash_Algorithms
[secret sharing]: https://en.wikipedia.org/wiki/Secret_sharing
[basic setup]: basic
[free, basic Phynti account]: basic
[custom setup]: custom
[tailor Phynti to your needs]: custom
[Non government key holders]: non-government-key-holders
[Safe rooms]: safe-rooms
