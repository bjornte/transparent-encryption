# transparent-encryption
A discussion on how to create controlled insight (screening) into encrypted communication

This project is considered merged with [Phynti][]. Proposed new description of Phynti below. Old README for this repository is [here](README-old.md)

# Phynti UX spec (wireframes & written material)

## Landing page ([phynti.com][])

_Keep your digital assets safe by trusting your friends._

### It's human to forget. By trusting your closest friends, you can still retrieve your passwords.

A situation may occur that makes you unable to recall your passwords. With Phynti, a vault for passwords & digital assets, that's OK. Using industry standard [secret sharing][], fragments of a [master passphrase][] is distributed among your closest friends.

### Keep yourself safe from hackers.

Your passwords & assets are protected by [the industry's best encryption][], a master passphrase of your choice, and optionally redundant [two factor authentication][]. We don't keep a copy of the master passphrase, so even if we are breached, there's nothing to steal. Our code is open source, so you can perform full due diligence on our procedures.

### Set up in three clicks...

The basic setup is _three_ key fragments of which _any two_ will uncover your master passphrase (when combined with a single-use SMS code sent to your phone). The fragments are distributed among your three most trusted friends or family members. 

[Click here][bootstrap] to get going, and you're done in 90 seconds.

### ...or design your own vault

* I want `three ▼` key fragments to distribute among friends. 
* Any `two ▼` of these are required to assemble the master passphrase. 
* In addition I want `no ▼` mandatory fragments. (These can be shared with selected third parties, such as affiliated [banks][] and [NGOs][])
* I'll use `SMS messages ▼` for [two factor authentication][]. Other, redundant options are available and recommended.
* When [safe rooms][] becomes available, my preferred [NGO key holder(s)][] are `Amnesty International and the Norwegian Bar Association ▼` 
* My encryption scheme is `SHA-512 enveloped in SHA-3 ▼`.

[Click here][tailor] to finish setting up your tailored Phynti.

### Phynti's encryption scheme
<a name="phyntis-encryption-scheme"></a>

By default, Phynti employs both [SHA-512 and SHA-3][Secure Hash Algorithms]. Both are Secure Hash Algorithms from a family of cryptographic hash functions. SHA-512 was designed by the NSA in 2001. SHA-3, formerly called Keccak, was designed by non-NSA designers in 2015, and its internal structure differs significantly. Your Phynti passphrase is split in two separate hashes used as passwords for the individual algorithms, and both are used (sequentially) to encrypt all your content.

## Phynti safe rooms ([phynti.com/safe-rooms][phynti-com-safe-rooms])

### A common ground for public safety and personal privacy

Both the EU, USA and other nations are evaluating or implementing legislations that will enforce citizens to unlock their data for scanning for safety threats (such as terrorist planning and illegal depiction of minors). 

Previously, the technical community has strongly resisted such legislation due to fears of safety breaches and undesired governmental surveillance. 

Phynti's safe rooms offers a common ground where safety and privacy can coexist. The safe rooms have uncompromised security, safeguarded in part by non governmental agencies (NGOs), while allowing law enforcement agencies to fulfil their threat monitoring duties. 

Phynti safe rooms are safer than other alternatives since threat monitoring technically cannot take place without the discretion of NGOs. The safe rooms do not compromise the basic encryption through use of backdoors or weaker algorithms, which are the alternatives currently being evaluated or implemented elsewhere.

The safe rooms are under planning. [Click here][newsletter] to receive our development newsletter. Until legislation enforces such scans, safe room participation is voluntary.

### How do the safe rooms work?

The safe rooms consist of both a technical infrastructure and a collaboration between multiple partners. Key contributing partners are:

* **[NGO key holders][]** (e.g. Amnesty, the International Red Cross and Doctors without Borders) who controls the key fragments that are necessary to perform decryption and thus threat monitoring. The NGOs act as a gatekeeper protecting the citizens' privacy rights.
* **[Service providers][]** (e.g. Facebook, Amazon, Google and Apple) who host the data on which threat monitoring is performed. The service providers make sure that the threat monitoring happens in a neutral environment outside the direct control of law enforcement agencies. 
* Select **[law enforcement agencies][]** (e.g. Interpol), who supplies the [dictionaries][] that are used for threat monitoring, and who evaluates if results should lead to formal investigation.

Phynti plans to offer [safe rooms][] where scans for safety threats can happen while otherwise protecting the users' privacy. 

### What is a safe room dictionary?

A safe room dictionary defines content that is statistically significant in terms of threat monitoring. It consists of:

* Words and terms, such as _"where to purchase explosives ingredients"_.
* [Regular expressions][], allowing for [fuzzy matching][] of above terms.
* [Hashes][] (fingerprints) of known threats, such as Microsoft's index of illegal depiction of minors.

### How are the dictionaries used?

The dictionaries are fed into a search service that monitor the [document corpus][] for matching content. The search has support for both linguistic operations and deep learning (neural networks).

The search service is hosted in a environment physically controlled by the service providers. The key fragments are supplied by the NGOs, and only when these have green lighted the content of the dictionaries. Law enforcement agencies do not have access to the content itself, but only to extracts indicating a safety threat, and only when submitted at the discretion of the participating NGOs. 

Before result output is presented to any user (either NGO or law enforcement representative), it is redacted such that both data owners and individualt mentioned will remain anonymous, through employment of hashed IDs (persistent pseudonyms). Only when the NGOs, on a case to case basis, accept that there is sufficient basis for format threat investigation, will the search publish actual identities.

## Safe room scenarios ([phynti.com/safe-room-scenarios][phynti-com-safe-room-scenarios])

All scenarios starts as follows: 

* The user has signed up with Phynti, either voluntary or due to legislation changes. 
* The law enforcement agency wants to perform threat monitoring. It provides a dictionary which is green lighted by the NGOs. 
* In the safe room, to which the law enforcement agency does not have access, the NGOs (and other mandatory key holders) supply key * fragments as well as the dictionary. 
* The service provider supplies encrypted data. 
* The content is decrypted and the search performs the scan. 

Scenarios:

* **Innocent, non suspiscious user:** No results are produced for the user. Unless explicitly requested by the user, the law enforcement agency is not informed that the user had content which was scanned.
* **Malicious user with innocent-looking content:** As above. 
* **Innocent user with irrellevant content that matches the dictionary:** Some results are produced for the user. The NGOs review the results and deem them irrellevant. The law enforcement agency is not informed that the user had content which was scanned. If the scan is performed across a large user base, the law enforcement agency is informed how many results were deemed irrellevant.
* **Innocent user with suspiscious content:** Some results are produced for the user. The NGOs review the results and deem them potentially suspiscious. The law enforcement agency is given results in which indenties are substituted with pseudonyms. It cannot make a case for formal investigation, and the individual's identity is not revealed.
* **Malicious user with suspiscious content:** Some results are produced for the user. The NGOs review the results and deem them potentially suspiscious. The law enforcement agency is given results in which indenties are substituted with pseudonyms. It convinces the NGOs that there is a case for formal investigation. The individual's identity is revealed.


[phynti]: https://phynti.com
[phynti.com]: https://phynti.com
[phynti-com-safe-rooms]: https://phynti.com/safe-rooms
[phynti-com-safe-room-scenarios]: https://phynti.com/safe-room-scenarios
[master passphrase]: #master-passphrase
[encryption]: https://en.wikipedia.org/wiki/Encryption (Encryption – Wikipedia)
[the industry's best encryption]: phyntis-encryption-scheme (Phynti's encryption scheme)
[Secure Hash Algorithms]: https://en.wikipedia.org/wiki/Secure_Hash_Algorithms (Secure Hash Algorithms – Wikipedia)
[bootstrap]: #bootstrap
[safe rooms]: #safe-rooms
[dictionaries]: #dictionaries
[hashes]: https://en.wikipedia.org/wiki/Cryptographic_hash_function (Cryptographic hash function – Wikipedia)
[tailor]: #tailor
[NGOs]: #NGOs
[NGO key holders]: #NGOs
[NGO key holder(s)]: #NGOs
[service providers]: #service-providers
[banks]: #banks
[law enforcement agencies]: #law-enforcement-agencies
[newsletter]: #newsletter
[two factor authentication]: https://en.wikipedia.org/wiki/Multi-factor_authentication (Multi-factor authentication – Wikipedia)
[Secret sharing]: https://en.wikipedia.org/wiki/Secret_sharing (Secret sharing – Wikipedia)
[fuzzy matching]: https://en.wikipedia.org/wiki/Record_linkage#Probabilistic_record_linkage (Probabilistic record linkage or fuzzy matching – Wikipedia)
[regular expressions]: https://en.wikipedia.org/wiki/Regular_expression (Regular expression – Wikipedia)
[document corpus]: https://en.wikipedia.org/wiki/Text_corpus (Text corpus – Wikipedia)

## To do

* Feedback from Torgeir.
* Improve texts
    * Proof reading.
    * Simplify further.  
    * More detailed information on technical issues such as [secret sharing][] & the employed [secure hash algorithms][]
    * Norwegian version if we want to pitch to government stakeholders.
* More detailed interaction design
    * Detailed flow for setting up a basic Phynti account with messages to friends etc.
    * Illustrations.
    * More detailed wireframing incl. Call to action (CTA) buttons.
* Front end development
    * Bootstrap or other CSS framework. 
    * Possibly style guide such as Pattern Lab.

### Payoff (variations)
* Digital safekeeping powered by trusting your friends.
* Put trust in your friends, with the password manager that allows you to forget.
* The password manager that allows you to forget by trusting your friends.
* It's OK forget when you trust your friends.
* Trust your friends, not your memory. (Or us.)
* Don't trust us. Don't trust yourself. Trust your friends.
* Don't trust us, or even yourself. But trust your friends.
* Trust your friends. Not us. Not yourself.

## Bin: Old text fragments

And in addition, your valuables are safe from your fleeting memory.

We're safer because we're different: We don't store your passwords, and we don't require you to remember the master key to the vault (although remembering it is convenient).


