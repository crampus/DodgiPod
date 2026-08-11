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
  - 5-pack of 2.4GHz Bluetooth iPEX antennas with 5cm leads
  - 10-pack of 4x4x2mm (ish) momentary switches
  - 10-pack of 10x4x2mm (ish) slider switches
  - clear hard plastic shell
  - a hot air / soldering station
  - 
- from Elite Obsolete:
  - replacement rear shell (as the final version shell once I got all my mistakes out of the way)
  - replacement face plate
  - replacement click wheel
  - 3,000 mAh "thin" battery
  - replacement LCD bracket
- From a local electronics retailer (Jaycar)
  - A pack of assorted solid core insulated copper wire
  - 2-part epoxy resin
  - 
- 
## 3. have a crack at it
