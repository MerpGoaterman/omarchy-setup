# omarchy-setup

Point a new Omarchy machine at this from a terminal:

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/MerpGoaterman/omarchy-setup/main/setup)
```

The script clones the private `dotfiles`, `dotskills`, and `memories` repos into the home directory, links them the way this account's machines already do, installs `mem`, and installs the Connect-backed `op` reader at `~/.local/bin/op`.

It opens GitHub login when this machine is not logged in. When `~/.config/op-connect/config.json` is missing, it asks once for the OP Connect token and does not print it. Leave that prompt empty to finish the rest and add the token later.

Run it again to update the three clones. It leaves files and links it did not create. It stops if a checkout has a different origin, or if an existing agent memory file differs from `~/dotfiles/agents.md`.

It does not change Hyprland or other desktop config, does not log in to Tailscale, and does not set a global git identity.

```bash
bash setup --self-test
```
