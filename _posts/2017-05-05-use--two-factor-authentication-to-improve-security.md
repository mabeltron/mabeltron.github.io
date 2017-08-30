---
title: Use two factor authentication to improve security
date: 2017-05-05 23:55
category: security
tags: passwords, 2fa
status: published
layout: post
---

Too many people still trust their online life to massively insecure passwords. The name of your dog and its birthday, or a cleverly crafted dictionary word changed to a combination of numbers and letters just doesn't cut it any more. Dictionary attacks are pervasive and high powered. There are still huge numbers of websites and services that can be cracked by dictionary attacks, where scripts throw word combinations at common usernames such as root or Administrator, or increasingly collections of stolen email addresses and passwords from other places that have been used elsewhere.

There are any number of solutions to this. Let's start with your passwords.

1. Make them unique for every site you log into. Which follows on to
2. Use a password manager. This allows you to store complex passwords easily. My personal favourite is [LastPass][57adc47a], which on and offline access to your passwords across all your devices. You can also combine this with
3. Use random passphrases. This seems counter-intuitive but a string of random words has much higher entropy than 12 or 16 random letters and characters. This [blog post](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases) from the EFF covers the principle and provides some updated word lists that can be randomly selected. I use the [random.org][9f6ada23] Randomizer app on my phone to pick my words. This is great for password that you have to type often, and you will surprise yourself by how many you can remember. Also where you can,
4. Use two factor authentication (2FA). There has been a gradual takeup with this across a lot of service. The rise and spread of the smartphone has assisted its takeup enormously because all of a sudden the principle of 'something that you have and something that you know' is picked up by that chunk of processing power in your pocket.

A lot of major services now provide 2FA. Google has for at least seven years with its own Google Authenticator app. Amazon offers authentication by SMS or authenticator app (Google or LastPass both work). Twitter and Facebook use SMS, as does Paypal to name but a few. The EFF recently had a [12 Days of 2FA][1c1ae9af] campaign which documented how to enable 2FA on many major services.

SMS is less satisfactory because it depends on having a conventional phone signal where an app usually relies on your phone's clock being in sync but it's still better than nothing.

2FA in combination with strong passwords will help protect your online life. It's more than just your bank details, it's a part of your identity so it makes sense to make it as secure as possible.

  [57adc47a]: https://www.lastpass.com "LastPass"
  [9f6ada23]: https://www.random.org/ "random.org"
  [1c1ae9af]: https://www.eff.org/deeplinks/2016/12/12-days-2fa-how-enable-two-factor-authentication-your-online-accounts "12 Days of 2FA"
