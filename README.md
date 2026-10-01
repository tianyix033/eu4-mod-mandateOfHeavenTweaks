# MandateOfHeavenTweaks

A Europa Universalis IV mod that fixes and tunes vanilla's existing Mandate of
Heaven mechanics. Target version 1.37.5.0. Requires the Mandate of Heaven DLC.

Where MandateOverhaul (`eu4-mandate-overhaul`) adds new content, this mod is
corrective: it touches vanilla's own disasters, imperial reforms and triggered
modifiers so they behave the way they read.

## What it changes

**The nomadic border crisis.** Vanilla's disaster can only end if the horde drops
below 300 development or becomes the Emperor's subject, which means a truce leaves
it running indefinitely and the "show superiority" option goes nowhere. A truce
now ends it too, with a weaker reward than a permanent settlement and text that
does not claim more than it should — the border is safe *for now*, and the
disaster can fire again once the truce lapses.

**Celestial imperial reforms.** The gate controlling when a new reform may be
enacted sat outside the `trigger` block in several reforms, so it was silently
ignored. All 21 are corrected, with the gate moved into a scripted trigger.

**The Ming crisis disaster.** Tuning to how it starts, stops and ends.

**Triggered modifiers** and the localisation that goes with all of the above.

## Install

Copy this folder into

    Documents/Paradox Interactive/Europa Universalis IV/mod/

and create a sibling `MandateOfHeavenTweaks.mod` next to it containing the same
lines as `descriptor.mod` plus an absolute path, forward slashes:

    path="C:/Users/<you>/Documents/Paradox Interactive/Europa Universalis IV/mod/MandateOfHeavenTweaks"

EU4 ignores the launcher's load order and resolves conflicts by mod *name*, with
the earlier-sorting name winning.

## Conventions

Every line changed in a copied vanilla file carries an `@` in its trailing comment
with the previous value, so a plain text search for `@` lists everything this mod
touches. Deleted lines are commented out rather than removed. Script files are
CP-1252 with LF endings and no BOM; localisation is UTF-8 with BOM. Both matter —
EU4 fails quietly on the wrong one.

## Note

`common/disasters/` and `common/imperial_reforms/` override by filename rather
than merging, so those files are Paradox Interactive's, copied and edited in place
with the changes marked as above. This is an unofficial personal mod, not
affiliated with or endorsed by Paradox Interactive.
