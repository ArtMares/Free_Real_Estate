# **This mod has been tested pretty thoroughly but may still break your save or have other problems since it's new. Please keep backups.**

# General info

## What is this?
This is a mod that allows you to build "factory buildings", which are buildings you can enter that are 36x36 inside.

## Why "free real estate"?
https://www.youtube.com/watch?v=cd4-UnU8lWY

## Changes for 1.1 (If/when I have time and interest again)

- Logistic input support, in the meantime just use a normal item relay and inserters.
- Belt inputs; I've figured out a way to do this now but I don't have time to add it.
- More factory sizes, more complicated production chain to create different kinds of factories. I'm open to suggestions!
- Power production building, which relays power created from inside to the outside.
- Icon selection that allows you to set a detail view (alt button) icon on top of the factory outside.

## IMPORTANT NOTES
- **Factories are not intended to be placed by construction robots. It should be impossible, but if another mod forces them to be placed expect undefined behavior.**
- I highly suggest using this with [Bob's Adjustable Inserters](https://mods.factorio.com/mods/Bobingabout/bobinserters) since item throughput is limited by how fast you can put items into and out of chests.
- Fluid relays do NOT exert any pressure in any direction. They are, on both sides, just storage tanks. This is intentional. If you want to move fluids you need to use pumps.

## How is this different from Factorissimo?

This mod was written from scratch and performs a lot better, but since I redesigned the mod from the ground up with different ideas many things are different.

The main differences:

- There is no way to produce power inside a factory and relay it outside. (Factorissimo's "power plants")
- Players can no longer be inside a factory when another player has picked it up.
- Buildings inside factories will not function when a factory has been picked up.
- There is no limit to the number of factories you can build. (Factorissimo was limited to 255, and would corrupt your save afterwards)
- Factories perform better, so you can use a lot of factories without lagging your map. Performance is directly related to how much stuff is moving through relays into and out of factories. Fluid and circuit relays are much faster than items, but even items are very fast.
- Factories are a bit more expensive and complex to make.

## What features does this mod have?

- Works in multiplayer.
- Item, fluid, and circuit relays to move things into and out of factories. These are directional, and can be configured from inside the factory.
- Pollution will be moved from inside the factory to wherever the factory has been placed.
- Factories can be placed inside factories if the recursion setting is enabled. This is disabled by default.
- Factory relays can link directly to each other. (If you place two factories touching each other their relays will link to the relay at that position in the other factory)
- Circuit relays allow you to send signals in and out of factories. (These run once every 2 seconds)
- Item relays correctly respect the "bar", the red X you can use on chests. If you set a bar on an output the input direction won't keep sending items you don't want.
- Fluid relays properly mix temperatures.
- Factories can be renamed. Names will show both on the building mouseover. (see [here](https://github.com/sirenfal-factorio/Free-Real-Estate/blob/master/Screenshots/outside_1.jpg)) and on the item tooltip when picked up.
- Factories which are empty will be un-named and will stack back with normal un-placed factory items.
- Several configurable settings. (see config.lua)

## Can you add support for other factory sizes?

Support for other factory sizes is already done, but I haven't decided what sizes to use and I don't have graphics for other factory sizes. I'm open to suggestions. Recipes probably need tweaking too.

If you're absolutely desperate for another factory size you can edit the `FACTORY_SIZE` constant at the top of the `factory\factory.lua` file. Changing this on an existing map should be safe, but you should back up your save first just in case. If you use it on an existing map factories that have already been placed will use the old size, and new factories will use the new size.

## Besides the factory building itself your graphics suck

Right? I'm a programmer, not an artist.




# Usage

## How do I enter a factory?
Walk near the door (or factory exit) and press your pick up item key.

![The outside of a factory](https://github.com/sirenfal-factorio/Free-Real-Estate/blob/master/Screenshots/outside_1.jpg)

## How do I get started once I'm inside?

Click on a selector on the left, top, or right wall and choose an item, circuit, or fluid input or output. Then hit the green refresh button on the left side of your screen to spawn your selected choices.

![The outside of a factory](https://github.com/sirenfal-factorio/Free-Real-Estate/blob/master/Screenshots/configure_1.jpg)

## How do I rename a factory?

Use the pencil icon next to the refresh icon when you're inside a factory.




# Final

## What do I do if I crash or experience a bug?

Please contact me (Sirenfal) with a copy of the save file and exactly what you did to the best of your knowledge (steps to reproduce).

## Credits

Thanks to...

- ElfLeaderMike: For helping me test repeatedly
- MagmaMcFry: The original Factorissimo author, for the idea and the original mod
- A graphic artist I commissioned to make the factory building model, who has asked to remain anonymous
- `[10:09:30 PM] Warchamp7: 1. I want credit I probably did something` Yeah, he probably did :D
- Brathahn: Factorio forum user who reported and helped fix several issues with the original alpha version.
- iulianov: Pull request that fixed a save corruption bug

- AmCh-Q: Submitted zh-CN and zh-TW localizations for the mod.

## License

All code is licensed under the [MIT Public License](https://opensource.org/licenses/mit-license.php). All graphical assets belong solely to Sirenfal and are not covered under this license. You are free to play with this mod as released, including the graphical assets, but you may not reuse or redistribute the graphical assets without explicit permission.
