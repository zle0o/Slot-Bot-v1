# Slot Bot – Advanced Slot Management Discord Bot

**Slot Bot** is a fully-featured **Discord bot** for managing premium slots within a community or server. Built with Python and `discord.py`, it automates slot creation, renewals, pings, role assignment, and more. Created and maintained by **zle0o**.

> 🛡️ **Warning**: This bot interacts with server roles, channels, and permissions. Use it only with proper understanding.

---

## 🧠 Features

- 🔧 Create and manage slot channels with time-based expiration.
- ⏱ Auto-expiration and renewal of slots.
- 🛑 Hold and unhold slot channels (e.g. during reports or conflicts).
- 📥 Assign and revoke premium roles automatically.
- 📢 Controlled ping system with usage limits.
- 🚫 Nuke command to clean slot channels.
- 📚 Embedded rule system with automated slot terms.
- 📊 Persistent JSON-based data storage.

---

## 🛠 Requirements

- Python 3.8+
- Required Python packages:
  - `discord.py`
  - `colorama`

---

## 📦 Install Dependencies

```bash
pip install -U discord.py colorama
````

---

## ⚙️ Setup

1. Clone or download this repository.
2. Replace `YOUR_BOT_TOKEN` in the `bot.run()` function with your bot token.
3. Just edit the config.json, the other files are for counting:
   * `config.json`:

     ```json
     {
       "premiumeroleid": "ROLE_ID",
       "categoryid": "DEFAULT_CATEGORY_ID",
       "staffrole": "STAFF_ROLE_ID",
       "guildid": "YOUR_GUILD_ID"
     }
     ```
   * `data.json`: `[]`
   * `pingcount.json`: `[]`
4. Run the bot:

   ```bash
   python bot.py
   ```

---

## 📘 Usage

### 💬 Commands

* `,create @user 7 d 2 category slotname` – Create a slot.
* `,renew @user #channel 7 d` – Renew a slot.
* `,add @user` – Add premium role.
* `,remove @user` – Remove premium role.
* `,hold` / `,unhold` – Restrict or re-enable messaging.
* `,delete` – Delete the current channel.
* `,revoke @user #channel` – Revoke slot access.
* `,ping @everyone/@here` – Ping with limit.
* `,nuke` – Delete all non-bot messages.
* `,help` – Show command list.

---

## ⏰ Auto Expiration

The bot checks every hour and removes access to expired slots based on their stored `endtime` in `data.json`.

---

## ❗ Important Notes

* Your bot must have **Administrator** permissions.
* Roles and categories **must exist** with the correct IDs configured in `config.json`.
* Slot expiration is **time-based** (days or months).
* Messages and logs are **not persistent** across restarts except for JSON data.
* Pings are limited and tracked per user.

---

## 📜 License  

MIT License – Free to use and modify.  

---

## 🔗 Community

Join the community Discord server here:  
👉 [https://discord.gg/qNemf7Uqum](https://discord.gg/qNemf7Uqum)

---

## 👨‍💻 Developer

Made with ❤️ by **zle0o**

---

Like this Slot Bot? Leave a ⭐ on GitHub!
