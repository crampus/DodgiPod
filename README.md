# DodgiPod
Documenting an ultimately failed adventure into bluetooth-modding an iPod Classic 6/7th Generation
> doc is a work in progress, will update with additional files and images as time permits

# preamble
If you're here looking to follow this as an actual guide, don't.
I'm approaching this as more of a cautionary tale rather than an actual how-to guide.

# kudos
Serious kudos to @Olsro and his serial number rewrite process.\
Without that, my entire project would have been dead in the water.\
I mean, ultimately, it was, but it would have been even *deaderer*.

Also kudos to ZacBuilds on Youtube.\
His project was the first I saw using a momentary switch at the base of the 3.5mm audio jack port for the Bluetooth Pair function.

# project aim
I wanted to explore whether it's possible to mod the iPod with:
- No permanent modifications to original hardware
- No loss to hold switch functionality
- Keeping the thin form factor
- Preserving as much of the metal back as physically possible
- Adding Bluetooth output
- Adding iFlash µDual w/ 2x256GB microSD cards (512GB)
- 3,000mAh battery pack added

> [!TIP]
> **isn't this just a classic connect with extra steps?**\
> well... kind of, and I'd strongly recommend anyone lurking here just does that instead.

# a series of occasionally fortunate events
## 0. buy an iPod
Obviously, the first thing you'll need to do is obtain an iPod.\
I stumbled across a very reasonably priced 120GB 2008 7th Generation iPod Classic (sometimes called a "6.5th generation"), in perfect working order; the battery is still holding strong, and even the original hdd still works. Or it did when I pulled it out at least.

> [!CAUTION]
> 120GB 7th Generation iPods on firmware 2.0.1 have a firmware limitation restricting them to 128GB or less storage.\
> If you want to use more than 128GB storage, you'll need to refer to @Olsro's guide to overwrite your serial number and trick iTunes into flashing 160GB 7th generation iPod firmware (version 2.0.4).

## 1. start designing things in CAD
Already owning a 3D printer, my next step was to start designing parts in CAD.\
- Obtain reference files:
  1. iPod 5th-7th generation rear shell
  2. iPod video face plate
- Parts designed:
  1. Switch slider to fit between hold switch and headphone jack on the iPod
  2. Drill guide jig

## 2. order parts from various locations
I procured a bunch of parts:
- from aliExpress:
  - replacement rear shell (ultimately, 2 of)
  - KCX BT EMITTER preprogrammed bluetooth transmitter (ultimately, 3 of)\
    > [!WARNING]
    > **KCX BT EMITTERs are notorious for signal strength issues.**\
    > All 3 I purchased cut out and were basically useless for bluetooth signal strength once the shell was closed.
  - 5-pack of 2.4GHz Bluetooth IPEX antennas with 5cm leads
  - 10-pack of 4x4x2mm (ish) momentary switches
  - 10-pack of 10x4x2mm (ish) slider switches
  - clear hard plastic shell
  - a hot air / soldering station
- from Elite Obsolete:
  - replacement rear shell (as the final version shell once I got all my mistakes out of the way)
  - replacement face plate
  - replacement click wheel
  - 3,000 mAh "thin" battery
  - replacement LCD bracket
- From a local electronics retailer (Jaycar)
  - A pack of assorted solid core insulated copper wire
  - 2-part epoxy resin
- From a local hardware store:
  - A 3.2mm hex drive drill bit
  - A 3.2mm round tip tungsten carbide dremel milling bit


## 3. have a crack at it
Once I had all the required bits and bobs, there was nothing for it but to give it a shot.
I had my new switch hole lined up in CAD:
<img width="1024" alt="sketch_slider_cutout" src="https://github.com/user-attachments/assets/7047e36d-743f-430f-9674-ef1dab70870c" />
and the printed jig:
<img width="1024" alt="img_0592" src="https://github.com/user-attachments/assets/18e114ec-f901-4250-a422-e7943f77dc15" />


And, somewhat disappointingly, my first attempt went rather poorly.
<img width="1024" alt="img_1107" src="https://github.com/user-attachments/assets/8dd7f8e6-c0ab-489d-9d3f-bcb074d5854f" />

I drilled too quickly, and the 3d printed drill jig melted and deformed, leading to one of the holes "walking" over the rounded edge of the rear shell.\
<img width="768" height="1024" alt="img_1091_1024" src="https://github.com/user-attachments/assets/cb08c851-944c-4dd5-aa31-8b3792aaa9e0" />

Compounding this issue, I first tried to use a cutting wheel to join the holes before moving to a drilling bit. 
<img width="1024" alt="img_1092" src="https://github.com/user-attachments/assets/800fa0d9-9675-471c-af22-452ea1f31fef" />\

Turns out, the cutting wheel radius was larger than I realised, and to cut through the holes, I wound up overshooting and nearly taking out the headphone jack mounting point.\
Stopping just shy of this, allowed me to continue with this as a proof of concept, but the aesthetic damage was done.
<img width="1024" alt="img_1107" src="https://github.com/user-attachments/assets/48a34890-5d24-4826-8645-d50a3cc90e9c" />

## 4. second chance
Given the total failure of the first attempt, I tried again. I redesigned the drill jig to have 3 holes, refining my drilling process to first "etch" a locating divet using an engraving bit before drilling, slowly, to create 3 holes instead of the original 2.
<img width="1024" alt="img_2460" src="https://github.com/user-attachments/assets/d85a3b84-2205-41a2-b034-4dc29929a0ae" />\

This was initially successful:
<img width="1024" height="768" alt="img_2467_1024" src="https://github.com/user-attachments/assets/3bc33008-2b0c-46ad-b872-9a46dca16e73" />

But still I let the project down by a bit of a slip while dremelling.\
And then another slip trying to work out the original slip.
<img width="768" height="1024" alt="img_2470_1024" src="https://github.com/user-attachments/assets/7ecec41a-89b1-4821-a27f-c3311296c143" />\

End of the day though, I managed to assemble a prototype:
<img width="768" height="1024" alt="img_3333_1024" src="https://github.com/user-attachments/assets/475d29b4-a8fc-4e45-a911-5d5433af5c2e" />
<img width="1024" alt="img_3258" src="https://github.com/user-attachments/assets/674503dd-ba8b-49d9-a6c2-6026d038628d" />
(spoilers: you can see the final electronics assembly at the top of frame)

## 5. proven concept
Having a "good enough for testing" prototype, I soldered up a proof of concept shell using a Samsung S21 vibrator and the KCX transmitter. I'm not going to go into the weeds on how to solder this up, other guides already exist; and it's a bit of a mess. The loopy white wire is connected to the COMMON pin of the slider switch. Power from a 5V supply was routed to the LEFT pin of the slider. 

Electronics guides here are not provided. I wouldn't recommend this specifically, but if you are going to go down this rabbit hole, refer to the many existing guides online, I didn't do anything special here, except by routing power to the KCX Transmitter via the slider switch at the top. And adding copious amounts of epoxy resin/glue, of course.
Testing on the bench was a success with the exception of a bit of signal noise: [video](https://github.com/user-attachments/assets/1e14ce0d-f60e-4ff7-aff8-55afbaf15aff)

## 6. final draft
Seeing as everything had worked so far, I was ready to go ahead with the final build.
I grabbed my engraving bit and lined up my holes...
<img width="1024" alt="img_3233" src="https://github.com/user-attachments/assets/08c2b343-40a1-48c8-b65e-641f2b7dd68f" />
<img width="1024" height="768" alt="img_3232_1024" src="https://github.com/user-attachments/assets/bd34c39f-c8b2-45bd-892d-0a043db25d26" />

Started drilling...
<img width="1024" alt="img_3239" src="https://github.com/user-attachments/assets/8c5289f5-6faf-4846-b5a9-a86eddd2b656" />

... carefully, using the jigs as slow as the drill would go ...
<img width="1024" alt="img_3242" src="https://github.com/user-attachments/assets/b86beadc-319c-495e-8456-54488f54fa2b" />

... until I had the same holes as before.
<img width="1024" alt="img_3243" src="https://github.com/user-attachments/assets/5d5e5780-e776-49ad-880d-4aa12924ece7" />

Remembering the lessons of the past, I used painters' tape to protect the surface, and then started dremelling...
<img width="1024" alt="img_3247" src="https://github.com/user-attachments/assets/188c9b37-d08c-4f2f-944a-5aa48937eade" />

Then I glued in place the switch slider...
<img width="1024" height="768" alt="img_3252_1024" src="https://github.com/user-attachments/assets/69f72cb8-7f3f-4022-a53e-bb95df27032d" />

pre-assembled the electronics modules...
<img width="1024" alt="img_3254" src="https://github.com/user-attachments/assets/910f73c7-b4ae-4521-9241-4730b9358009" />

... de-soldered the piezo-electric clicker speaker...
<img width="1024" alt="IMG_3448" src="https://github.com/user-attachments/assets/a0738997-9be8-4dc1-8c3f-1326fa6e31d3" />

... drilled out by hand the rear of the audio jack to fit the pairing switch...
<img width="1024" alt="IMG_3442" src="https://github.com/user-attachments/assets/75f3d6e0-680a-4b5b-9b7b-301868e6986a" />
> [!CAUTION]
> Be very gentle whilst hand-drilling. You do not need much pressure, all you're doing is applying a mild chamfer to the rear of the hole, until the switch sits comfortably in the hole without activating.

... soldered in the audio wires...
<img width="1024" alt="IMG_3639" src="https://github.com/user-attachments/assets/c2a8d114-d207-4a08-ba88-fc04f3a5060a" />

... soldered in the pairing button...
<img width="1024" alt="IMG_3640" src="https://github.com/user-attachments/assets/541a7684-9587-42ce-9c17-4b84dd335720" />

... and the taptic mod...
<img width="1024" alt="IMG_3645" src="https://github.com/user-attachments/assets/b5d277ac-89dd-4be6-aeae-312fbb712dfc" />

... finally sealing it all up ready for installing in the iPod.
<img width="1024" alt="IMG_3648" src="https://github.com/user-attachments/assets/e5024669-1bbd-4f05-80ca-e02f7d3b593b" />

Installation was relatively smooth, I used some cheap double-sided tape to hold everything in place.
<img width="1024" alt="IMG_3654" src="https://github.com/user-attachments/assets/f12436b8-75f8-4bdf-b37d-cd791099c0f9" />

... and started soldering in wires.
<img width="1024" alt="IMG_3655" src="https://github.com/user-attachments/assets/27913166-b711-436f-a557-3d39a215ea3c" />
>[!NOTE]
>You may notice how close together the power and taptic wires are. DO NOT DO THIS. Wires this short conduct heat extremely effectively. These wires melted together during soldering, causing a short, and nearly killing my iPod.

On the other side, I had already prepared an LCD bracket, with a hole cut into it, and an antenna passed through to the other side. There is enough room, and it doesn't put _too much_ pressure on the LCD, but you will probably get a slight pressure spot on the display. One thing I would not recommend is adhering the antenna to the display. Use Kapton tape to adhere it to the LCD bracket instead. The antenna adhesive sticks _too well_ to the LCD, and if you try to remove it, you will damage the fragile LCD panel backlight polarising sheets.
<img width="1024" alt="IMG_3691" src="https://github.com/user-attachments/assets/a25034be-c46c-4bb4-9d41-34e8fd53b4a2" />

Gave it a test, everything works perfectly on the bench.
<img width="1024" alt="IMG_3692" src="https://github.com/user-attachments/assets/75f62bf8-080c-4b92-baef-2e3e2db1ba5b" />

Still, I completed the sync and, blissfully ignorant to the issues I was about to face, I prepared to close everything up.
<img width="1024" alt="IMG_3695" src="https://github.com/user-attachments/assets/fc418bc8-5f6d-4ab2-8e2b-58714ffaed98" />

Here was the first hint of danger. The battery is slightly too long for this mod-kit, and occupies the same space as some of the wires and the antenna cable. I was starting to doubt at this point, but pressed on as hope slowly faded...
<img width="1024" alt="IMG_3695" src="https://github.com/user-attachments/assets/a9155de9-321a-41d0-84b8-762879c69edd" />
>[!NOTE]
>You might have better luck with a 2,000mAh battery instead of the "Slim" 3,000mAh battery I used here.

Final steps of assembly, I used some tape to hold the battery in place, and soldered together the ground wire for the bluetooth mod.
<img width="1024" alt="IMG_3699" src="https://github.com/user-attachments/assets/08efe1a5-104c-43c2-84a8-8076ce150594" />

... and noticed I had my power wire tangled with the antenna wire...
<img width="1024" alt="IMG_3700" src="https://github.com/user-attachments/assets/2519cd5c-80db-4938-8bfb-82ffef673f61" />

... but got it soldered together and added some heat shrink to keep it safe.
<img width="1024" alt="IMG_3707" src="https://github.com/user-attachments/assets/8102573b-896c-473d-ba5b-3dd3d458829c" />

Connecting everything together was a bit of a finnicky process.
<img width="1024" alt="IMG_3943" src="https://github.com/user-attachments/assets/80b345c2-0e1d-47a4-8dc9-c8231fc4e856" />
There's too many wires in here, and they're all fighting for space.
Coupled with the battery too large, I could never actually close the case, even though I could get it to fit in a plastic hard-case to keep it safe.

<img width="1024" alt="IMG_3709" src="https://github.com/user-attachments/assets/8ec44548-64c3-4e8c-a033-ce2faeb9d9bd" />
<img width="1024" alt="IMG_3708" src="https://github.com/user-attachments/assets/80af5b52-e0e5-44f0-8101-6b3d3ac3ae57" />

Great. it's fine, everything kind of fits, everything on the iPod works, taptic feels great,  I'll just get a new, smaller, battery later...

Success!

## 7. it all falls apart
Turned on the bluetooth...

Not Success!

Why is it getting so hot? Why is taptic not working now?

Oh crap, I've ballsed something up...

During the ensuing panic, I didn't take any further photos, but what had happened is, in soldering in the power wires to the switch (red wire)
<img width="1024" alt="IMG_3655" src="https://github.com/user-attachments/assets/78c5878b-0885-4a0a-bcdf-701bd02c4888" />
the wire had melted the shielding on the white taptic wires right next to it causing a short circuit.\ 
Oh crap. No matter, I checked and resoldered everything, moved the wires around and insulated them wires a bit better, put it all back together, everything works, happy days.

Except. Up until this point I'd only tested on the bench. As soon as I put the iPod in my pocket, the audio immediately started cutting out.\
Constantly.\
Pulling it out of my pocket, it also cut out when I put any part of my body between the screen and my headphones. And when I pointed the screen away from my face.\
Not a great sign... What's the point of hacking in bluetooth if you can't have the iPod in your pocket and listen?\
Why is the signal so directional?\
Is the screen acting like a polariser film for the signal somehow?

I'm not skilled enough at radio theory to troubleshoot further, and at this point, I'm thinking it's not really worth continuing to throw good money after bad at this project; I just want something that works, and that I know will work.

Now, something I only noticed later, is that there was a "nick" in the shielding of the antenna cable. So the antenna cable MIGHT have been damaged.
The nick isn't visible here:
<img width="1024" alt="IMG_3707" src="https://github.com/user-attachments/assets/60a0ee59-32b3-4cad-b9ec-3ff74adf2f57" />
but is here:
<img width="1024" alt="IMG_3943" src="https://github.com/user-attachments/assets/28734a4e-5eb1-4829-8766-aa487cd2c515" />
But, in removing everything from the case to think about what I want to do to make this again, later, better, I found out the antenna was extremely difficult to remove from the LCD without damaging it.
And the amount of epoxy resin I'd put everywhere, made everything nigh on impossible to service.

So, unfortunately, everything has been returned to the standard shell, with only the iFlash kit surviving to this day, and this whole experiment has made me realise the commercial options out there are probably better than anything I can hack together myself; 

## 8. next steps
I'm not entirely sure where to go from here.
Having a PCB with through-holes to solder directly to the relevant pads of the headphone jack would help make the KCX mod more compact and easy to solder in to iPods, but at this point, given the sub-optimal range and broadcast characteristics of the bluetooth mod when it _did_ work, I'm not sure that I really want to dive head-first into PCB design just for this project. It would be cool to know how to make PCBs though, so maybe one day I will, but for now, I just want a functional iPod with bluetooth and taptic feedback.

So which commercial option do I choose?

There's only three mod kits from two vendors I know of:
1. BoxyPixel Mk II MAX & Mk II MIN
  - I love the aesthetic of these two. The metal frame, glass front/back, all looks amazing.
  - The MAX is a bit too chonky for my liking, so I would have preferred the MIN
  - The MIN doesn't support installing taptic engines anywhere, only the MAX does; and it's a different taptic engine to what I have already on-hand.
  - Looks like it uses the same KCX transmitters as this homemade kit.
  - No range claims on website, and there is an external antenna that looks the same as the one I used with my kit already.
    - None of that is conclusive and the issues I did have may have been self-inflicted, but it feels like rolling the dice on a kit that could wind up having the same issues.
  - Out of stock as at early August 2026 when I'm weighing up my options. So even if I did want to, I can't pick this option.
2. Moonlit Market Classic Connect 2
  - Rear shell only, basically plug and play, ticks all the boxes; bluetooth, taptic, all in one self-contained PCB ready to go
  - It doesn't use a KCX transmitter, and they advertise it as having up to 20m of range, which gives me a high level of confidence it will work from my pocket.
  - I'm less of a fan of the design of the replacement rear shell. It gives the iPod a thick border, and it is completely plastic.
  - Definitely not a fan of needing glue to stick it all together, but I understand having retention nubs wouldn't have been compatible with the injection moulding process used by Moonlit Market
  - I could always just 3D print a different shell; that won't have the same process limitation and could instead attach with some nubs...

Maybe a Mk. III version of option 1 will come along and use a different/more reliable Bluetooth chip and change my mind. but at this stage, but I'm leaning towards Option 2.
