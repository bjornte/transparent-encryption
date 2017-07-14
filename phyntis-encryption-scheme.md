(Proposed UX specification for https://phynti.com/encryption-scheme)

# Phynti's encryption scheme

## A master passphrase provides access to your content

(To do: Write documentation here.)

## Secure hash algorithms encrypts your content

By default, Phynti employs both [SHA-512 and SHA-3][Secure Hash Algorithms]. Both are Secure Hash Algorithms from a family of cryptographic hash functions. SHA-512 was designed by the NSA in 2001. SHA-3, formerly called Keccak, was designed by non-NSA designers in 2015, and its internal structure differs significantly. Your Phynti passphrase is split in two separate hashes used as passwords for the individual algorithms, and both are used (sequentially) to encrypt all your content.

## Key fragments are distributed to your friends. 

(To do: Write documentation here.)

--> Set up a [free, basic Phynti account][] or [tailor Phynti to your needs][].

[Secure Hash Algorithms]: https://en.wikipedia.org/wiki/Secure_Hash_Algorithms
[free, basic Phynti account]: basic
[tailor Phynti to your needs]: custom
