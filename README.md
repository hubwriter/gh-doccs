# gh-doccs

A GitHub CLI extension to create a new codespace for docs work.

This extension creates a codespaces from the docs-internal repository (assuming you have access to it), and then opens the codespace so that you can start using it.

"doccs" = docs codespace

## 📦 Installation

1. If you haven't already, install the `gh` CLI - see the [installation](https://github.com/cli/cli#installation)

   _Installation requires a minimum version (2.0.0) of the the GitHub CLI that supports extensions._

1. Use the GitHub CLI to install the extension:

   ```
   gh ext install https://github.com/hubwriter/gh-doccs
   
   Cloning into '/Users/yourname/.local/share/gh/extensions/gh-doccs'...
   remote: Enumerating objects: 35, done.
   remote: Counting objects: 100% (35/35), done.
   remote: Compressing objects: 100% (30/30), done.
   remote: Total 35 (delta 6), reused 24 (delta 3), pack-reused 0
   Receiving objects: 100% (35/35), 9.65 KiB | 4.83 MiB/s, done.
   Resolving deltas: 100% (6/6), done.
   ✓ Installed extension https://github.com/hubwriter/gh-doccs
   ```
   
## ⚡️ Usage

Run
```sh
gh doccs
```
Then enter a display name for the codespace. Don't use quote marks around the name. The name can include spaces and hyphens.

For example:<br>
<img width="514" alt="image" src="https://user-images.githubusercontent.com/54933897/214870852-ea3e1845-2122-45e1-8df4-b9d23a411cd5.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/54933897/214872075-4ce2bb50-12ed-4c49-b8a3-d857a13baf37.png">


   ```
