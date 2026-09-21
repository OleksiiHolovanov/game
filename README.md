# Erosbound Online — GitHub Pages build

This folder can be published directly with GitHub Pages. No npm install/build step is required.

## Publish
1. Create a GitHub repository.
2. Upload the contents of this folder to the repository root.
3. Open Settings → Pages.
4. Under Build and deployment choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then Save.

The game uses relative asset paths, so it works both on a user site and under `username.github.io/repository-name/`.

## Important limitation
GitHub Pages is static hosting and cannot run the Node.js/Socket.IO server from the original MVP. This build therefore runs the gameplay/NPC quest directly in the browser, stores progress in localStorage, and uses simulated travelers.

For real multiplayer, keep this GitHub Pages frontend and deploy the WebSocket/Socket.IO backend separately (for example on a VPS). Then the client can connect to that backend over HTTPS/WSS.
