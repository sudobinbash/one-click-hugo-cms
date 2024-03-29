---
title: Dangerous Beer USB attack spotted on San Francisco
date: 2020-02-29T19:24:14.371Z
description: Free beer and a USB stick with streaming accounts? Too good to be truth...
image: img/img_20200228_140855.jpg
---
As an early domain name investor **Mike O’Connor** had by 1994 snatched up several choice online destinations, including bar.com, cafes.com, grill.com, place.com, pub.com and television.com. Some he sold over the years, but for the past 26 years O’Connor refused to auction perhaps the most sensitive domain in his stable —**corp.com**. It is sensitive because years of testing shows whoever wields it would have access to an unending stream of passwords, email and other proprietary data belonging to hundreds of thousands of systems at major companies around the globe.

Now, facing 70 and seeking to simplify his estate, O’Connor is finally selling corp.com. The asking price — $1.7 million — is hardly outlandish for a 4-letter domain with such strong commercial appeal. O’Connor said he hopes**Microsoft Corp.**will buy it, but fears they won’t and instead it will get snatched up by someone working with organized cybercriminals or state-funded hacking groups bent on undermining the interests of Western corporations.

One reason O’Connor hopes Microsoft will buy it is that by virtue of the unique way**Windows**handles resolving domain names on a local network, virtually all of the computers trying to share sensitive data with corp.com are somewhat confused Windows PCs. More importantly, early versions of Windows actually encouraged the adoption of insecure settings that made it more likely Windows computers might try to share sensitive data with corp.com.

At issue is a problem known as “[namespace collision](https://www.computerworld.com/article/3480799/icann-seeks-to-tackle-dns-namespace-collision-risks.html),” a situation where domain names intended to be used exclusively on an internal company network end up overlapping with domains that can resolve normally on the open Internet.

Windows computers on an internal corporate network validate other things on that network using a Microsoft innovation called[Active Directory](https://en.wikipedia.org/wiki/Active_Directory), which is the umbrella term for a broad range of identity-related services in Windows environments. A core part of the way these things find each other involves a Windows feature called “[DNS name devolution](https://www.itprotoday.com/security/whats-dns-name-devolution),” which is a kind of network shorthand that makes it easier to find other computers or servers without having to specify a full, legitimate domain name for those resources.

For instance, if a company runs an internal network with the name internalnetwork.example.com, and an employee on that network wishes to access a shared drive called “drive1,” there’s no need to type “drive1.internalnetwork.example.com” into Windows Explorer; typing “\\drive1\” alone will suffice, and Windows takes care of the rest.

But things can get far trickier with an internal Windows domain that does not map back to a second-level domain the organization actually owns and controls. And unfortunately, in early versions of Windows that supported Active Directory — Windows 2000 Server, for example — the default or example Active Directory path was given as “corp,” and many companies apparently adopted this setting without modifying it to include a domain they controlled.

Compounding things further, some companies then went on to build (and/or assimilate) vast networks of networks on top of this erroneous setting.

Now, none of this was much of a security concern back in the day when it was impractical for employees to lug their bulky desktop computers and monitors outside of the corporate network. But what happens when an employee working at a company with an Active Directory network path called “corp” takes a company laptop to the local Starbucks?

Chances are good that at least some resources on the employee’s laptop will still try to access that internal “corp” domain. And because of the way DNS name devolution works on Windows, that company laptop online via the Starbucks wireless connection is likely to then seek those same resources at “corp.com.”

In practical terms, this means that whoever controls corp.com can passively intercept private communications from hundreds of thousands of computers that end up being taken outside of a corporate environment which uses this “corp” designation for its Active Directory domain.
