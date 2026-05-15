This is a very simple harness based on built-in support of subagents in Codex cli.

# Installation

If you don't have any existing subagents you can simply link the whole agents directory from here:

```
$ git clone [repo]
$ ln -s $PWD/codex-harness/agents ~/.codex/agents 
```

Otherwise, you can link the individual toml and prompt md files into your `~/.codex/agents` directory.

# Usage

There are two ways to use it from your project repo after you have installed the agents.

1. Launch your vanilla codex and tell it to use coordinator to do the work.

```
$ codex "Use coordinator subagent to implement a new REST api get_changed_nodes..."
```

2. Directly launch into the coordinator:

```
$ codex -c "model_instructions_file=~/.codex/agents/prompts/coordinator.md" \
    "Implement a new REST api get_changed_nodes..."
```
