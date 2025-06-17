# Personal Scripts Collection

A guide for setting up and managing personal shell scripts on macOS.

## Initial Setup

### 1. Create bin Directory

Create a personal bin directory in your home folder:

```bash
mkdir -p ~/bin
```

### 2. Add bin to PATH in zsh Configuration

Edit your `.zshrc` file to include the bin directory in your PATH:

```bash
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
```

### 3. Reload zsh Configuration

Apply the changes to your current terminal session:

```bash
source ~/.zshrc
```

## Creating and Using Scripts

### 4. Create a Script

Create a new script file in your bin directory:

```bash
touch ~/bin/my-script
```

You can use any text editor to edit the script. For example:

```bash
nano ~/bin/my-script
```

Or with VS Code:

```bash
code ~/bin/my-script
```

Basic script template:

```bash
#!/bin/bash

# Description: What this script does
# Usage: How to use this script

echo "Hello, this is my script!"
```

### 5. Make the Script Executable

This step is essential for your script to be runnable:

```bash
chmod +x ~/bin/my-script
```

### 6. Run Your Script

From any directory in your terminal:

```bash
my-script
```


## Common Issues

If your script doesn't run:
- Check if it's executable (`ls -la ~/bin/my-script`)
- Verify ~/bin is in your PATH (`echo $PATH`)
- Ensure your script starts with a proper shebang line (`#!/bin/bash`)
- Check for syntax errors in your script
