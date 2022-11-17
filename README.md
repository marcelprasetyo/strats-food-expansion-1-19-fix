Temporary fix for Strat's Food Expansion Addon v1.5 Drinks Update, for Minecraft Bedrock 1.19

Fixes Cook Book not working and some crops unable to be planted. Includes a few minor quality of life improvements for the items being fixed, as detailed below.

## How to install

First, download this repo. If you do not use GitHub, click the green button named "Code" above (top-right) and then click Download ZIP.

Then, see the instructions below for different cases.
(In case you make some unintentional mistakes, or there is a bug which corrupts the world, feel free to backup your world first.)

### Addon already installed for a specific world

1. Copy the folder "behavior_packs" from this repo

2. Open the directory where your minecraft worlds are saved, and navigate inside the folder of your desired minecraft world (sometimes the world folder name is obfuscated, try to see the timestamp of the files inside to find out your most recently played world)

3. Paste the folder copied in step 1 there, so that the copied folder merges with "behavior_packs" in step 2 and click Yes to overwrite prompt

4. Restart the server if you are using a server

### Addon already installed globally / world behavior_packs folder empty

If the above didn't fix the problem, probably your world does not save the behavior packs under its own folder, but under the root Minecaft folder.

1. Navigate to the root directory of your minecraft installation / server directory and check that "behavior_packs" folder is there

2. Copy the folder "behavior_packs" from this repo and paste at the directory mentioned above which contains "behavior_packs" folder. Click Yes to overwrite

3. Restart the server if you are using a server

### Editing the addon's .mcaddon file itself (not recommended)

1. Unzip the original Strat's Food Expansion .mcaddon

2. Inside the BP or behaviourpack folder of the unzipped folder, there will be folders named "blocks" and "items"

3. Copy the "blocks" and "items" folders from this repo, under "behavior_packs/Strat'sFoo" and paste it in the directory in step 2, click Yes to overwrite

4. Zip the topmost folders back and rename the file extension into .mcaddon again

5. If you have never installed the addon before, skip this step. Otherwise, delete the addon folder named "Strat'sFoo" or similar which are placed *inside* your world folder or root folder's behavior_packs and resource_packs folders, if you have installed the addon before.

6. Install/reinstall the edited .mcaddon file

## Fixes

### Strat's Cook Book not working

#### Issue

When right clicking / pressing use, there is a sound effect but the page doesn't turn

#### Solution included

Instead of doing transform-item, the replaceitem command is run, as per the method in Stratospheer's Bedrock port of Tinker's Construct, v1.6

#### Added features

When sneaking, opens previous page rather than the next.

- Code is also made more consistent with regards to 'swinging' animation - now this happens for opening previous page and not for opening next page, with the exceptions of the first and last page. First and last page each does swinging animation whether for opening the next page or the previous.

### Certain crops from the addon are immediately supplanted after being planted on farmland

#### Issue

When planting a tomato, lettuce or tea crop on farmland, the farmland immediately becomes dirt and the crop reverts to become the seed item

#### Solution included

Add "minecraft:breathability":"air" line for the block definition files of these three crops. The supplanting happens because the farmland thinks the crop that was just placed on it was a solid block, and the farmland becomes dirt as is expected in vanilla minecraft. If the crop block is counted as transparent or 'air', this issue is resolved.

#### Added features

Sound effect when harvesting the lettuce and tea crops with 'interact' button just like the tomato crop

## Credits

All credit goes to the ones credited in Strat's Food Expansion Addon [mcpedl.com page](https://mcpedl.com/strat-s-food-expansion/), including Stratospheer.
