# Overview

Are your (non-domestic) slaves refusing to generate energy credits?  This mod will get them back to work producing wealth for their owners.

# Changes

This mod replaces the `common/pop_jobs/03_worker_jobs.txt` file that defines most worker-strata jobs.  The only change is to
modify the weight condition for the `technician` job for enslaved populations (that are not domestic slaves).  The condition was incorrectly
a `NOR` which requires every condition to be false (in this case, four flavors of energy credit traits) - this means that slaves **without**
energy-enhancing traits will more strongly prefer being technicians.  This is the opposite of what should be intuitively happening.  To fix
this inverted rule, the condition is changed to an `OR` which applies the bonus weight when an eligible pop has any of the eligible traits.

## Compatibility

**If you use StarNet AI, you do not need this mod.**  In fact, it will mess up the custom job re-weighting in that mod because they alter the same file.

Because it replaces a core Stellaris file, this mod is inherently incompatible with any other mods that overwrite the same file.  Generally,
any mod that alters the default worker jobs will not be compatible with this one.  Altering jobs for other strata should work as expected
because they are defined in other files.

This mod is not compatible with achievements because it overwrites a core Stellaris file.

### Post-Game Start

This mod can be safely added or removed from your savegame after the game has started.  It only alters one worker job to fix the priority.  If you remove it, your game will work normally.

## Changelog

* 1.0.0 Initial Version
* 1.0.1 Added incompatibility warning to README/description
* 2.0.0 Compatible with Stellaris version 3.0.3

## Source Code

[Hosted on Github](https://github.com/corsairmarks/technician_slave_fix)

### Development Notes

It is best to clone this repository in a directory _other_ than `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder in this repository via a `*.mod` file's `path` property.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.