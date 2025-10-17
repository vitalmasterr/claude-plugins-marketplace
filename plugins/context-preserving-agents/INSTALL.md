# Installation Guide

Quick installation instructions for the Context Preserving Agents plugin.

## Quick Install

### Method 1: Copy to Claude Plugins Directory

```bash
# Copy the entire plugin folder to your Claude Code plugins directory
cp -r context-preserving-agents ~/.claude/plugins/
```

### Method 2: Symlink (For Development)

```bash
# Create a symlink if you want to keep the plugin in a different location
ln -s /path/to/context-preserving-agents ~/.claude/plugins/context-preserving-agents
```

### Method 3: Git Clone

```bash
cd ~/.claude/plugins/
git clone https://github.com/yourusername/context-preserving-agents.git
```

## Verify Installation

1. Restart Claude Code (if running)
2. Check installed plugins:
   ```
   /plugins list
   ```
3. You should see "Context Preserving Agents" in the list

## Configure Your Project

1. Copy the CLAUDE.md template to your project:
   ```bash
   cp ~/.claude/plugins/context-preserving-agents/CLAUDE.md.template your-project/CLAUDE.md
   ```

2. (Optional) Customize the decision tree in CLAUDE.md to match your workflow

## Test the Installation

Try these commands in Claude Code:

```
"Investigate the project architecture"
→ Should trigger researcher-agent

"Should we use approach A or B? Consider pros and cons"
→ Should trigger thinker-agent

"Update the README with installation instructions"
→ Should trigger bookworm-agent
```

## Troubleshooting

### Plugin not showing in list
- Check that the plugin folder is in `~/.claude/plugins/`
- Verify the `.claude-plugin/plugin.json` file exists
- Restart Claude Code

### Agents not activating
- Ensure CLAUDE.md is in your project root
- Check the decision tree patterns match your requests
- Try explicit invocation: "Use the researcher-agent to..."

### Permission errors
- Check file permissions: `chmod -R 755 ~/.claude/plugins/context-preserving-agents`
- Verify you have write access to the plugins directory

## Next Steps

1. Read the [README.md](README.md) for detailed usage examples
2. Review the [CHANGELOG.md](CHANGELOG.md) for version information
3. Check agent files in `agents/` directory for customization options
4. Join discussions at https://github.com/yourusername/context-preserving-agents/discussions

## Uninstallation

```bash
rm -rf ~/.claude/plugins/context-preserving-agents
```

Then restart Claude Code.

## Support

- Issues: https://github.com/yourusername/context-preserving-agents/issues
- Documentation: [README.md](README.md)
- Template: [CLAUDE.md.template](CLAUDE.md.template)
