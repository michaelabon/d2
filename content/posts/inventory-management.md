---
title: "Inventory Management"
date: 2021-06-16T10:46:18-05:00
summary: Feeling like your vault is stuffed? Can’t figure out what roll to keep?
---
## [Destiny Item Manager]

<details>
<summary>Here are my go-to searches</summary>
    
### Favourite these:

    is:armor basestat:custom:>=32 not:classitem tag:none not:exotic not:blue

### Keep these:

    is:armor basestat:total:>=64 not:classitem tag:none not:exotic not:blue

### Raid armor - consider keeping these for the mod slot

    (is:armor source:raid) tag:none

### Junk these:

    is:armor basestat:total:<64 basestat:custom:<32 not:classitem not:exotic not:maxpower  not:tagged not:inloadout
    is:classitem energycapacity:<5 not:tagged  not:maxpower not:inloadout
    perk:"field prep" OR perk:"firmly planted" OR perk:"sneak bow" tag:none  not:maxpower
    is:blue not:tagged not:maxpower not:inloadout (is:armor OR is:weapon)

which combined becomes:

    (is:armor basestat:total:<64 basestat:custom:<32 not:classitem not:exotic not:maxpower  not:tagged not:inloadout) OR (is:classitem energycapacity:<5 not:tagged  not:maxpower not:inloadout) OR (perk:"field prep" OR perk:"firmly planted" OR perk:"sneak bow" tag:none  not:maxpower) OR (is:blue not:tagged not:maxpower not:inloadout (is:armor OR is:weapon))

### Infuse these:

    tag:junk power:>powerfulcap

</details>

## [Vault Cleaner]

Figure out which weapon and armor rolls you should keep
and which you should shard.

Vault Cleaner just locks/unlocks the results for you,
so you can dismantle the items yourself.

I usually start here and then fine-tune the results with God Roll Finder.

## [God Roll Finder]

Compare your drops with 1) expert wisdom (same as DIM) and 2) community-selected perks.

## [D2 Gunsmith]

Craft your own god roll,
see how the perks and masterworking affect the stats,
and copy your wishlists into DIM.

## [D2 Checklist]

Turns out, the armor that the vendors sell can actually be great!
I've ignored Zavala's armor rolls for _years_.
The _Armor Stat Deals_ section is a great way to find out
who is selling armor that you might be interested in.

## Today in Destiny

The [Eververse Calendar] is useful to
find out what Tess will be selling for Silver
and what she will be selling for Bright Dust.

## Lost Sector Calendar

Two different formats for you to choose:

-   [Visual][lost-sector-visual]
-   [Spreadsheet][lost-sector-spreadsheet]

[D2 Checklist]: https://www.d2checklist.com/home
[D2 Gunsmith]: https://d2gunsmith.com
[Destiny Item Manager]: https://app.destinyitemmanager.com
[Eververse Calendar]: https://www.todayindestiny.com/eververseCalendar
[God Roll Finder]: https://www.light.gg/god-roll/roll-appraiser/
[Vault Cleaner]: https://destinyrecipes.com/vault
[lost-sector-spreadsheet]: https://docs.google.com/spreadsheets/d/1rWoyGWouGFismhk2BQzbeuV7PgoxzGRhxf2Kyi27kTo/edit#gid=0
[lost-sector-visual]: https://www.todayindestiny.com/ls_calendar
