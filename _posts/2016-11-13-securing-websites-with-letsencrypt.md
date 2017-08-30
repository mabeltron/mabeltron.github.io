---
Title: Securing websites with LetsEncrypt
Date: 2016-11-13 09:02
Category: Security
Tags: https, letsencrypt
---

Given the benefit of hindsight, there probably should have been a method of providing security and identity in the original specification for the [World Wide Web][537ef69b]. [HTTPS][376fb81e] was added to Netscape in 1994 and adopted as a standard in 2000, and in the meantime became a lucrative business for a number of companies. While it was possible to secure communications on a web site with a self signed certificate, the lack of 'trust' by a third party has increasingly become an issue in web browsers.

This issue has been addressed by [LetsEncrypt][1e8cc30c], a service which provides free [domain validated certificates][4f3fd40d] that are backed by a certificate authority and supported by many large organisations. Their certificates work with all modern browsers alongside [SNI][09d86c58] so the previous issue of requiring multiple IP addresses for domains has also been removed.

LetsEncrypt is easy to set up and use. Your [hosting provider][6228ff4e] may support it, and I'll talk about working with cPanel in a future post, but if not LetsEncrypt and the [EFF][918941a1] supply the [Certbot ACME client][45cba73a] which provides instructions for common platforms and operating systems.

LetsEncrypt certificates are valid for three months by default, but it's simple to [automate renewal][6489f8cb]. LetEncrypt also reminds you when the certificates are about to expire.

There's no excuse not to secure your website any more. LetsEncrypt is simple, open and free.

[537ef69b]: http://webfoundation.org/about/vision/history-of-the-web/ "World Wide Web"
[376fb81e]: https://en.wikipedia.org/wiki/HTTPS "HTTPS"
[1e8cc30c]: https://letsencrypt.org "LetsEncrypt"
[4f3fd40d]: https://en.wikipedia.org/wiki/Domain-validated_certificate "Domain validated certificates"
[09d86c58]: https://en.wikipedia.org/wiki/Server_Name_Indication "SNI"
[6228ff4e]: https://community.letsencrypt.org/t/web-hosting-who-support-lets-encrypt/6920 "hosting provider"
[918941a1]: https://eff.org "Electronic Frontier Foundation"
[45cba73a]: https://certbot.eff.org/ "Certbot ACME client"
[6489f8cb]: https://certbot.eff.org/docs/using.html#renewal "certbot renewal"
