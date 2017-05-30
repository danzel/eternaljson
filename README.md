Eternal JSON
============

JSON file containing all of the cards and text from the [Eternal Card Game](https://www.eternalcardgame.com/).

Spec
====

The eternal.json file is an array of all the cards.  
```
[
	{
		"set":       String     The set of cards where this card appears
		"name":      String     Name of the card
		"text":      String     Text of the card, semi-colon indicates a line-break, can contain icon indicators, eg. {T}
		"cost":      Integer    Power cost of the card 
		"influence": String     Amount of influence needed to cast the card, uses the following: {T} {P} {S} {F} {J}
		"colors":    String[]   Full words of the colors of the cards, no duplicates
		"rarity":    String     Legendary, Rare, Uncommon, Common, or Basic (for basic Sigils)
		"attack":    Integer    Only available if it is a unit or weapon
		"health":    Integer    Only available if it is a unit or weapon
		"type":      String     Curse, Fast Spell, Power, Relic, Relic Weapon, Spell, Unit, or Weapon
		"subtypes":  String[]   Only available if it is a unit
		"num":       Integer    Internal number used by the Eternal client for importing and exporting
		"__id":      Integer    Internal ID used by my database
	},
	...
]
```

Text formatting notes
=====================

Include the fullstops at the end of lines.

Use `;` to break up lines of text. Example: `Deadly; Summon: You gain 5 Health.`

Use `{T} / {P} / {S} / {F} / {J}` to show the influence icons. Example: `Summon: You gain {T} {J}.`

When new versions are released
==============================

1. Copy the current latest version and update the version number.
2. Make changes 
3. Send a PR with the new file (and old file still there)

We accept fixes in old and new files when there are mistakes, however fixes in old files are not required.

Please use tabs for formatting the JSON file.

Thanks
======

https://www.eternaljson.com/

Dire Wolf Digital - Made Eternal