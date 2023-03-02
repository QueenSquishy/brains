# SOC Bypasses

This repository highlights key weaknesses in common or traditional analysts / Security Operation Centres. While you can use these to avoid being detected by a human if you run a SOC or are an analyst think about how you can address these weaknesses.

## Get tuned out

Volume is generally perceived as evil in a SOC because they both lacked the foresight to equip themselves to improve their detections before they received to much volume and lack the expertise or funding to fix the issue now that it is present. Use resources like https://wtfbins.wtf/ and your own testing to find behaviours that generate alerts. Then start to spam the SOC with these alerts. At best your going to get an exclusion placed for a directory you will now be conscious of and at worst analysts will skip over you if you hide the noise you created well enough.

## IT Support is the SOCs enemy

IT Support are often granted the exact same or even greater permissions than security personnel all the while being less equipped to calculate the associated risks of their decisions. Get users using machines to raise IT tickets by slowing down their machines or breaking desktop icons etc. Once IT Support connects to that machine a plethora of opportunities will arise. One particularly crazy idea would be to wait for a remote connection from IT support and then force a UAC prompt. UAC prompts create a protected desktop that depending on the RMM software makes IT Supports screen go black. How do IT support often get around this? They share their password with the user.


## If its not on the internet dont patch it

Over time the industry has really put the fear into people when it comes to patching stuff (for the most part) but IT teams still use their own and often misguided criteria for what should be patched first. A perfect example of this is IT infrastructure that isn’t present on the internet. If you can find it in an org it will very likely not be up to date. The solarwinds attack is a great example of this as one of the largest mitigating factors was that people simply hadn’t updated the product in so long that they never received the back door. If your lucky this is doubly so for misconfigurations as well.

## Public Cloud Storage

Often, I see adversaries trying to use public cloud storage but make one clear mistake. They use the wrong one. Don’t bother building your infrastructure prior to landing in an enterprise as thanks to covid there’s a 99 per cent chance they are already using some form of public cloud storage whether its google drive or otherwise. Enumerate this then setup your infrastructure in the exact same place. This will get you past both detection and prevention mechanisms.  

## Parent/Child Process Relationships are our fav

How a parent file or process relates to the file or process its invoking is the biggest point of interest for a traditional analyst beyond file properties so its important you make these look as normal as possbile. That means no using your own binaries to launch other unknown binaries, no launching stuff in silly directories like temp or the desktop and download folders. If you want to use a file native to the system understand what it normally does first and keep to that behaviour. If that native file doesnt behave the way you want it dont use it just find another file.

## Only English

This one is super simple. Everytime you write something do it in a language thats not english particulary a english that doesnt translate well to english because analysts are ltierally going to just just run it through google translate so the more broken the translation the longer their response times.
