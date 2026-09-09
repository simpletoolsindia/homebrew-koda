# homebrew-koda

Homebrew tap for [koda](https://github.com/simpletoolsindia/koda) — a terminal
coding agent that drives the model you already run locally, and never leaves
your machine.

```sh
brew tap simpletoolsindia/koda
brew install koda
```

After the tap, the short name is all you need:

```sh
brew upgrade koda
brew uninstall koda
brew untap simpletoolsindia/koda
```

The formula installs the prebuilt binary for your platform from koda's GitHub
releases — macOS and Linux, Intel and ARM — so installing is a download rather
than a Rust build. It also pulls in
[ripgrep](https://github.com/BurntSushi/ripgrep), which koda's `search` tool
uses when it is present.

koda talks to a model server you run yourself (Ollama, LM Studio, llama.cpp,
vLLM, MLX, or anything else speaking the OpenAI chat API). Run `koda` and use
`/setup` to point it at one.

- [Documentation](https://simpletoolsindia.github.io/koda/)
- [Installation guide](https://simpletoolsindia.github.io/koda/install/)

## Updating this tap

The formula is generated from a release, so it is not edited by hand:

```sh
# in the koda repo
packaging/update.py v0.2.0
cp packaging/homebrew/koda.rb ../homebrew-koda/Formula/koda.rb
```
