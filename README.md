# SOC Bypasses

This repository highlights key weaknesses in common or traditional analysts / Security Operation Centres. While you can use these to avoid being detected by a human if you run a SOC or are an analyst think about how you can address these weaknesses.

## Get tuned out

Volume is generally perceived as evil in a SOC because they both lacked the foresight to equip themselves to improve their detections before they received to much volume and lack the expertise or funding to fix the issue now that it is present. Use resources like https://wtfbins.wtf/ and your own testing to find behaviours that generate alerts. Then start to spam the SOC with these alerts. At best your going to get an exclusion placed for a directory you will now be conscious of and at worst analysts will skip over you if you hide the noise you created well enough.

## IT Support is the SOCs enemy

IT Support are often granted the exact same or even greater permissions than security personnel all the while being less equipped to calculate the associated risks of their decisions. Get users using machines to raise IT tickets by slowing down their machines or breaking desktop icons etc. Once IT Support connects to that machine a plethora of opportunities will arise. One particularly crazy idea would be to wait for a remote connection from IT support and then force a UAC prompt. UAC prompts create a protected desktop that depending on the RMM software makes IT Supports screen go black. How do IT support often get around this? They share their password with the user.


## If its not on the internet dont patch it

tbd

## Public Cloud Storage

tbd
