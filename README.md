# Comm Bot

<div align="center">

![Comm Bot Logo](logo.png)

**A powerful Discord bot for creating custom slash commands**

[![Discord.py](https://img.shields.io/badge/discord.py-2.0+-blue.svg)](https://github.com/Rapptz/discord.py)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

[Features](#features) • [Installation](#installation) • [Usage](#usage) • [Commands](#commands) • [License](#license)

</div>

---

## Overview

Comm Bot enables Discord server administrators to create custom slash commands with ease. Whether you need automated replies, role management, or embedded messages, Comm Bot provides an intuitive interface for building custom interactions without writing code.

## Features

✨ **Custom Reply Commands**
- Create commands that send custom messages
- Configure rich embeds with titles, descriptions, images, and more
- Add advanced styling options

🎭 **Role Management**
- Create commands to add roles to users
- Create commands to remove roles from users
- Support for multiple role selection

🎨 **Rich Embeds**
- Customizable titles and descriptions
- Add images and thumbnails
- Configure colors, authors, and footers
- Advanced styling options

🔒 **Permission System**
- Administrator-only command creation
- Secure role management

💾 **Persistent Storage**
- Commands saved locally in JSON format
- Automatic synchronization across server restarts

## Installation

### Prerequisites

- Python 3.8 or higher
- A Discord Bot Token ([Create one here](https://discord.com/developers/applications))

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/comm-bot.git
   cd comm-bot
   ```

2. **Install dependencies**
   ```bash
   pip install discord.py
   ```

3. **Configure your bot token**
   
   Open `commands.py` and replace the token at the bottom:
   ```python
   TOKEN = "YOUR_BOT_TOKEN_HERE"
   ```

4. **Run the bot**
   ```bash
   python commands.py
   ```

5. **Invite the bot to your server**
   
   Use this URL format (replace `YOUR_CLIENT_ID`):
   ```
   https://discord.com/api/oauth2/authorize?client_id=YOUR_CLIENT_ID&permissions=268435456&scope=bot%20applications.commands
   ```

## Usage

### Creating Commands

Use the `/createcommand` slash command to start creating custom commands. You'll need Administrator permissions.

![Create Command Demo](demo-create.gif)

### Command Types

**1. Reply Commands**
- Send text messages or rich embeds
- Perfect for announcements, FAQs, or automated responses

**2. Add Role Commands**
- Automatically assign roles to users
- Great for self-role systems

**3. Remove Role Commands**
- Remove roles from users
- Useful for role management workflows

## Commands

### `/createcommand`

Create a new custom command for your server.

**Parameters:**
- `action` - Type of command (reply / add-role / delete-role)
- `embed` - Configure embed for reply commands (yes / no)

**Example:**
```
/createcommand action:reply embed:yes
```

![Command Creation Flow](demo-flow.png)

### `/deletecommand`

Delete an existing custom command.

**Parameters:**
- `command_name` - Name of the command to delete

**Example:**
```
/deletecommand command_name:welcome
```

## Configuration

### Embed Configuration

When creating a reply command with embeds, you can configure:

**Basic Settings:**
- Title
- Description
- Footer text
- Image URL
- Thumbnail URL

**Advanced Settings:**
- Author name and icon
- Embed color (hex format)

![Embed Configuration](demo-embed.png)

## File Structure

```
comm-bot/
├── commands.py           # Main bot file
├── custom_commands.json  # Command storage (auto-generated)
├── README.md            # This file
└── LICENSE              # License file
```

## Examples

### Example 1: Welcome Message

Create a command that sends a welcome message with an embed:

```
/createcommand action:reply embed:yes
```

Then configure:
- Command name: `welcome`
- Message: `Welcome to our server!`
- Embed title: `Welcome!`
- Embed description: `We're glad you're here`

### Example 2: Member Role

Create a command that gives users a "Member" role:

```
/createcommand action:add-role
```

Then select the role and provide a command name.

![Examples](demo-examples.png)

## Troubleshooting

**Commands not appearing?**
- Ensure the bot has the `applications.commands` scope
- Wait a few minutes for Discord to sync commands
- Try kicking and re-inviting the bot

**Permission errors?**
- Verify the bot role is above the roles it needs to manage
- Check that the bot has `Manage Roles` permission

**Bot not responding?**
- Check the console for error messages
- Verify your bot token is correct
- Ensure the bot is online

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Support

Need help? Here are some resources:

- [Discord.py Documentation](https://discordpy.readthedocs.io/)
- [Discord Developer Portal](https://discord.com/developers/docs)
- [Open an Issue](https://github.com/yourusername/comm-bot/issues)

## Roadmap

- [ ] Command categories and organization
- [ ] Command usage statistics
- [ ] Scheduled commands
- [ ] Button and dropdown support
- [ ] Command permissions per role
- [ ] Export/import command configurations

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [discord.py](https://github.com/Rapptz/discord.py)
- Inspired by the Discord community's need for customization

---

<div align="center">

Made with ❤️ for the Discord community

[⬆ Back to Top](#comm-bot)

</div>
