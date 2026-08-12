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
<img width="1024" alt="img_1107" src="https://github.com/user-attachments/assets/48a34890-5d24-4826-8645-d50a3cc90e9c" />\

## 5. second chance
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

## 4. proven concept
Having a "good enough for testing" prototype, I soldered up a proof of concept shell using a Samsung S21 vibrator and the KCX transmitter. I'm not going to go into the weeds on how to solder this up, other guides already exist; and it's a bit of a mess. The loopy white wire is connected to the COMMON pin of the slider switch. Power from a 5V supply was routed to the LEFT pin of the slider. 

Electronics guides here are not provided. I wouldn't recommend this specifically, but if you are going to go down this rabbit hole, refer to the many existing guides online, I didn't do anything special here, except by routing power to the KCX Transmitter via the slider switch at the top. And adding copious amounts of epoxy resin/glue, of course.
Testing on the bench was a success with the exception of a bit of signal noise: [video](https://github.com/user-attachments/assets/1e14ce0d-f60e-4ff7-aff8-55afbaf15aff)

## 5. final draft
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

and connected up the electronics modules...
<img width="1024" alt="img_3254" src="https://github.com/user-attachments/assets/910f73c7-b4ae-4521-9241-4730b9358009" />

> [!WARNING]
> Cliffhanger, things here did not go according to plan...
