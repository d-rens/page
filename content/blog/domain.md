---
title: "Changing the Domain"
date: 2024-04-13T14:49:53+02:00
description: Will change my domain to d-rens.xyz due to .site price and to get rid of namecheap.
tags:
  - Technology
---

> You probably already noticed if you're here, the domain has changed from `https://d-rens.site` to `https://d-rens.xyz` on the 13th april 2024.

## Why switching the domain?

I have changed the domain for simple reasons. 

1. Had the domain on namecheap and transfer to porkbun would've cost ~$20.
2. The domain renewal (with .site) also cost $23, after the first year cost $1.96.

Both things could've been avoided easily but a year ago at this time I had no idea about renewals, DNS and everything attached to it so I did not make the smartest decision.

The .xyz domain now cost me $2.04 and the yearly renewal will cost around $10, so much more sustainable without any downsides, other than having go through this hassle now.


## What to do/consider when switching

Was asking myself that and also got good help on the exozyme matrix from [1a](https://www.1a-insec.net/) and [ersei](https://ersei.net/). They could tell me which HTTP response status to place ([301/308](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/301)), but as this is hosted by github pages (out of convenience for now) I have no access to the server or am able to place it another way[^0] :/ .

So I instead did it the *'wrong'* way I made up myself.

1. Bought the new domain
2. Made a new [git repo](https://github.com/d-rens/website-notice) 
3. Added html/css to portrait the following:

{{< figure src="../../domain/notice.png" title="Figure 1: notice on the old domain" >}} 

4. Added index.xml which is the rss feed, deleted all entries and instead added a notice that the domain will change.
5. Switched the host domain of the [normal repo](https://github.com/d-rens/page) and the [notice repo](https://github.com/d-rens/website-notice), so that the normal page will run on d-rens.xyz and the notice will run on d-rens.xyz, together with the rss entry.

## further 

I think that was a good way to do it with the means available, the old domain will expire in 5 days on the 19th april 2024, until then the notice will be portrait and the rss entry pervail.
Afterwards I'm finally gotten rid of namecheap and the too expensive renewal.

Apparently namecheap is not the worst dns provider there is, but the UI/UX, monopolist structure, advertisement, ... is just not enjoyable.

### API Options

At some point I thought that could be fixed by just using a [happy domain](https://www.happydomain.org/en/) docker and using it to manage my domains there, but the following hindered me:

> *We’re sorry, you have not met the criteria to qualify for API access. To qualify, you must have: Account balance of $50+, 20+ domains in your account, or purchases totaling $50+ within the last 2 years.*

That is an odd thing, because the API access should not cost them any meaningful amount extra, so that one needs to guarantee them these payments by having account balance or a lot of domains there, an amount of domains or balance  probably very few people ever use in two years on domains. 

Now with porkbun the dns management on the side is superior and if I want I can just run happydomain on an raspberry pi and manage the dns from there.


## conclusion

- Should've made more research when getting the domain.
- Should host the website myself. *Is there a cheap option for it?*
- namecheap is weird.

Have a nice day.



[^0]: At least I think so, am not sure.

