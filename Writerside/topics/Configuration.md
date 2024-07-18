# Configuration

<chapter title="Overview"/>

Project Atlas has a range of different configuration files.
All the files are located in the <code>plugins/ProjectAtlas/config/</code> folder.
However, data is stored in the <code>plugins/ProjectAtlas/data/</code>.

<table>
    <tr>
        <td>File</td>
        <td>Content</td>
    </tr>
    <tr>
        <td>general.yml</td>
        <td>Contains basic configuration fields, such as debug mode, activation of the plugin, data storage options, and more.</td>
    </tr>
    <tr>
        <td>messages.yml</td>
        <td>Contains messages that will be shown to the player. This file also includes formatting, prefixes and suffixes in the messaging system.</td>
    </tr>
    <tr>
        <td>species.yml</td>
        <td>Contains settings for the different species, for instance passives, availability, etc.</td>
    </tr>
    <tr>
        <td>spells.yml</td>
        <td>Contains all the spells where you can set the delay, mana cost. We don't recommend changing any of these values, for balancing reasons.</td>
    </tr>
    <tr>
        <td>items.yml</td>
        <td>Contains information about custom items, such as weapons and potions.</td>
    </tr>
</table>

<chapter title="Saving Data"/>

Manually editing or messing with saved data is a bit different. In most cases, overwriting the data in the storage will not work because Project Atlas uses
a system to increase performance when it comes to saving data. In fact, there are two storages that are being used.

<tabs>
<tab title="In-Memory (Short-Term)">
    The in-memory database is a virtual set of variables, like player HP, spells, classes, etc. that are stored in the memory (RAM). 95% of all operations
    will be done directly on the memory, instead of resorting to config files or databases. This increases the performance, a lot.
</tab>
<tab title="Database (Long-Term)">
    The long-term database, either a real database like MySQL or a simple .yml file, is never actually used to directly write data on. Project Atlas will load
    all the necessary data into the in-memory database when the server starts. Furthermore, whenever a new player joins, their data will also be fetched
    from the long-term storage and saved into the in-memory database, if data is present.<br/>Additionally, this data will be saved periodically, when
    a player quits, or when the server is shutting down.
</tab>
</tabs>

<chapter title="Editing the Config"/>

Project Atlas will never overwrite any configuration field, which means you only need to edit the config file(s) and restart the server. All the values will
be loaded into the in-memory database when the plugin starts.

<chapter title="Editing Data"/>

<warning title="Safety Measures">
    Only edit data directly if you know what you are doing.
    For safety measures, use in-game commands,
    such as <code>/setspecies</code> or <code>/reset</code> to edit individual players.
</warning>

To manually edit data in a config file,
make sure the server is off or make sure the player has not joined since the last server-start if you are editing
the data of an individual player.

After editing, save the file and start the server again. In case you only edited a player that has not been loaded yet, you don't need to perform any additional
steps, as the plugin will load the new data when the player joins.