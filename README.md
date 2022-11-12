Temporary fix for Strat's Food Expansion Addon v1.5, for Minecraft Bedrock 1.19

## Fixes

### Strat's Cook Book not working
Issue : When right clicking / pressing use, there is a sound effect but the page doesn't turn
Solution included : Instead of doing transform-item, replaceitem command is run, as per the method in Strat's Bedrock port of Tinker's Construct, v1.6
Added features : When sneaking, opens previous page rather than the next
Notes : Code is made more consistent with regards to 'swinging' animation - now this happens for opening previous page and not for opening next page, with the exceptions of first and last page. First and last page does swinging animation nevertheless.

### Certain crops from the addon are immediately supplanted after being planted on farmland
Issue : When planting a tomato, lettuce or tea crop on farmland, the farmland immediately becomes dirt and the crop reverts to become the seed item
Solution included : Add "minecraft:breathability":"air" line for the block definition files of these three crops. The supplanting happens because the farmland thinks the crop that was just placed was a solid block, and the farmland becomes dirt as is expected in vanilla minecraft. If the block is counted as transparent or 'air', this issue is resolved.

All credit goes to the ones credited in Strat's Food Expansion Addon [mcpedl.com page](https://mcpedl.com/strat-s-food-expansion/), including Stratospheer.
