# transparent-encryption
A discussion on how to create controlled insight (screening) into encrypted communication

* This project is considered merged with [Phynti][] by [Torgeir Hovden][]. 
* Proposed new description of Phynti below. 
* Old readme for this repository is [here](README-old.md).

---

# Phynti UX spec (wireframes & written material)

* [phynti.com landing page][Phynti landing page]
* [Safe rooms][]

### Phynti's encryption scheme
<a name="phyntis-encryption-scheme"></a>

By default, Phynti employs both [SHA-512 and SHA-3][Secure Hash Algorithms]. Both are Secure Hash Algorithms from a family of cryptographic hash functions. SHA-512 was designed by the NSA in 2001. SHA-3, formerly called Keccak, was designed by non-NSA designers in 2015, and its internal structure differs significantly. Your Phynti passphrase is split in two separate hashes used as passwords for the individual algorithms, and both are used (sequentially) to encrypt all your content.



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

Before result output is presented to any user (either NGO or law enforcement representative), it is redacted such that both data owners and individuals mentioned will remain anonymous, through employment of hashed IDs (persistent pseudonyms). Only when the NGOs, on a case to case basis, accept that there is sufficient basis for format threat investigation, will the search publish actual identities.

## Safe room scenarios ([phynti.com/safe-room-scenarios][phynti-com-safe-room-scenarios])

All scenarios starts as follows: 

* The user has signed up with Phynti, either voluntary or due to legislation changes. 
* The law enforcement agency wants to perform threat monitoring. It provides a dictionary which is green lighted by the NGOs. 
* In the safe room, to which the law enforcement agency does not have access, the NGOs (and other mandatory key holders) supply key * fragments as well as the dictionary. 
* The service provider supplies encrypted data. 
* The content is decrypted and the search performs the scan. 

Scenarios:

* **Innocent, non suspicious user:** No results are produced for the user. Unless explicitly requested by the user, the law enforcement agency is not informed that the user had content which was scanned.
* **Malicious user with innocent-looking content:** As above. 
* **Innocent user with irrelevant content that matches the dictionary:** Some results are produced for the user. The NGOs review the results and deem them irrelevant. The law enforcement agency is not informed that the user had content which was scanned. If the scan is performed across a large user base, the law enforcement agency is informed how many results were deemed irrelevant.
* **Innocent user with suspicious content:** Some results are produced for the user. The NGOs review the results and deem them potentially suspicious. The law enforcement agency is given results in which indentities are substituted with pseudonyms. It cannot make a case for formal investigation, and the individual's identity is not revealed.
* **Malicious user with suspicious content:** Some results are produced for the user. The NGOs review the results and deem them potentially suspicious. The law enforcement agency is given results in which indentities are substituted with pseudonyms. It convinces the NGOs that there is a case for formal investigation. The individual's identity is revealed.


[phynti]: https://phynti.com
[phynti.com]: https://phynti.com
[Phynti landing page]: phynti-landing-page
[safe rooms]: safe-rooms
[phynti-com-safe-rooms]: https://phynti.com/safe-rooms
[phynti-com-safe-room-scenarios]: https://phynti.com/safe-room-scenarios
[Torgeir Hovden]: https://github.com/thovden
[master passphrase]: #master-passphrase
[encryption]: https://en.wikipedia.org/wiki/Encryption
[the industry's best encryption]: phyntis-encryption-scheme
[Secure Hash Algorithms]: https://en.wikipedia.org/wiki/Secure_Hash_Algorithms
[bootstrap]: #bootstrap
[dictionaries]: #dictionaries
[hashes]: https://en.wikipedia.org/wiki/Cryptographic_hash_function
[tailor]: #tailor
[NGOs]: #NGOs
[NGO key holders]: #NGOs
[NGO key holder(s)]: #NGOs
[service providers]: #service-providers
[banks]: #banks
[law enforcement agencies]: #law-enforcement-agencies
[newsletter]: #newsletter
[two factor authentication]: https://en.wikipedia.org/wiki/Multi-factor_authentication
[Secret sharing]: https://en.wikipedia.org/wiki/Secret_sharing
[fuzzy matching]: https://en.wikipedia.org/wiki/Record_linkage#Probabilistic_record_linkage
[regular expressions]: https://en.wikipedia.org/wiki/Regular_expression
[document corpus]: https://en.wikipedia.org/wiki/Text_corpus

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
