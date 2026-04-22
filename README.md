# My Opencode Configuration

Welcome to my personal opencode configuration setup. Because apparently, I'm
so incredibly skilled at configuring things that I've decided to share my
"expertise" with the world. Truly, what a gift to humanity.

This repository contains my custom configuration for opencode, designed to
make your coding experience as... well, as mediocre as possible while still
pretending to be professional.

## Installation

### Prerequisites

Before you begin, you'll need to install opencode and ollama. Please refer to
the official documentation for these installations:

- [Opencode Installation Guide](https://github.com/anomalyco/opencode)
- [Ollama Installation Guide](https://github.com/ollama/ollama)

### Cloning the Configuration

To install this configuration, simply clone the repository into your
`~/.config/opencode` directory:

```bash
git clone https://github.com/Bastes/opencode-config ~/.config/opencode
```

### Installing the Qwen3 Coder Model

Once you have ollama installed, you can pull the `qwen3-coder:30b` model:

```bash
ollama pull qwen3-coder:30b
ollama pull qwen3.5:35b-a3b
ollama pull qwen3.6:35b-a3b
ollama pull sam860/lucy:1.7b
```

To ensure the model properly understands how to use available tools, please run the following commands:

```bash
ollama run qwen3-coder:30b
> /set parameter num_ctx 16384
Set parameter 'num_ctx' to `16384`
> /save qwen3-coder:30b
Created new model `qwen3-coder:30b'
> /bye

ollama run qwen3.5:35b-a3b
> /set parameter num_ctx 16384
Set parameter 'num_ctx' to `16384`
> /save qwen3.5:35b-a3b-16384
Created new model `qwen3-coder:30b-16384'
> /bye

ollama run qwen3.6:35b-a3b
> /set parameter num_ctx 16384
Set parameter 'num_ctx' to `16384`
> /save qwen3.6:35b-a3b-16384
Created new model `qwen3-coder:30b-16384'
> /bye
```

This increases the context window size to accommodate the tool usage instructions and other contextual information that opencode needs to properly function.

That's it. You're now officially configured to use my amazing setup. Enjoy
the... "optimization" of your workflow.
