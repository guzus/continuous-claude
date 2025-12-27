# Deep Claude

## Debugging New Features

To test new features on a remote machine:

1. **Build and deploy to remote:**
   ```bash
   make scp-linux
   ```
   This builds the Linux binary and copies it to the remote machine, setting up the `dclaude` alias.

2. **Test on remote:**
   ```bash
   ssh deep-claude-vm "source ~/.bashrc && cd ~/test-folder && dclaude -p 'test' --max-runs 1 --dry-run"
   ```

   Or connect interactively:
   ```bash
   ssh deep-claude-vm
   dclaude -p "test task" --max-runs 1 --dry-run
   ```

Use `--dry-run` to simulate without making actual changes. The `--max-runs 1` flag limits execution to a single iteration for quick testing.

## Background Mode

Run in detached tmux session:
```bash
dclaude -d -p "task description" --max-runs 5
```

Manage sessions:
```bash
dclaude sessions   # Interactive session picker
dclaude logs dc-*  # View logs
dclaude attach dc-*  # Attach to session
dclaude kill dc-*  # Kill session
```
