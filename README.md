# gh-doccs

A GitHub CLI extension to create a new codespace for docs work.

This extension creates a codespaces from the docs-internal repository (assuming you have access to it), and then opens the codespace so that you can start using it.

"doccs" = docs codespace

**Note**: This extension is a simplified, GitHub-Docs-Team-specific, version of the https://github.com/hubwriter/gh-quickcs extension.

## 📦 Installation

1. If you haven't already, install the `gh` CLI - see the [installation](https://github.com/cli/cli#installation)

   _Installation requires a minimum version (2.0.0) of the the GitHub CLI that supports extensions._

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


