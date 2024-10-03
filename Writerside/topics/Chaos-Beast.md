# Chaos Beast

<img src="showcase_chaos_beast.png" alt="showcase_chaos_beast" title="Chaos Beast Showcase"/>

<img src="item_nether_star.png" alt="nether_star" width="32" style="inline" title="Nether Star"/> In a rare event, multiple Void Walkers can merge and create a new species: the Chaos Beast. They share a hive mind and are able to manipulate time and space on a larger scale.

<tip>This subspecies is an extension of the <img src="item_fire_charge.png" alt="demon_icon" width="32" style="inline" title="Demon Icon"/> <a href="Demon.md"/> base species.</tip>

<chapter title="Key Ability">

The Chaos Beast can right-click a redstone block to spawn a domain expansion using **aura**.
Domain expansions are spherical regions where nobody can get in or out, except the owner of the domain.
Since this mechanism works by using barrier blocks that disappear when the owner of the domain wants to enter or exit, it is possible for players to pass through the barrier with the chaos beast.

// todo domain image

Right-clicking the redstone block again will remove the domain.
Domains can intersect each other, but their center must be more than `3` blocks apart.
If they are closer, the existing domain will collapse.

<img src="graph_chaos_beast_intersection.png" alt="graph_chaos_beast_intersection" title="Chaos beast domain intersection"/>

Any chaos beast can have a specific maximum number of domain expansions at the same time, normally set to `5`.
An existing and active domain will drain `1` **aura points** per execution of the main thread (around 4/s).
This rate will, of course, multiply with the number of active domains.

<img src="graph_chaos_beast_bar.png" alt="text_chaos_beast_aura" title="Chaos Beast Aura"/>

</chapter>

<chapter title="Passive Abilities">

The passive abilities, buffs and debuffs are listed in the table below.

<table>
    <tr>
        <td width="100">Type</td>
        <td>Description</td>
    </tr>
    <tr>
        <td>✅ Buff</td>
        <td><img src="effect_night_vision.png" alt="night_vision_icon" width="32" style="inline" title="Night vision"/> Night vision at night</td>
    </tr>
    <tr>
        <td>❌ Debuff</td>
        <td>Permanent <img src="effect_slowness.png" alt="slowness_icon" width="32" style="inline" title="Slowness"/> slowness (II)</td>
    </tr>
    <tr>
        <td>❌ Debuff</td>
        <td>Touching prismarine will let every domain collapse</td>
    </tr>
    <tr>
        <td>❌ Debuff</td>
        <td>Damage in water</td>
    </tr>
</table>

</chapter>