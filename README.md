# 🌀 ConicSpawn

**An ultra-lightweight, blazing-fast spawn plugin with advanced optimization and full customization support.**
Perfect for any Minecraft server, from small survival worlds to large-scale networks.

## [**Modrinth**](https://modrinth.com/plugin/conicspawn)
[**Report Bugs & Get Support**](https://discord.gg/JvVv7wHQc7)

---

## 📥 Installation

1. Download the latest **ConicSpawn** `.jar` from Modrinth or your preferred source.
2. Place it inside your server’s `plugins/` folder.
3. Restart or reload your server.
4. Configure `config.yml` and `messages.yml` to your liking.
5. Set your spawn point with:
   ```
   /setspawn
   ```

---

## 📌 Features

- ⚡ **Lightning-fast teleports** with optional countdown delay
- 🛡 **Teleport safety** – cancel teleport if the player moves or takes damage
- 🔊 Fully customizable **sounds, messages, and action bar displays**
- 🧹 Lightweight & performance-friendly
- 🔄 `/conicspawn reload` command to reload configs without restarting
- 🎯 **First join, join, leave, and respawn at spawn** events (toggleable)
- 📜 Configurable **commands to execute on teleport**
- 📍 Show exact **spawn coordinates** when setting spawn
- 🔒 Permission-based command system

---

## 🖥 Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `/spawn` | Teleport to spawn | `conicspawn.spawn` |
| `/setspawn` | Set the spawn location | `conicspawn.admin` |
| `/conicspawn reload` | Reload configuration files | `conicspawn.admin` |

---

## 🔑 Permissions

| Permission | Description | Default |
|------------|-------------|---------|
| `conicspawn.admin` | Allows using `/setspawn` and `/conicspawn reload` | OP |
| `conicspawn.spawn` | Allows using `/spawn` | True |

---

## ⚙ Configuration

### `config.yml`
```yaml
# ==========================
# ConicSpawn Configuration
# ==========================
# Time in seconds before a player is teleported to spawn.
teleport-delay: 3

# The sound played every second during the teleport countdown.
countdown-sound: BLOCK_NOTE_BLOCK_PLING

# The sound played when the player is teleported to spawn.
teleport-sound: ENTITY_ENDERMAN_TELEPORT

# Whether to send messages in the player's chat.
chat-message: true

# Whether to send countdown messages in the action bar.
actionbar-message: true

# Toggle if teleport commands should be executed
commands: true
teleport-commands:
  - 'tellraw {player} "§fHey §b§l{player}§f, Configure commands from §3config.yml"'
  - 'give {player} diamond 1'
```

---

### `messages.yml`
```yaml
# ==========================
# ConicSpawn Messages
# ==========================
prefix: "&b&lConic &8»"

no-permission: "{prefix} &cYou do not have permission."
set-spawn: "{prefix} &fYou have set spawn at &b{spawnlocation}&f."
spawn-not-set: "{prefix} &fSpawn is &cnot&f set!"
teleport-countdown: "{prefix} &fTeleporting in &b{seconds}&f seconds..."
teleport-complete: "{prefix} &fTeleported to &bspawn&f."
actionbar-message: "&fTeleporting to spawn in &b{seconds} &fsec."
```

---

## 🔄 Placeholders

| Placeholder | Description |
|-------------|-------------|
| `{prefix}` | The prefix from `messages.yml` |
| `{seconds}` | Countdown seconds remaining |
| `{spawnlocation}` | Spawn coordinates (X, Y, Z) |
| `{player}` | Player name |

---

## 🛠 How to Use

1. **Set Spawn**
   ```
   /setspawn
   ```
   Saves the current location as the spawn point.

2. **Teleport to Spawn**
   ```
   /spawn
   ```
   Teleports you (with countdown if enabled) to the spawn point.

3. **Reload Configurations**
   ```
   /conicspawn reload
   ```
   Reloads `config.yml` and `messages.yml` without restarting the server.

---

## ⚡ Performance

- Zero lag impact — runs async where possible.
- No unnecessary event listeners when features are disabled.
- Efficient cache usage and automatic cleanup.

---

## 📜 License

This project is licensed under the MIT License.

---

## 🤝 Contributing

We welcome contributions! Feel free to submit a pull request or open an issue.
[**Report Bugs & Request Features**](https://discord.gg/JvVv7wHQc7)

---

## ⭐ Support
If you like this plugin, consider leaving a star ⭐ on GitHub or a review on Modrinth.
