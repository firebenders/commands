# Firebender Commands

A community collection of custom AI commands for [Firebender](https://firebender.com).

👉 **Learn about commands:** [Firebender Commands Documentation](https://docs.firebender.com/context/commands)
## Repository Purpose

This repository exists so people can share their useful Firebender commands with the community. Each
command is stored in its own folder for easy browsing and copying.

## Repository Structure

Commands in this repository are organized as:

```
command-name/
├── command-name.md              # The actual command prompt/instructions
├── firebender.json             # Configuration for this specific command
├── command-name-instructions.md # Setup instructions and usage guide
├── demo.gif                     # Optional: Demo of the command in action
├── setup-screenshot.png         # Optional: Screenshots for setup steps
└── examples/                    # Optional: Additional example files
```

**Additional files are encouraged!** Include images, GIFs, example outputs, or any other files that
help users understand and use your command effectively.

## Contributing a Command

### 1. Create Your Command Folder

Create a folder named `your-command-name` with these three **required** files:

**`your-command-name.md`** - The command content:

```markdown
# Your Command Title

Write clear, specific instructions for what the AI should do.
```

**`firebender.json`** - Configuration for this repository:

```json
{
  "commands": [
    {
      "name": "your command name",
      "path": "./your-command-name.md",
      "model": "default",
      "mode": "auto"
    }
  ]
}
```

**`your-command-name-instructions.md`** - Setup guide:

```markdown
# Your Command Name - Setup Instructions

## Overview
What this command does.

## Setup
1. Step-by-step instructions
2. How to configure
3. How to test

## Usage
When and how to use this command.
```

### 2. Add Supporting Files (Encouraged)

- `demo.gif` or `demo.mp4` - Show the command in action
- Screenshots for setup steps or expected outputs
- Example files or folders that demonstrate usage
- Any other documentation that helps users

### 3. Submit Your Command

1. Fork this repository
2. Add your command folder with all files
3. Submit a pull request

---

**Join the Community:**

- 💬 [Discord Community](https://discord.com/invite/4WF9D5Bzvd)