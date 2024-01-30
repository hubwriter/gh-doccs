# gh-doccs

A GitHub CLI extension to create a new codespace for docs work.

This extension creates a codespaces from the docs-internal repository (assuming you have access to it), and then opens the codespace so that you can start using it.

"doccs" = docs codespace

**Note**: This extension is a simplified, GitHub-Docs-Team-specific, version of the https://github.com/hubwriter/gh-quickcs extension.

## 📦 Installation

1. If you haven't already, install the `gh` CLI - see the [installation](https://github.com/cli/cli#installation)

   _Installation requires a minimum version (2.0.0) of the GitHub CLI, which supports extensions._

1. Use the GitHub CLI to install the extension:

   ```
   gh ext install hubwriter/gh-doccs
   
   Cloning into '/Users/yourname/.local/share/gh/extensions/gh-doccs'...
   remote: Enumerating objects: 35, done.
   remote: Counting objects: 100% (35/35), done.
   remote: Compressing objects: 100% (30/30), done.
   remote: Total 35 (delta 6), reused 24 (delta 3), pack-reused 0
   Receiving objects: 100% (35/35), 9.65 KiB | 4.83 MiB/s, done.
   Resolving deltas: 100% (6/6), done.
   ✓ Installed extension hubwriter/gh-doccs
   ```
   
## ⚡️ Usage

1. Run

   ```sh
   gh doccs
   ```
   
1. Enter a display name for the codespace. Don't use quote marks around the name. The name can include spaces and hyphens.
1. Enter the name of a new branch you want to create, or press Enter to use the default branch. (Note this option can be turned off by setting `REQUEST_BRANCH` to `false` in the `gh-doccs` script.)

For example:<br>
<img width="1057" alt="image" src="https://user-images.githubusercontent.com/54933897/216063640-2d773aae-595e-45c2-9f07-05ce256dc50c.png">

<img width="580" alt="image" src="https://user-images.githubusercontent.com/54933897/216062894-b88986a4-39e8-49ea-969c-93704c81c8d6.png">

## 🔧 Configuration

Typically the script doesn't need any configuration, but you can change some of the settings if required. 
You can do this by editing your local copy of the `gh-doccs` file and editing the values of the variables at the top of the script.

```bash
REPO="github/docs-internal"
DEVCONTAINER=".devcontainer/devcontainer.json"
TIMEOUT="3h"
MACHINE="xLargePremiumLinux" # To list available machine types for a repo use:
                             # gh api --jq ".machines[].name" repos/OWNER/REPONAME/codespaces/machines
LOCATION="" # e.g. EastUs|SouthEastAsia|WestEurope|WestUs2
            # Leave empty for automatic location selection.
            # To list current available locations see: gh cs create --help
RETENTION="720h"
OPEN_IN_BROWSER=false # Set to true to open the codespace in a browser, or false to open in VS Code.
REQUEST_BRANCH=true # Set to true to request a branch name, or false to use the default branch.
```

For example, by default `LOCATION` is an empty string, but you can set this to a particular location 
(e.g. `EastUs` or `SouthEastAsia` or `WestEurope` or `WestUs2`).

After changing any of the variable values, uninstall the existing version of the extension:

```
gh ext remove doccs
```

Then, on the command line, move to the location of `doccs` file and install the extension locally:

```
gh ext install . 
```
