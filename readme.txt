# Slot-Bot – What do you need to replace?

1. **Bot Token:**
   - Open the file `main.py`.
   - Find the line `bot.run("YOUR_BOT_TOKEN")` at the very bottom.
   - Replace `YOUR_BOT_TOKEN` with your own Discord bot token.(line 443)

2. **Staff Role:**
   - Open the file `config.json`.
   - Replace the value of `"staffrole"` with the ID of your desired Discord role that should have admin rights for the bot.

3. **Premium Role:**
   - In `config.json`, you can replace the value of `"premiumeroleid"` with the ID of your slot role.

4. **Guild ID:**
   - In `config.json`, you can replace the value of `"guildid"` with your Discord server's ID.

5. **Category ID:**
   - In `config.json`, you can replace the value of `"categoryid"` with the ID of the category where slots should be created.

6. **Other IDs in the code:**
   - In `main.py`, there are other places with IDs (e.g., `guild = discord.Object(id=...)) (Its in line 18). Adjust these to match your server structure if needed.

7. **Prefix:**
   - The prefix is currently set to `,` (see `command_prefix=","` in `main.py`). Change it there if you want a different prefix.