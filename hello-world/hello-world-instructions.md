# Hello World Command - Setup Instructions

## Overview

This is a simple example command that demonstrates how Firebender commands work. When executed, it
provides a friendly greeting and explains what Firebender can do in your current project context.

Perfect for:

- Testing that your Firebender setup is working
- Understanding how commands function
- Getting oriented when you start working in a new codebase

## Prerequisites

- Firebender plugin installed and configured
- Access to a Firebender account with API credits

## Setup

1. **Copy the command file**:
   ```bash
   # Copy hello-world.md to your project's prompts/commands directory
   mkdir -p ./prompts
   cp hello-world.md ./prompts/
   ```

2. **Update your project's firebender.json**:

   If you don't have a `firebender.json` file in your project root, create one:
   ```json
   {
     "commands": [
       {
         "name": "hello world",
         "path": "./prompts/hello-world.md",
         "model": "default",
         "mode": "auto"
       }
     ]
   }
   ```

   If you already have a `firebender.json` file, add the command to your existing `commands` array:
   ```json
   {
     "commands": [
       // ... your existing commands
       {
         "name": "hello world",
         "path": "./prompts/hello-world.md",
         "model": "default",
         "mode": "auto"
       }
     ]
   }
   ```

3. **Test the command**:
    - Open Firebender chat in your IDE
    - Type `/hello` and select "hello world" from the dropdown
    - The command should execute and provide a friendly greeting with project context

## Usage

### When to Use

- First time setting up Firebender in a project
- Testing that your command configuration is working
- Getting a quick overview of what Firebender can see in your project
- Demonstrating Firebender to team members

### How to Execute

1. Open the Firebender chat interface
2. Type `/hello` (or `/hello world`)
3. Select the "hello world" command from the dropdown
4. Press Enter to execute

### Expected Output

The command will provide:

- A friendly greeting
- Information about your current project context
- Suggestions for what Firebender can help with
- Next steps specific to your codebase

## Configuration Options

You can customize this command by modifying the following in your `firebender.json`:

- **name**: Change `"hello world"` to whatever you want to call it
- **model**:
    - `"default"` - Uses your current model selection
    - `"quick"` - Uses the fastest available model
    - `"claude-4 sonnet"` - Uses a specific model
- **mode**:
    - `"auto"` - Let Firebender choose the best mode
    - `"read"` - Read-only analysis mode
    - `"write"` - Allow code changes and terminal commands

## Troubleshooting

### Command doesn't appear in dropdown

- Check that your `firebender.json` is in the project root
- Verify the JSON syntax is valid
- Ensure the `path` points to the correct location of `hello-world.md`
- Try restarting your IDE

### Command executes but gives an error

- Check that the `hello-world.md` file exists at the specified path
- Verify you have Firebender API credits available
- Check the Firebender plugin logs for specific error details

### Want to modify the command

- Edit the `hello-world.md` file to change what the AI does
- The changes will take effect immediately on the next command execution
- No need to restart your IDE for content changes

## Next Steps

Once you have this working, try:

1. Creating your own custom commands for your specific workflows
2. Exploring other community commands in this repository
3. Reading the [Firebender Commands documentation](https://docs.firebender.dev/context/commands) for
   advanced features