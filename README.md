# Minecraft hopper sorter 26.3

Supports Purpur/Paper

Includes

- Whitelist or blacklist items on each hopper
- Craftable filter tool, or sneak + right-click if you turn the tool off in `items.yml`
- Material match, or exact match (name, lore, enchantments, custom model data) per item
- Fully configurable menu: slots, materials, names, lore, and custom model data in `gui.yml`
- Hoppers skip blocked items and keep pulling the next allowed one from chests, droppers, minecarts, and item streams
- Players can edit a hopper only when protection plugins would let them open it
- Works without NMS

Re-worked version of [JEFF-Media's Hopper-sorter](https://www.spigotmc.org/resources/filtered-hoppers.96037)

[![Click counter](https://hits.dwyl.com/InstantName2/hopper-sorter.svg?style=flat-square)](http://hits.dwyl.com/InstantName2/hopper-sorter)

## Use

Right-click a hopper with the filter tool. Put the items that hopper should accept or reject into the menu. Right-click an entry to toggle exact match. The status wool turns the filter on or off. The mode wool switches between whitelist and blacklist.

The default tool is a nautilus shell surrounded by redstone. `/hf give` gives the tool without crafting.

On Paper and Purpur, leave hopper move events enabled. If `InventoryMoveItemEvent` is disabled, hoppers move items without telling plugins and filters will not run.

## Commands

| Command | What it does | Permission |
| --- | --- | --- |
| `/hf give [player] [amount]` | Give the filter tool | `hopperfiltering.give` |
| `/hf reload` | Reload `config.yml`, `items.yml`, and `gui.yml` | `hopperfiltering.reload` |
| `/hf exact [on\|off\|toggle]` | Set exact match on every item in the open filter, or the hopper you are looking at | `hopperfiltering.exact` |

Aliases: `/hopperfiltering`, `/filteredhoppers`

`hopperfiltering.use` lets a player open and edit filters. It is granted to everyone by default.

## Files

| File | What it controls |
| --- | --- |
| `items.yml` | Tool material, name, lore, custom model data, glow, crafting recipe, and whether sneak + right-click is used instead |
| `gui.yml` | Menu title, slot layout, buttons, and exact-match text |
| `config.yml` | Chat messages, and whether filter items drop when the hopper breaks |
| `hoppers.yml` | Saved filters. Written by the plugin |
Might add a hopper speed changer/upgrade system in the future.

## Virus Total scan
https://www.virustotal.com/gui/file/663a27a09d77577331a66b71c8084500de8e5a78458a8a5b435c4782ad48f4b9?nocache=1
