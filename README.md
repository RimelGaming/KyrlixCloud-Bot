☁️ KyrlixCloud Bot

An All-in-One Discord Shop & Community Management Bot

KyrlixCloud Bot is a feature-rich Discord bot built with Python and "discord.py". It combines hosting shop information, moderation, customer reviews, leveling, support tickets, giveaways, and interactive embeds in one modular application.

Developed with ❤️ by Rimel Hossain for the KyrlixCloud community.

✨ Features

- 🛒 Hosting Shop — Hosting plans, pricing, payment methods, and useful links.
- 🛡️ Moderation — Ban, temporary ban, unban, timeout, and role management.
- 🎨 Embed Builder — Create custom embeds with quick commands or an interactive builder.
- ⭐ Review System — Star ratings, discussion threads, useful votes, and reports.
- 📈 Leveling System — Chat XP, member ranks, and leaderboards.
- 🎫 Support Tickets — Private support channels with configurable staff access.
- 🎉 Giveaways — Timed giveaways with interactive entry buttons and automatic winner selection.
- 📚 Help Command — Automatically lists commands from loaded cogs.
- 💾 Database Support — MySQL-backed storage for supported features.
- 🧩 Modular Structure — Organized cogs for easier maintenance and expansion.

🛠️ Tech Stack

- Python 3.10+
- discord.py
- MySQL / MariaDB
- aiomysql
- Environment-based configuration

📂 Project Structure

KyrlixCloud-Bot/
├── bot.py
├── config.py
├── requirements.txt
├── .env.example
├── cogs/
│   ├── shop.py
│   ├── moderation.py
│   ├── embeds.py
│   ├── reviews.py
│   ├── leveling.py
│   ├── tickets.py
│   ├── giveaways.py
│   └── help.py
└── utils/
    ├── time_parser.py
    └── db.py

🤖 Commands

Command| Description
"/plans"| Browse hosting plans and pricing tiers.
"/pay"| View payment methods and regions.
"/bkash"| Display bKash payment information.
"/nagod"| Display Nagad payment information.
"/links"| Show configured links.
"/web"| Get the website link.
"/panel"| Display client panel information.
"/ban"| Permanently ban a member.
"/tempban"| Temporarily ban a member.
"/unban"| Unban a user by ID.
"/mute"| Apply a Discord timeout.
"/role"| Add or remove a member's role.
"/embed"| Create custom embeds.
"/review"| Submit a star-rated review.
"/rank"| View a member's rank and XP.
"/leaderboard"| View the top 10 members by XP.
"/ticket"| Open a private support ticket.
"/giveaway"| Start a timed giveaway.
"/help"| Display available commands.

Some interactive commands, including the review flow and embed modal, require slash commands. Prefix commands use "!" where implemented.

🚀 Installation Guide

1. Install Python 3, pip, and Git

Update your package list and install the required packages on Ubuntu/Debian:

sudo apt update
sudo apt install -y python3 python3-pip python3-venv git

Verify the installation:

python3 --version
pip3 --version
git --version

2. Clone the Repository

git clone https://github.com/RimelGaming/KyrlixCloud-Bot.git
cd KyrlixCloud-Bot

3. Configure Environment Variables

Create your ".env" file:

mv .env.example .env
nano .env

Enter your Discord bot token and MySQL database credentials using the variable names specified in ".env.example".

Save and exit Nano:

1. Press "Ctrl + O" to save.
2. Press "Enter" to confirm.
3. Press "Ctrl + X" to exit.

4. Install Python Dependencies

Create and activate a virtual environment:

python3 -m venv .venv
source .venv/bin/activate

Install the dependencies:

pip install -r requirements.txt

5. Configure MySQL

Make sure your MySQL or MariaDB server is running and reachable.

Create the database if it does not already exist:

CREATE DATABASE kyrlixcloud_bot
    CHARACTER SET utf8mb4
    COLLATE utf8mb4_unicode_ci;

Configure the database connection in ".env" according to the variable names used by the application.

Ensure the bot's database initialization code creates all tables required by the enabled features.

6. Configure Your Discord Bot

1. Visit the "Discord Developer Portal" (https://discord.com/developers/applications).
2. Create an application and add a bot.
3. Copy the bot token into ".env".
4. Enable Message Content Intent for prefix commands and message-based XP.
5. Enable Server Members Intent if required by your implementation.
6. Generate an invitation URL using the "bot" and "applications.commands" OAuth2 scopes.
7. Grant the bot the permissions required by its enabled features.

Ensure the bot's role is above any roles it needs to manage.

7. Start the Bot

python3 bot.py

Keep the terminal session running while you want the bot online. Closing the session may stop the bot.

⚙️ Customization

Most shop content and feature settings are available in "config.py".

Setting| Purpose
"TIER_SPECS"| Hosting plan specifications.
"REGIONS"| Hosting regions and pricing.
"PAYMENT_NUMBERS"| Payment details.
"LINKS"| Website and community links.
"WEB_PANEL"| Client panel information.
"REVIEWS_CHANNEL_ID"| Review destination channel.
"REVIEW_REPORT_LOG_CHANNEL_ID"| Optional review-report log channel.
"TICKETS_CATEGORY_ID"| Support ticket category.
"TICKET_STAFF_ROLE_ID"| Optional support staff role.
"XP_MIN" / "XP_MAX"| XP awarded per eligible message.
"XP_COOLDOWN_SECONDS"| XP cooldown duration.
"LEVEL_UP_ANNOUNCE"| Enable or disable level-up announcements.

Use the exact setting names present in your current "config.py".

🔐 Security

- Never publish your Discord bot token or database password.
- Keep ".env" out of Git using ".gitignore".
- Use a dedicated MySQL user instead of the root account for production.
- Grant only the Discord permissions the bot needs.
- Back up important database data regularly.

If a secret is accidentally published, rotate it immediately.

🩺 Troubleshooting

Bot cannot connect to MySQL

- Check whether MySQL is running.
- Verify the host, port, username, password, and database name.
- Check firewall rules and remote database permissions.

Slash commands do not appear

- Confirm that the bot was invited with "applications.commands".
- Check the command synchronization logs.
- Allow time for global command updates.

Prefix commands do not work

- Enable Message Content Intent in the Developer Portal and in the bot's code.
- Check that you are using the configured prefix.

Role or moderation commands fail

- Verify the bot's permissions.
- Ensure its highest role is above the roles it needs to manage.

🗺️ Roadmap

- [ ] Improve installation documentation.
- [ ] Expand automated testing.
- [ ] Improve logging and monitoring.
- [ ] Add database migration support.

🤝 Contributing

Contributions, bug reports, and suggestions are welcome.

1. Fork the repository.
2. Create a branch for your changes.
3. Test your changes.
4. Submit a pull request with a clear description.

📄 License

Check the repository for its "LICENSE" file to determine the applicable terms of use and redistribution. If no license is present, permission to reuse the code is not automatically granted.

👨‍💻 Author

Rimel Hossain
Founder & CEO of KyrlixCloud

- GitHub: "@RimelGaming" (https://github.com/RimelGaming)
- Repository: "KyrlixCloud-Bot" (https://github.com/RimelGaming/KyrlixCloud-Bot)
- Website: "kyrlixcloud.top" (https://kyrlixcloud.top)

---

<p align="center">
  <strong>KyrlixCloud Bot</strong><br>
  Made with ❤️ by Rimel Hossain
</p>
