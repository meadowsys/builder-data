# Builder Data

NOTE: this is currently a draft/experiment, and there are absolutely zero stability guarantees. This repo's format can and will evolve over time as we toy around with things. More explanation as to what this is may come in the future.

## Current plan

### Definitions

WIP

- **Data source** (uncertain of this name): A repository of textures and options.
- **Texture**: a grouping of options, which would almost always be a single block or item. (A texture might be allowed to affect more than one block/item, but this is not fleshed out yet and end up not actually being a thing.) Textures are placed in the directory `textures`, with its filepath acting as its pack builder identifier for grouping options together. For example, `minecraft:stone` should probably be put at `textures/minecraft/stone`, and has intuitively a pack builder ID of `minecraft/stone`.
- **Namespace**: Represented by a subdirectory in the `textures` dir. For example, `minecraft/stone` is in the namespace of `minecraft`. (For organisation purposes, we are considering allowing a subdirectory to be marked as "collapsed" in a manifest, which allows better organisation in sub directories. For example, `minecraft/stone` can actually be placed in the directory `textures/minecraft/blocks/stone`, where `blocks` is marked to be collapsed.) Usually the first namespace would be the "mod id" (eg. `minecraft`).
- **Option**: One choice of potentially many for a texture.
- **Provider**: One of potentially many providers for a texture. These contain the real instructions for pack builder as to how to represent this texture in the output pack. A provider can provide for many different MC versionss, meaning less maintenance burden for pack authors.
- **Preset**: A list of options chosen for textures, to act either as a compiled list of options for a complete resource pack, or a baseline starting point in which users can add or override their own texture choices on top of it. Presets can be provided by data sources, as standalone files, or as preset repositories containing one or more presets.
- **Addon**: A data source designed to be added on top of other data sources, adding options to textures.

## Unanswered Questions

None so far..

## Some misc details

This commit is the commit we will pin ourselves to when porting over the initial data, for consistency reason. After we're done with this initial version, we can update/backport to newer/older commits.

Current target commit in L&T main repo: `3cc361aeb777d11847c20ed5629fb909f55f1ca9`

<!--
The below is for checking the repo history for older versions of textures that could get added here as variants. For later!

- Newest commit checked: todo
- Oldest commit checked: todo
-->
