# Smash Ultimate Randomizer

A static website for tier-based Super Smash Bros. Ultimate character randomization. Includes custom default tiers, named saved tier lists, 1–8 players, character histories, stats, and streak notifications.

## Deploy from GitHub to Render

1. Create a new GitHub repository (e.g. `smash-ultimate-randomizer`).
2. Upload **the files inside this folder** (`index.html`, `render.yaml`, and `README.md`) to the **repository root**, not inside a subfolder. Commit to `main`.
3. In Render, choose **New > Blueprint**, connect GitHub if necessary, and select your repository. Render will read `render.yaml` and create a Static Site. Approve the deployment.
4. Wait for deployment, then open the `onrender.com` URL provided by Render.
5. Future commits to the connected branch trigger new deployments automatically, subject to your Render settings.

Alternative: **New > Static Site** in Render, connect the repository, set build command to `echo "Static site ready"` and publish directory to `.`.

## Important data behavior

The site stores tier-list saves, active players, histories, and statistics in each browser's `localStorage`. Publishing it online **does not synchronize data across devices**. A player visiting from another browser/device will have their own separate data. Clearing site data or using a private window can erase saved progress. To share player histories or tier lists across devices, the site would need a backend/database and likely user accounts.

The character portraits are requested from external online image hosts and require internet access. Their availability depends on those hosts.

## Local testing

Open `index.html` directly in a browser. No dependencies or server build are needed.

## Latest changes
- Header uses the online Smash Ball SVG from SmashWiki.
- Reset Players & Stats also restores the full playable fighter pool and clears current picks and streak alerts.
