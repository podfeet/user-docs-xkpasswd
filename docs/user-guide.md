# User Guide

### Why is it beta?

When you first go to [xkpasswd.net](https://xkpasswd.net) while the project is in beta, you'll see an explanation of how this tool is being ported from old and busted Perl code to modern web development languages including JavaScript. You'll be invited to push the "Use the Beta" button to get started. 

![screenshot of xkpasswd.net with an arrow pointing to the Use the Beta button](assets/use-the-beta.png)

If you want to skip this step, go directly to the beta version at [beta.xkpasswd.net](https://beta.xkpasswd.net).

The tool is not yet feature-complete, but what you can use is functioning properly. If any feature is not functioning properly when you visit the tool, you'll see it labeled as such.

### Generate Password(s) with Default Configuration

If you don't want to fuss around with any kind of settings to generate some passwords, you can simply enter the desired number of passwords and hit the Generate button. By default, this will create 3 highly-complex passwords of the following configuration:

* 3 English words of 4-8 characters in length where each word has a leading capital letter
* Each word is separated by a randomly chosen character but is consistent within each password generated
* 2 digits of padding are on each end of the character-separated words
* 2 random character symbols are added as final padding on either end

For example: `%%85?Fell?Tokyo?Building?74%%`

![3 passwords created according to the configuration described above](assets/default-passwords.png)

### Copying passwords

You have two options to copy the passwords. By default, the passwords are shown in a list format with their own individual copy buttons which will copy directly to your clipboard.

![List view with a red text box explaining to click on the copy buttons](assets/passwords-list-view.png)

The second radio button lets you view the same password list as a block of text that is pre-selected. This view lets you simply use Command/Control-C to copy all of the offered passwords and paste them elsewhere for modification or to let you have a big list of passwords when you're changing several of them at the same time.

![Preselected block of passwords ready to be copied](assets/passwords-block-of-text.png)

## Presets

For ease of use, XKPASSWD comes with a set of predefined presets. Presets can be used as-is, or, they can be used as a starting point for creating your own configuration. Note that one of the presets is for security questions. You should never give a real answer to a security question because this is the kind of information that's easy to get in a phishing attack. Think about how easy it would be to find out the city in which you went to high school for example. Instead of answering truthfully, use the `SECURITYQ` preset and store the question and answer in your password manager.

The following presets are defined:

* `APPLEID` - a preset respecting the many prerequisites Apple places on Apple
ID passwords. Apple's official password policy is located here:
[http://support.apple.com/kb/ht4232](http://support.apple.com/kb/ht4232). Note that Apple's knowledgebase article
neglects to mention that passwords can't be longer than 32 characters. This preset
is also configured to use only characters that are easy to type on the standard
iOS keyboard, i.e. those appearing on the letters keyboard (`ABC`) or the
numbers keyboard `.?123`, and not those on the harder-to-reach symbols
keyboard `#+=`. Below is a sample password generated with this preset:

    `@60:london:TAUGHT:forget:70@`

* `DEFAULT` - the default configuration. Below is a sample password generated
with this preset:

    `12:settle:SUCCEED:summer:48`

* `NTLM` - a preset for 14-character NTMLv1 (NTLM Version 1) passwords. ONLY USE
THIS PRESET IF YOU MUST! The 14-character limit does not allow for sufficient
entropy in the case where the attacker knows the dictionary and config used
to generate the password, hence this preset will generate low entropy warnings.
Below is a sample password generated with this preset:

    `0=mAYAN=sCART@`

* `SECURITYQ` - a preset for creating fake answers to security questions. It
generates long nonsense sentences ending in `.`, `!` or `?`, for example:

    `Wales outside full month minutes gentle?`

* `WEB16` - a preset for websites that don't allow more than 16-character long
passwords. Because 16 characters is not very long, a large set of
symbols are chosen from for the padding and separator. Below is a sample
password generated with this preset:

    `:baby.ohio.DEAR:`

* `WEB32` - a preset for websites that don't allow more than 32 character long
passwords. Below is a sample password generated with this preset:

    `+93-took-CASE-money-AHEAD-31+`

* `WIFI` - a preset for generating 63 character long WPA2 keys (most routers
allow 64 characters, but some only 63, hence the odd length). Below is a sample
password generated with this preset:

    `2736_ITSELF_PARTIAL_QUICKLY_SCOTLAND_wild_people_7441!!!!!!!!!!`

* `XKCD` - a preset inspired by the original [XKCD comic](http://xkcd.com/936/), but with some alterations to provide sufficient
entropy to avoid low entropy warnings. Below is a sample password generated
with this preset:

    `KING-madrid-exercise-BELGIUM`

