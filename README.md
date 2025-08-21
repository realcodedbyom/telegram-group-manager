# 🌼 DaisyBot - Telegram Group Management Bot

A comprehensive and user-friendly Telegram bot designed to help manage your chat groups with ease. DaisyBot provides a beautiful interface with inline keyboards and powerful moderation tools to keep your community blooming! 🌻

## ✨ Features

### 🛡️ Moderation Tools
- **User Management**: Ban, unban, kick, mute, and unmute users
- **Warning System**: Warn users with automatic actions after 3 warnings
- **Advanced Actions**: Delete messages with simultaneous warning/muting
- **Permission Control**: Lock/unlock all chat permissions
- **Admin Tools**: Promote and demote users with custom titles

### 🎯 Smart Features
- **Message Filtering**: Create custom filters that respond to keywords
- **Anti-Spam Protection**: Configurable spam detection and prevention
- **Anti-Flood System**: Prevent message flooding with customizable limits
- **Global Ban**: Owner-only global ban across all bot-managed chats
- **Message Purging**: Bulk delete messages efficiently

### 🎮 Fun Commands
- 🎲 **Dice Rolling**: Roll a 6-sided dice
- 🪙 **Coin Flipping**: Heads or tails decision maker
- 🔢 **Random Numbers**: Generate numbers between 1-100
- 💬 **Inspirational Quotes**: Get motivational quotes

### ⚙️ Customization
- **Welcome/Goodbye Messages**: Set custom greetings
- **Chat Rules**: Define and display community guidelines
- **Flexible Settings**: Configure anti-spam and anti-flood parameters

### 📱 User-Friendly Interface
- **Inline Keyboard Menus**: Easy navigation through bot features
- **Comprehensive Help System**: Built-in command documentation
- **User/Chat Information**: Quick access to IDs and statistics
- **Organized Commands**: Categorized by admin, user, and fun functions

## 🚀 Quick Start

### Prerequisites
- Python 3.6 or higher
- A Telegram Bot Token from [@BotFather](https://t.me/botfather)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/realcodedbyom/telegram-group-manager.git
   cd telegram-group-manager
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure the bot**
   ```python
   # Replace in the code or use environment variables (recommended)
   TOKEN = 'YOUR_BOT_TOKEN_HERE'
   OWNER_ID = YOUR_TELEGRAM_USER_ID
   OWNER_USERNAME = "@realcodedbyom"
   ```

4. **Run the bot**
   ```bash
   python bot.py
   ```

### 🔒 Security Setup (Recommended)

For production deployment, use environment variables:

1. Create a `.env` file:
   ```env
   BOT_TOKEN=your_bot_token_here
   OWNER_ID=your_user_id
   OWNER_USERNAME=@yourusername
   ```

2. Modify the bot code to use environment variables:
   ```python
   import os
   from dotenv import load_dotenv
   
   load_dotenv()
   TOKEN = os.getenv('BOT_TOKEN')
   OWNER_ID = int(os.getenv('OWNER_ID'))
   OWNER_USERNAME = os.getenv('OWNER_USERNAME')
   ```

3. Add `python-dotenv==1.0.0` to requirements.txt

## 📋 Commands Reference

### Admin Commands
| Command | Description | Usage |
|---------|-------------|--------|
| `/ban` | Ban a user | Reply to user's message |
| `/unban` | Unban a user | `/unban <user_id>` |
| `/kick` | Kick a user | Reply to user's message |
| `/mute` | Mute a user | Reply to user's message |
| `/unmute` | Unmute a user | Reply to user's message |
| `/warn` | Warn a user | Reply to user's message |
| `/unwarn` | Remove a warning | Reply to user's message |
| `/promote` | Promote to admin | `/promote [custom_title]` |
| `/demote` | Demote admin | Reply to user's message |
| `/purge` | Delete messages | `/purge <number>` |
| `/lockall` | Lock all permissions | `/lockall` |
| `/unlockall` | Unlock all permissions | `/unlockall` |
| `/dwarn` | Delete message & warn | Reply to message |
| `/dmute` | Delete message & mute | Reply to message |

### Filter Commands
| Command | Description | Usage |
|---------|-------------|--------|
| `/filter` | Create a filter | Reply to message + `/filter <keyword>` |
| `/stop` | Remove a filter | `/stop <keyword>` |
| `/filterlist` | List all filters | `/filterlist` |

### Settings Commands
| Command | Description | Usage |
|---------|-------------|--------|
| `/set_welcome` | Set welcome message | `/set_welcome <message>` |
| `/set_goodbye` | Set goodbye message | `/set_goodbye <message>` |
| `/set_rules` | Set chat rules | `/set_rules <rules>` |
| `/set_antispam` | Configure anti-spam | `/set_antispam <msg_limit> <time_frame>` |
| `/set_antiflood` | Configure anti-flood | `/set_antiflood <msg_limit> <time_frame>` |

### User Commands
| Command | Description |
|---------|-------------|
| `/start` | Start the bot and show main menu |
| `/help` | Show help information |
| `/info` | Show user and chat information |
| `/id` | Show user and chat IDs |
| `/rules` | Display chat rules |

### Fun Commands
| Command | Description |
|---------|-------------|
| `/roll_dice` | Roll a dice (1-6) |
| `/flip_coin` | Flip a coin (Heads/Tails) |
| `/random_number` | Generate random number (1-100) |
| `/quote` | Get an inspirational quote |

### Owner-Only Commands
| Command | Description | Usage |
|---------|-------------|--------|
| `/gban` | Global ban user | Reply to user's message |
| `/announcement` | Send announcement to all chats | `/announcement <message>` |

## 🛠️ Technical Details

### Built With
- **Python 3.x**: Core programming language
- **python-telegram-bot**: Telegram Bot API wrapper
- **Inline Keyboards**: Modern user interface
- **In-memory Storage**: User data and settings (consider database for production)

### Architecture
- **Modular Design**: Separate functions for each feature
- **Error Handling**: Comprehensive error catching and user feedback
- **Permission System**: Role-based access control
- **Anti-Spam/Flood**: Time-based message tracking

## 📚 Setup for Different Environments

### Local Development
```bash
python bot.py
```

### Docker Deployment
```dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["python", "bot.py"]
```

### Heroku Deployment
1. Create `Procfile`:
   ```
   worker: python bot.py
   ```
2. Set config vars for TOKEN, OWNER_ID, OWNER_USERNAME

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

- This bot requires admin permissions in your Telegram group to function properly
- Always test commands in a test group before deploying to production
- Be cautious with global ban feature - it affects all groups where the bot is present
- Keep your bot token secure and never commit it to public repositories

## 🆘 Support

If you encounter any issues or have questions:

1. Check the [Issues](../../issues) section
2. Create a new issue with detailed description
3. Contact the bot owner for urgent matters

## 🔄 Updates

Stay updated with the latest features and bug fixes by watching this repository or checking the [Releases](../../releases) section.

---

Made with 💖 by [Your Username] | Let's make Telegram communities bloom! 🌻
