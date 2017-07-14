(Proposed UX specification for https://phynti.com/what-is-a-safe-room-dictionary)

### What is a safe room dictionary?

A safe room dictionary defines content that is statistically significant in terms of threat monitoring. It consists of:

* Words and terms, such as _"where to purchase explosives ingredients"_.
* [Regular expressions][], allowing for [fuzzy matching][] of above terms.
* [Hashes][] (fingerprints) of known threats, such as Microsoft's index of illegal depiction of minors.

[fuzzy matching]: https://en.wikipedia.org/wiki/Record_linkage#Probabilistic_record_linkage
[regular expressions]: https://en.wikipedia.org/wiki/Regular_expression
[hashes]: https://en.wikipedia.org/wiki/Cryptographic_hash_function
