# 🔂 Continuous Claude

Automated wrapper for Claude Code that runs tasks repeatedly with automatic git commits and error handling.

## 🚀 Quick start

```bash
# Download the script
curl -o continuous_claude.sh https://raw.githubusercontent.com/AnandChowdhary/continuous-claude/refs/heads/main/continuous_claude.sh

# Make it executable
chmod +x continuous_claude.sh

# Run it with your prompt and infinite max runs
./continuous_claude.sh --prompt "add unit tests until all code is covered" --max-runs 0
```

## 🎯 Flags

- `-p, --prompt`: Task prompt for Claude Code (required)
- `-m, --max-runs`: Number of iterations, use `0` for infinite (required)

## 📝 Examples

```bash
# Run 5 iterations
./continuous_claude.sh -p "improve code quality" -m 5

# Run infinitely until stopped
./continuous_claude.sh -p "add unit tests until all code is covered" -m 0
```

## 📃 License

MIT (c) [Anand Chowdhary](https://anandchowdhary.com)
