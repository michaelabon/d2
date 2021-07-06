---
title: "Inventory Management"
date: 2021-06-16T10:46:18-05:00
lastmod: 2021-07-05T18:02:00-05:00
summary: Feeling like your vault is stuffed? Can’t figure out what roll to keep?
weight: 2
keywords:
- "outside"
---
## [Destiny Item Manager]

<details>
<summary>Here are my go-to searches</summary>
    
### Favourite these:

    basestat:custom:>=32 tag:none not:exotic not:blue

### Keep these:

    basestat:total:>=64 tag:none not:exotic not:blue
    basestat:highest:>=25 basestat:secondhighest:>=20 tag:none not:exotic not:blue

which combined becomes:
    
    (basestat:total:>=64) OR (basestat:highest:>=25 basestat:secondhighest:>=20) tag:none not:exotic not:blue
    
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

<details>
    <summary>TMMania has a good Vault Analyzer search, which I've modified below</summary>
    
    ("TMMania's Vault Analyzer** | Highlights Trash |
    Update Version: July 4th, 2021"
    or
    (
    (
        (
        is:weapon is:blue or "Removed sunset filter"
        )
    or
    (
        (is:armor -is:exotic -is:classitem)

        -(source:raid -source:dcv OR "Removed is:dupelower, since I want to have multiple energy types")
        -(source:events)

        -(maxbasestatvalue:any)
        -(basestat:any:>=23)
        -(basestat:total:>=65)

        -(((basestat:mobility&resilience:>=17.5) or
        (basestat:mobility&recovery:>=17.5) or
        (basestat:mobility&discipline:>=17.5) or
        (basestat:mobility&intellect:>=17.5) or
        (basestat:mobility&strength:>=17.5) or
        (basestat:resilience&mobility:>=17.5) or
        (basestat:resilience&recovery:>=17.5) or
        (basestat:resilience&discipline:>=17.5) or
        (basestat:resilience&intellect:>=17.5) or
        (basestat:resilience&strength:>=17.5) or
        (basestat:recovery&mobility:>=17.5) or
        (basestat:recovery&resilience:>=17.5) or
        (basestat:recovery&discipline:>=17.5) or
        (basestat:recovery&intellect:>=17.5) or
        (basestat:recovery&strength:>=17.5) or
        (basestat:discipline&mobility:>=17.5) or
        (basestat:discipline&resilience:>=17.5) or
        (basestat:discipline&recovery:>=17.5) or
        (basestat:discipline&intellect:>=17.5) or
        (basestat:discipline&strength:>=17.5) or
        (basestat:intellect&mobility:>=17.5) or
        (basestat:intellect&resilience:>=17.5) or
        (basestat:intellect&recovery:>=17.5) or
        (basestat:intellect&discipline:>=17.5) or
        (basestat:intellect&strength:>=17.5) or
        (basestat:strength&mobility:>=17.5) or
        (basestat:strength&resilience:>=17.5) or
        (basestat:strength&recovery:>=17.5) or
        (basestat:strength&discipline:>=17.5) or
        (basestat:strength&intellect:>=17.5)) -basestat:secondhighest:<15)

        -(((basestat:mobility&resilience&recovery:>=15) or
        (basestat:mobility&resilience&discipline:>=15) or
        (basestat:mobility&resilience&intellect:>=15) or
        (basestat:mobility&resilience&strength:>=15) or
        (basestat:mobility&recovery&discipline:>=15) or
        (basestat:mobility&recovery&intellect:>=15) or
        (basestat:mobility&recovery&strength:>=15) or
        (basestat:mobility&discipline&intellect:>=15) or
        (basestat:mobility&discipline&strength:>=15) or
        (basestat:mobility&intellect&strength:>=15) or
        (basestat:resilience&recovery&discipline:>=15) or
        (basestat:resilience&recovery&intellect:>=15) or
        (basestat:resilience&recovery&strength:>=15) or
        (basestat:resilience&discipline&intellect:>=15) or
        (basestat:resilience&discipline&strength:>=15) or
        (basestat:resilience&intellect&strength:>=15) or
        (basestat:recovery&discipline&intellect:>=15) or
        (basestat:recovery&discipline&strength:>=15) or
        (basestat:recovery&intellect&strength:>=15) or
        (basestat:discipline&intellect&strength:>=15)) -basestat:thirdhighest:<11)

        -(((basestat:mobility&resilience&recovery&intellect:>=13.25) or
        (basestat:mobility&resilience&recovery&discipline:>=13.25) or
        (basestat:mobility&resilience&recovery&strength:>=13.25) or
        (basestat:mobility&resilience&intellect&discipline:>=13.25) or
        (basestat:mobility&resilience&intellect&strength:>=13.25) or
        (basestat:mobility&resilience&discipline&strength:>=13.25) or
        (basestat:mobility&recovery&intellect&discipline:>=13.25) or
        (basestat:mobility&recovery&intellect&strength:>=13.25) or
        (basestat:mobility&recovery&discipline&strength:>=13.25) or
        (basestat:mobility&intellect&discipline&strength:>=13.25) or
        (basestat:resilience&recovery&intellect&discipline:>=13.25) or
        (basestat:resilience&recovery&intellect&strength:>=13.25) or
        (basestat:resilience&recovery&discipline&strength:>=13.25) or
        (basestat:resilience&intellect&discipline&strength:>=13.25) or
        (basestat:recovery&intellect&discipline&strength:>=13.25)) -basestat:fourthhighest:<10)

        -(basestat:mobility&resilience&recovery&discipline&intellect&strength:>=9 basestat:sixthhighest:>5 basestat:highest:<15)
    )

    or
        (is:classitem energycapacity:<=5 -is:modded -is:locked -(source:raid -is:dupelower -source:dcv))
    or
        (is:armor is:sunset)
    or
        (is:armor is:blue -(name:"war mantis" is:gauntlets))	
    or
        ((is:armor or is:weapon) and (is:common or is:uncommon))
    )
    -(is:tagged -tag:junk) -is:maxpower -power:pinnaclecap -is:inloadout -is:masterwork -(is:armor -is:armor2.0)
    )  or (tag:junk -is:maxpower)
    )

</details>
    
<details>
    <summary>New Item Checking</summary>
    
    ("New Item Checking" or (-(-is:armor -is:weapon) -is:classitem -is:maxpower is:new))
</details>
    
<details>
    <summary>Top 0.01% of all Armor</summary>
    
    "Top 0.01% of all Armor" or is:armor -is:classitem ((((basestat:mobility&resilience:>=26 ) or (basestat:mobility&recovery:>=26 ) or (basestat:mobility&discipline:>=26 ) or (basestat:mobility&intellect:>=26 ) or (basestat:mobility&strength:>=26 ) or (basestat:resilience&mobility:>=26 ) or (basestat:resilience&recovery:>=26 ) or (basestat:resilience&discipline:>=26 ) or (basestat:resilience&intellect:>=26 ) or (basestat:resilience&strength:>=26 ) or (basestat:recovery&mobility:>=26 ) or (basestat:recovery&resilience:>=26 ) or (basestat:recovery&discipline:>=26 ) or (basestat:recovery&intellect:>=26 ) or (basestat:recovery&strength:>=26 ) or (basestat:discipline&mobility:>=26 ) or (basestat:discipline&resilience:>=26 ) or (basestat:discipline&recovery:>=26 ) or (basestat:discipline&intellect:>=26 ) or (basestat:discipline&strength:>=26 ) or (basestat:intellect&mobility:>=26 ) or (basestat:intellect&resilience:>=26 ) or (basestat:intellect&recovery:>=26 ) or (basestat:intellect&discipline:>=26 ) or (basestat:intellect&strength:>=26 ) or (basestat:strength&mobility:>=26 ) or (basestat:strength&resilience:>=26 ) or (basestat:strength&recovery:>=26 ) or (basestat:strength&discipline:>=26 ) or (basestat:strength&intellect:>=26 )) -basestat:thirdhighest:>=17) or (((basestat:mobility&resilience&recovery:>=19.66 ) or (basestat:mobility&resilience&discipline:>=19.66 ) or (basestat:mobility&resilience&intellect:>=19.66 ) or (basestat:mobility&resilience&strength:>=19.66 ) or (basestat:mobility&recovery&discipline:>=19.66 ) or (basestat:mobility&recovery&intellect:>=19.66 ) or (basestat:mobility&recovery&strength:>=19.66 ) or (basestat:mobility&discipline&intellect:>=19.66 ) or (basestat:mobility&discipline&strength:>=19.66 ) or (basestat:mobility&intellect&strength:>=19.66 ) or (basestat:resilience&recovery&discipline:>=19.66 ) or (basestat:resilience&recovery&intellect:>=19.66 ) or (basestat:resilience&recovery&strength:>=19.66 ) or (basestat:resilience&discipline&intellect:>=19.66 ) or (basestat:resilience&discipline&strength:>=19.66 ) or (basestat:resilience&intellect&strength:>=19.66 ) or (basestat:recovery&discipline&intellect:>=19.66 ) or (basestat:recovery&discipline&strength:>=19.66 ) or (basestat:recovery&intellect&strength:>=19.66 ) or (basestat:discipline&intellect&strength:>=19.66 )) -basestat:fourthhighest:>=14) or (((basestat:mobility&resilience&recovery&intellect:>=15.5 ) or (basestat:mobility&resilience&recovery&discipline:>=15.5 ) or (basestat:mobility&resilience&recovery&strength:>=15.5 ) or (basestat:mobility&resilience&intellect&discipline:>=15.5 ) or (basestat:mobility&resilience&intellect&strength:>=15.5 ) or (basestat:mobility&resilience&discipline&strength:>=15.5 ) or (basestat:mobility&recovery&intellect&discipline:>=15.5 ) or (basestat:mobility&recovery&intellect&strength:>=15.5 ) or (basestat:mobility&recovery&discipline&strength:>=15.5 ) or (basestat:mobility&intellect&discipline&strength:>=15.5 ) or (basestat:resilience&recovery&intellect&discipline:>=15.5 ) or (basestat:resilience&recovery&intellect&strength:>=15.5 ) or (basestat:resilience&recovery&discipline&strength:>=15.5 ) or (basestat:resilience&intellect&discipline&strength:>=15.5 ) or (basestat:recovery&intellect&discipline&strength:>=15.5 )) -basestat:fifthhighest:>=12) or (((basestat:mobility&resilience&recovery&discipline&intellect:>=12.8) or (basestat:mobility&resilience&recovery&discipline&strength:>=12.8) or (basestat:mobility&resilience&recovery&intellect&strength:>=12.8) or (basestat:mobility&resilience&discipline&intellect&strength:>=12.8) or (basestat:mobility&recovery&discipline&intellect&strength:>=12.8) or (basestat:resilience&recovery&discipline&intellect&strength:>=12.8)) -basestat:sixthhighest:>=12 ) or (basestat:mobility&resilience&recovery&discipline&intellect&strength:>=11 basestat:sixthhighest:>5 basestat:highest:<15))	
</details>


## [Vault Cleaner]

Figure out which weapon and armor rolls you should keep
and which you should shard.

Vault Cleaner just locks/unlocks the results for you,
so you can dismantle the items yourself.

I usually start here and then fine-tune the results with God Roll Finder.

## [God Roll Finder]

Compare your drops with 1) expert wisdom (same as DIM) and 2) community-selected perks.
    
```
Array.from(document.querySelectorAll('.weapon-type')).forEach(container => Array.from(container.querySelectorAll('.roll')).sort((a, b) => a.querySelector('.item-title').querySelector('strong').innerText.localeCompare(b.querySelector('.item-title').querySelector('strong').innerText)).forEach(node => container.appendChild(node)))
```

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
