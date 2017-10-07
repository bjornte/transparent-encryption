(This is the first version of the landing page, showing what it look like in March 2016 before this effort was [merged with Phynti](README.md).)

# Transparent encryption

Welcome!
---
This is a completely open discussion. Please make any changes as you wish. If you know of other forums where this concept has been described, please provide a link.

This concept also has a (rather downvoted) [thread on Information Security][StackExchange thread] over at Stack Exchange.

Summary
---
A concept for how to make it harder to commit crimes by creating controlled insight (screening) into encrypted communication. An attempt at discovering middle ground between Cook's and Obama’s standpoints in the current GovtOS debate.

Background & motivation
---
As of 2016, Tim Cook and Barack Obama is in a divisive fight over encryption, privacy rights and law enforcement’s need of screening our communication for unlawful content. Both Cook and Obama have [MLK][MLK] as an idol, so I’m assuming both want good to prevail. This repository is intended as a discussion (at least initially) for how to bridge the current gap between the parties.

Intended benefits
---
* Strong encryption with no back doors. Just as difficult as previously for criminals to hack into an account.
* Make it harder for criminals to operate without detection. Screening opportunity for law enforcement – in a controlled, transparent setting. It should become harder to commit crimes for two reasons:
  * Services that supported the screening process would be less suitable for criminal activity.
  * Services that opt out of this concept would become more visible.

First (admittedly rough) draft
---
* A customer, possibly voluntarily <sup>1</sup>, shares parts of her password, «partials», with 3<sup>rd</sup> party «key holders» of her own choosing.
  * The 3<sup>rd</sup> parties can be government agencies, commercial entities such as banks, and major [NGOs][NGO] such as [Amnesty International][Amnesty].
  * E.g., a Norwegian customer may choose to share her partials with Amnesty, [DNB][DNB] and the Norwegian government’s tax authority.
  * For the customer, the password handling should be integrated into [password management apps][password manager] such as 1password.
  * The splitting up of the password is probably done with [Shamir's Secret Sharing][SSSS] (SSSS) or similar.
* These partial passwords can be combined into complete passwords in a strictly controlled setting.
  * Perhaps naïvely, I’m imagining that all the key holders have representatives physically present at a location such as the [European Court of Human Rights][ECtHR] (for European customers). The combination of partial passwords into complete ones happens only in this location.
* This controlled setting has the purpose of detecting criminal behavior by way of screening<sup>2</sup>.
  * The screening of customers’ data should be transparent and very tightly controlled. 
  * The screening is limited only to defined use cases that are seen as beneficial by the respective key holders (or possibly to a superior organ. I can only think of the UN).
  * The key holders must publish information<sup>3</sup> about all algorithms they allow to be run on their customers’ data sets.
* The screening is similar to what already happens on Dropbox, OneDrive etc. using PhotoDNA. The intention here is to investigate if this type of screening can be made both more transparent and universal. Probably the biggest difference between today’s and the suggested screenings is the concept that the key holders are independent 3<sup>rd</sup> parties that are selected by the customer.
* A major prerequisite is to avoid [single points of failure][SPOF].

<sup>1</sup> About voluntariness: There are several possibilities, including: 1) The service is voluntary. 2) The service is mandatory, similar to how banks must report clients’ holdings to tax authorities (while keeping the assets safe from other prying eyes). I realize it’s too early for me to have an opinion about incentives. I agree with [@SmokeDispenser, @Matthew et al][StackExchange thread] that people probably needs some stronger incentive than «just helping out law enforcement in general». However I don’t have an answer to what the incentive(s) should be. That’s a major discussion… which should take place on GitHub. However, even if the service ended up being mandatory, my suggestion remains that the customer herself can choose her own key holders, and that these key holders safeguard which algorithms are run on their customers’ data sets.

<sup>2</sup> Long term, this could possibly also make it harder for AIs to communicate undetectedly.

<sup>3</sup> Whether source code and hashes should be published is also open for discussion. I’m assuming at least some information should be withheld, e.g. I guess it’s a bad idea to post all the PhotoDNA hashes.


License
---
[CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/)

[SSSS]: https://en.wikipedia.org/wiki/Shamir%27s_Secret_Sharing
[ECtHR]: https://en.wikipedia.org/wiki/European_Court_of_Human_Rights
[SPOF]: https://en.wikipedia.org/wiki/Single_point_of_failure
[Amnesty]: https://en.wikipedia.org/wiki/Amnesty_International
[UBS]: https://en.wikipedia.org/wiki/Banking_in_Switzerland
[DNB]: https://en.wikipedia.org/wiki/DNB_ASA
[MLK]: https://en.wikipedia.org/wiki/Martin_Luther_King,_Jr.
[NGO]: https://en.wikipedia.org/wiki/Non-governmental_organization
[StackExchange thread]: http://security.stackexchange.com/questions/118227/a-service-for-sharing-partial-passwords-with-key-holders-for-screening-purpo
[password manager]: https://en.wikipedia.org/wiki/Password_manager
