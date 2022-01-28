# Overview

Are your (non-domestic) slaves refusing to take Technician jobs?  This mod will get them back to work producing energy for their owners.

# Changes

As of Stellaris version 3.3 "Libra," this mod overrides _only_ the `technician` job.  The only change to the job is to modify the weight condition for enslaved Pops (that are not domestic slaves).  The condition was incorrectly a `NOR` which requires every condition to be false (in this case, four flavors of energy production traits) - which means that slaves _without_ energy-enhancing traits more strongly preferred being technicians.  This is the intuitively opposite of what should be happening.  To fix this inverted rule, the condition is changed to an `OR` which correctly applies the bonus weight when an eligible Pop has any of the eligible traits.

## Compatibility

**If you use StarNet AI or StarTech AI, you do not need this mod.**  In fact, it may undo custom job re-weighting in that mod for the `technician` job.

Because this mod only overwrites the `technician` job, it is compatible with practically any other Stellaris mod that doesn't make changes to the same job.

Built for Stellaris version 3.3 "Libra." Not compatible with achievements.

### When to Install

This mod can be safely added or removed from your savegame after the game has started.  It only alters one worker job to fix the weight.  If you remove it, your game will work normally.

## Changelog

* 1.0.0 Initial Version
* 1.0.1 Added incompatibility warning to README/description
* 2.0.0 Compatible with Stellaris version 3.0.3
* 2.0.1 Remove extra images files to keep distribution lightweight (no script changes)
* 3.0.0 Updated for Stellaris version 3.1.1 "Lem" - no functionality changes, integrated underlying game changes
* 3.0.1 Verify compatibility for Stellaris version 3.1.2 - no code changes
* 4.0.0 Updated for Stellaris version 3.2.1 "Herbert" - no functionality changes, integrated underlying game changes
* 4.0.1 Mark as compatible with Stellaris version 3.2.2 "Herbert" - the game patch had no script changes
* 4.0.2 Update `mortal_initiate` job trigger
* 5.0.0 Updated for Stellaris version 3.3 "Libra" - the game now allows for single-job overwrites, so this mod has **much**-increased compatibility with other mods

## Source Code

[Hosted on Github](https://github.com/corsairmarks/technician_slave_fix)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.