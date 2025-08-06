
# RoCommand ⚙️

A Discord bot designed for Roblox moderation, featuring commands to ban, unban, kick Roblox users, and manage role-based permissions. The bot uses JSONBin for remote configuration and stores ban/kick data securely with API keys.

| Command      | Description                               | Usage Example                                               | Permissions                 |
|--------------|-------------------------------------------|-------------------------------------------------------------|-----------------------------|
| `/whitelist` | Whitelist a role for moderation commands | `/whitelist @Role`                                          | Server Owner only            |
| `/ban`       | Ban a Roblox user with reason and proof clip | `/ban 123456 "Cheating" https://clip.url`                  | Whitelisted roles           |
| `/unban`     | Unban a Roblox user by user ID            | `/unban 123456`                                             | Whitelisted roles           |
| `/kick`      | Kick a Roblox user briefly by adding to kick list | `/kick 123456`                                          | Whitelisted roles           |
| `/get`       | Get current ban info for a Roblox user    | `/get 123456`                                              | Whitelisted roles           |
| `/tutorial`  | Show tutorial on setting up the bot       | `/tutorial`                                                | Server Owner only            |
| `/config`    | Configure server's API keys                | `/config` (interactive modal)                              | Server Owner only            |
| `/invite`    | Get the bot invite link and credits        | `/invite`                                                 | Everyone                    |

# How to Setup the Bot 🔨

- Invite the bot using [this](https://discord.com/oauth2/authorize?client_id=1402372113175941210&permissions=2617502769&integration_type=0&scope=bot) link.
- Create an account on https://jsonbin.io.
- Once created, go to https://jsonbin.io/app/bins and create 2 new bins. Use the placeholders below in the bin. Save these somewhere safe.

**Ban Placeholder:**

```json
[
  {
    "userid": 1,
    "reason": "Example ban",
    "clip": "https://example.com/proof.png",
    "author": 123456789012345680
  }
]
```
**Kick Placeholder:**
```json
[
  {
    "userid": 0,
    "kicked_by": ""
  }
]
```
- Go to https://jsonbin.io/app/app/api-keys and copy your "X-Master-Key". This allows the bot to access your bins.
- Use the config command on the bot and press "Edit Config", and fill out the information. 
- Use the whitelist command to set up the roles allowed to use ban, kick, unban and get commands.

# How to Setup the Roblox stuff! 🔨
- Once the bot is set up, head to [this](https://create.roblox.com/store/asset/130010432442031/RoCommand) link to get the RoCommand server logic for roblox.
- Put this into ServerScriptService, and ensure you have enabled **Studio Access to API Services** and allowed **HTTP Requests**!
- Head to the module script called "RoCommand" inside the "Server" script, and paste your ban bin ID, kick bin ID and Master Key inside of the table! 
- Once this has all been done, the bot **should** work.

# Head to https://discord.gg/FYKASgDBJg for further assistance.
