(Proposed UX specification for https://phynti.com/safe-room-scenarios)

## Safe room scenarios

All scenarios start as follows: 

* The user has [signed up][] with Phynti, either voluntary or due to legislation changes, and has selected her [NGO key holders][]. 
* The [law enforcement agency][] wants to perform threat monitoring. It provides a dictionary which is green lighted by the NGOs. 
* In the safe room, to which the law enforcement agency does not have access, the NGOs (and other mandatory key holders) supply [key fragments][] as well as the dictionary. 
* The [service provider][] supplies encrypted data. 
* The content is decrypted and the search performs the scan. 

Scenarios:

* **Innocent, non suspicious user:** No results are produced for the user. Unless explicitly requested by the user, the law enforcement agency is not informed that the user had content which was scanned.
* **Malicious user with innocent-looking content:** As above. 
* **Innocent user with irrelevant content that matches the dictionary:** Some results are produced for the user. The NGOs review the results and deem them irrelevant. The law enforcement agency is not informed that the user had content which was scanned. If the scan is performed across a large user base, the law enforcement agency is informed how many results were deemed irrelevant.
* **Innocent user with suspicious content:** Some results are produced for the user. The NGOs review the results and deem them potentially suspicious. The law enforcement agency is given results in which indentities are substituted with pseudonyms. It cannot make a case for formal investigation, and the individual's identity is not revealed.
* **Malicious user with suspicious content:** Some results are produced for the user. The NGOs review the results and deem them potentially suspicious. The law enforcement agency is given results in which indentities are substituted with pseudonyms. It convinces the NGOs that there is a case for formal investigation. The individual's identity is revealed.

<-- Back to [Safe rooms][]

[Safe rooms]: safe-rooms
[Law enforcement agency]: law-enforcement-agency
[NGO key holders]: non-government-organisation
[service provider]: service-provider
[signed up]: basic
[key fragments]: key-fragments
