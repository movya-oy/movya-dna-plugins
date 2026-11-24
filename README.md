# Movya DNA plugins

Official connection settings and general usage instructions for Movya DNA.
Requires an authorized Movya DNA account; installing a plugin grants no access.

## What is public

This repository contains plugin metadata, the public MCP endpoint (https://dna.movya.net/mcp),
installation instructions, a general usage skill and the package licence. It contains no private
knowledge pages, business skills, attachments, user lists, credentials or executable scripts.
Private content is retrieved from DNA after sign-in, under the user's existing permissions.

## Apps

### Claude app

In the app's plugin interface, open Customize > Plugins > Add > Add marketplace > Add from a repository.
Enter movya-oy/movya-dna-plugins. Under Discover, open Movya DNA and choose Add to this computer.
If its Connectors tab shows DNA as disconnected, choose Connect and sign in.
Plugin availability may depend on your workspace settings. Use Claude Code's instructions for Code.

### Codex app

In the desktop plugin interface, open Plugins > Add > Add a marketplace. Enter movya-oy/movya-dna-plugins
as Source and leave Git ref and Sparse paths empty. Add Movya DNA from the plugin list.
This also applies to ChatGPT desktop in Codex mode where that plugin interface is available,
not ordinary ChatGPT web chat or the IDE extension. If already installed through the CLI, check the
plugin list before installing again. Complete sign-in if prompted, then start a new chat.

## Terminal tools

Git and a client version with plugin support are required.

### Claude Code

Installs for your user across projects:

```sh
claude plugin marketplace add movya-oy/movya-dna-plugins
claude plugin install movya-dna@movya-dna --scope user
```

Start claude, enter /mcp, select the plugin's Movya DNA server and choose Authenticate.

### Codex CLI

```sh
codex plugin marketplace add movya-oy/movya-dna-plugins
codex plugin add movya-dna@movya-dna
```

If installation did not complete sign-in:

```sh
codex mcp login movya-dna
```

## Sign in and test

Complete Google sign-in in your browser and review the DNA consent screen with your provisioned
Movya account. Existing membership and permissions remain authoritative. There is no token to copy.
Start a new chat with the plugin enabled and ask: **List the available skills in Movya DNA.**
A successful DNA tool response confirms the connection, even if the list is empty. Installation or
an assistant's unsupported claim of success does not confirm a connection.

## Existing manual connections and other clients

Before enabling the plugin, remove the old manual Movya DNA MCP entry in your client to avoid
duplicate connections. Keep other servers. Removing the plugin or entry may leave sign-in active;
use your client's sign-out or OAuth revocation controls when ending access.
Other compatible clients can use Streamable HTTP, server name movya-dna, and https://dna.movya.net/mcp
with OAuth. A manual connection does not install the plugin's local usage skill.

## Licence

MIT applies to this package only. It grants no rights to private DNA content or Movya trademarks.
