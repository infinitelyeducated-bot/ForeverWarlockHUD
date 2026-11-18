<p align="center"><img src="media/readme/hero.svg" width="100%" alt="ForeverWarlockHUD: a warlock HUD for World of Warcraft: Forever"></p>

**ForeverWarlockHUD** is a warlock HUD for World of Warcraft: Forever (Interface 16001). Open its menu with `/fwl`.
Version 2.0.0. **Not yet verified in the game client.** It starts only on a warlock.

Every panel below is drawn on this class's menu backdrop. Under each one, "Text version" holds the
same words as plain text.

<p align="center"><img src="media/readme/01-install.svg" width="100%" alt="Install and first run"></p>

<details>
<summary>Text version: Install and first run</summary>

- **1. Get it** - Download this repository (Code, Download ZIP) or clone it.
- **2. Place it** - Put the folder in World of Warcraft/_forever_/Interface/AddOns/ and name it exactly ForeverWarlockHUD.
- **3. Start** - Restart the game or type /reload, then type /fwl to open the menu.
- **Only on a warlock** - On any other class this HUD stays completely off: nothing on screen, nothing saved, and /fwl just says which class it is for. You can leave every class's HUD enabled.
- **Optional: ForeverArt** - Adds the painted backdrop, header picture and class crest to the menu. The HUD works without it.

**Set up in five minutes**

- **Open** - /fwl. The grid appears and every HUD item can now be grabbed.
- **Choose abilities** - Abilities tab: tick On for each ability you want an icon for.
- **Arrange** - Hold CTRL and the left mouse button on a bar or icon and put it where you want it. CTRL + wheel sizes it.
- **Dress it** - Skins tab: pick a skin, or click a colour in the strip to make your own.
- **Keep it** - Profiles tab: type a name and press Save. Close the menu with Escape.

</details>

<p align="center"><img src="media/readme/02-mouse.svg" width="100%" alt="Mouse controls"></p>

<details>
<summary>Text version: Mouse controls</summary>

These work only while the menu is open and Lock is off. Point at any bar or icon: it lights up and a tooltip names it.

- **Move** - Hold CTRL, then hold the LEFT mouse button on the item. It sticks to the cursor until you let go.
- **Size** - Hold CTRL and roll the MOUSE WHEEL over the item. Up is bigger, down is smaller (0.2x to 4x).
- **Turn** - Hold CTRL, then hold the RIGHT mouse button on the item and drag around it. It stays as you leave it.
- **Straighten** - Double-click the RIGHT mouse button on the item: back to its original orientation.
- **What turns how** - Icons turn to any angle, with a soft stop on the quarter turns. Bars and the recent-actions row turn in quarter turns, because the game cannot draw a bar at an angle. Text always stays upright.
- **Grid, snap, stick** - The grid shows while the menu is open. Snap drops an item on the nearest grid line; Stick makes an item dropped right beside another one click against its edge.
- **Menu closed** - Nothing can be clicked or moved, so the HUD never gets in the way of the game.

Position and turning are done with the mouse; size is done both ways: CTRL + wheel on the item, or the Scale slider in the menu (one for each bar and each icon). The menu has no X / Y or orientation controls.

</details>

<p align="center"><img src="media/readme/03-hud.svg" width="100%" alt="Configuration guide: the HUD tab"></p>

<details>
<summary>Text version: Configuration guide: the HUD tab</summary>

**Whole HUD**

- **Show HUD** - Everything on or off.
- **Lock** - Stops all mouse editing, so a stray CTRL-click cannot move anything.
- **Auto-hide out of combat** - Hides the whole HUD until combat starts. The open menu always shows it.
- **Auto-hide combo at 0** - Hides the combo points while you have none and are out of combat.
- **Snap items to grid / Grid size** - Drops land on the grid; Grid size (8 to 64) sets the spacing.
- **Join energy, regen and swing into one bar** - Switch on from the HUD tab. The regen overlay sits on the energy bar and the swing strip runs under it; the three move and scale together. Each keeps its own colours and options.
- **Stick items together** - A drop right next to another item abuts its edge. Needs Snap on.

**Each element: Mana bar, Mana regen, Swing timer, Combo points, Recent actions**

- **Show** - The switch on the right of the element's heading.
- **Width / Height** - The shape of the bar or of one pip or icon.
- **Opacity** - 0.1 to 1.
- **Scale** - Size of the whole item, 0.5 and up, with no maximum. The same value as CTRL + wheel on the item. Hold CTRL and roll the wheel over this slider to step it by 0.25.

**Mana bar and Mana regen**

- **Show the value as text** - The number on the bar, on or off.
- **Show mana / sec** - The rate printed on the regen bar.
- **Full at** - The rate per second at which the regen bar is completely full (5 to 60).

**Swing timer**

- **Use skin colour, Bar red / green / blue** - Take the bar colour from the skin, or mix your own.
- **Background opacity** - How solid the empty part of the bar is.
- **Spark, Spark size** - The bright marker at the moving edge, and its size (8 to 40).
- **Text and its mode** - Off, or one of: elapsed / total, remaining, percent.
- **Ticks, Tick count** - Marks across the bar (1 to 10).
- **Ready flash** - The bar glows for the last 0.2 seconds of a swing.
- **Source** - Where the swing length comes from: the swing event, or polling your attack speed.
- **Reset on target change** - A new target restarts the bar.
- **Manual speed override, Manual speed** - Force a swing length (0.5 to 4 s), for testing.

</details>

<p align="center"><img src="media/readme/04-abilities.svg" width="100%" alt="Configuration guide: the Abilities tab"></p>

<details>
<summary>Text version: Configuration guide: the Abilities tab</summary>

**Notifications on every icon (one switch each)**

- **Show countdown numbers** - Time left in the icon's bottom-right corner, to the hundredth of a second under a minute.
- **Clock sweep** - The shadow that sweeps round the icon while it is on cooldown.
- **Darken on cooldown** - The picture goes dark and grey until the ability is back.
- **Flash when ready** - The border pulses once when a cooldown ends.
- **Glow while the effect is on you** - Lit while the ability's own buff is active.
- **Dim when you cannot use it** - For example not enough mana.
- **Red when out of range** - The target is too far away.

**Each ability (33 of them)**

- **On** - Gives the ability an icon. New icons appear in a grid above the HUD; move them with the mouse.
- **Opacity** - 0.1 to 1 for that icon.
- **Scale** - Size of this icon, 0.5 and up, with no maximum. The same value as CTRL + wheel on the icon. Hold CTRL and roll the wheel over this slider to step it by 0.25.

On by default: Death Coil, Howl of Terror, Soul Fire, Shadow Ward. The full list with spell IDs is at the end of this page.

</details>

<p align="center"><img src="media/readme/05-look.svg" width="100%" alt="Configuration guide: the Skins tab"></p>

<details>
<summary>Text version: Configuration guide: the Skins tab</summary>

**Menu artwork (needs ForeverArt)**

- **Menu artwork** - High resolution, Low resolution or Off.
- **Header picture** - Painted or Alternate.

**Your own colours**

- **The colour strip** - Ten colours: resource bar, swing bar, bar background, spark, text, accent, borders, window background, combo points, icon border. Click one to open a colour wheel.
- **Colour wheel** - Pick on the wheel and the brightness bar. Changes show at once. Done keeps it, Cancel puts the old colour back.
- **Opacity** - The four see-through parts (bar background, borders, window background, icon border) also get an Opacity slider.
- **Custom colours** - Tick to use your colours, untick for the plain skin. A part you have not coloured keeps the skin's colour.
- **Save / Load / Delete** - Type a name and press Save to keep a colour set (up to 40). Load lists the saved sets. They survive Reset to default.

**Skins**

- **40 skins** - Click one. A skin is a palette plus an edge style (flat, line, bevel, rune, ember, frost, gilded). It only recolours; it never moves or resizes anything.

</details>

<p align="center"><img src="media/readme/06-profiles.svg" width="100%" alt="Configuration guide: Profiles and saved settings"></p>

<details>
<summary>Text version: Configuration guide: Profiles and saved settings</summary>

- **Save** - Type a name (up to 32 characters) and press Save. Saving over an existing name asks first. Up to 40 profiles.
- **Load / Delete** - Select a profile in the list, then Load or Delete. Delete asks first and does not change the HUD.
- **What a profile holds** - Every item's place, size, rotation, opacity and on/off state, the swing and regen options, notifications, skin and custom colours.
- **Reset to default** - Top right of the menu. Asks first, and keeps your saved profiles and colour sets.
- **Where it is stored** - WTF/Account/<your account>/SavedVariables/ForeverWarlockHUD.lua. Copy that file to move your setup to another PC.
- **Only while the menu is open** - Saving and loading, like moving things, need the menu open.

</details>

<p align="center"><img src="media/readme/07-commands.svg" width="100%" alt="Commands"></p>

<details>
<summary>Text version: Commands</summary>

| Command | What it does |
|---|---|
| `/fwl` | Open or close the menu. |
| `/fwl help` | Open the Help tab, which explains all of this in game. |
| `/fwl abilities \| skins \| profiles` | Open that tab. |
| `/fwl show \| hide` | Whole HUD on or off. |
| `/fwl energy\|regen\|swing\|combo\|trail on\|off` | One element on or off. "energy" is the mana bar, "trail" the recent-actions row. |
| `/fwl cooldown on\|off` | Countdown numbers. |
| `/fwl lock \| unlock` | Mouse editing off or on. |
| `/fwl sticky \| grid` | Toggle Stick and Snap. |
| `/fwl skin <name>` | Apply a skin by name. |
| `/fwl save <name> \| load <name>` | Profiles (the menu must be open). |
| `/fwl reset` | Reset to default, after asking. |

</details>

<p align="center"><img src="media/readme/08-limits.svg" width="100%" alt="Good to know"></p>

<details>
<summary>Text version: Good to know</summary>

- **Status** - Version 2.0.0. Not yet verified in the game client: it passes a mocked-client test suite and boots cleanly in a simulated UI, but nobody has confirmed it in the real game.
- **Rotation** - Bars turn in quarter turns only, and a turned icon's border, sweep and number stay upright.
- **Combat secrecy** - Glow, dim and red tint depend on what the game will tell an addon. In combat it may withhold those answers; the icon then stays plain. A cooldown it will not reveal shows no number.
- **Spell IDs** - The IDs listed are rank 1 and only a fallback: at login the addon asks the game for the ID behind each spellbook name, so an icon follows the rank you know.
- **Rules it keeps** - Public API only. No protected calls, no combat automation, no combat log, nothing written outside its own saved settings.
- **How it is built** - One generator produces all nine class HUDs from a single reference, with a mocked-client test suite, a Lua 5.1 limits check and a simulated-UI run on every build.

</details>

<details>
<summary>All 33 abilities and their fallback spell IDs</summary>

| Ability | Fallback ID | Default |
|---|---|---|
| Death Coil | 6789 | on |
| Howl of Terror | 5484 | on |
| Soul Fire | 6353 | on |
| Shadow Ward | 6229 | on |
| Fear | 5782 | off |
| Life Tap | 1454 | off |
| Banish | 710 | off |
| Inferno | 1122 | off |
| Curse of Agony | 980 | off |
| Curse of the Elements | 11723 | off |
| Curse of Shadow | 402791 | off |
| Corruption | 172 | off |
| Immolate | 348 | off |
| Drain Life | 689 | off |
| Drain Soul | 1120 | off |
| Searing Pain | 5676 | off |
| Rain of Fire | 5740 | off |
| Hellfire | 1949 | off |
| Incinerate | 412758 | off |
| Bane of Havoc | 1225228 | off |
| Wrack | 1316697 | off |
| Shadowburn | 17877 | off |
| Conflagrate | 17962 | off |
| Siphon Life | 18265 | off |
| Amplify Curse | 18288 | off |
| Fel Domination | 18708 | off |
| Shadow Bolt | 686 | off |
| Demon Armor | 706 | off |
| Demon Skin | 687 | off |
| Summon Imp | 688 | off |
| Summon Voidwalker | 697 | off |
| Summon Succubus | 712 | off |
| Summon Felhunter | 691 | off |

</details>
