# BANKSapi plugins

Plugin marketplace for Codex and the ChatGPT desktop app. It lists the BANKSapi plugin, which
gives your assistant live access to the BANKSapi developer documentation and OpenAPI
specifications and teaches it the integration flow.

This repository contains only the marketplace catalog. The plugin itself lives in
[BANKSapi/claude-plugin](https://github.com/BANKSapi/claude-plugin) and is installed from its
`main` branch.

## Install in Codex

```bash
codex plugin marketplace add BANKSapi/plugins
```

Then start Codex, enter `/plugins`, open the **BANKSapi** marketplace tab and install
**BANKSapi**. Start a new session before you use it.

In the ChatGPT desktop app, configured marketplaces appear as a source in the Plugins
Directory.

## What the plugin does

- Searches the BANKSapi documentation, reads docs pages and fetches single operations from the
  OpenAPI specifications through the BANKSapi docs connector at `https://banksapi.io/docs-mcp`
- `integrate`: walks through the BANKS/Connect flow from tokens and users to bank accesses and
  transactions, including the REG/Protect redirect and consent renewal
- `diagnose`: explains failing API calls and bank accesses that stopped updating

The plugin reads public documentation only. It doesn't access bank accounts, doesn't initiate
payments and never asks for credentials. See the plugin's
[README](https://github.com/BANKSapi/claude-plugin#data) for which services receive which data.

## Update

Codex installs the plugin from `BANKSapi/claude-plugin` at `main`. To pull the latest catalog:

```bash
codex plugin marketplace upgrade banksapi
```

## License

[MIT](LICENSE)
