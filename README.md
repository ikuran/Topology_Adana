# TopoLogic World Portal — GitHub Pages

## Publish
1. Create a GitHub repository and upload **the contents of this folder to the repository root** (including `.github`).
2. Use branch `main`.
3. Repository Settings → Pages → Build and deployment → Source: **GitHub Actions**.
4. Actions → Publish TopoLogic Portal → Run workflow (or push a commit).
5. Open the GitHub Pages URL shown in the deployment.

## Add worlds
- Place standalone HTML files directly in `worlds/`, e.g. `worlds/map.html`.
- Place projects with assets in `worlds/project-name/index.html`, with assets next to that file.
- Commit/push changes to `main`. GitHub Actions regenerates `worlds.json` and republishes.
- Removing a world and pushing removes it from the portal.
- No Node.js/server required on GitHub Pages.

## Notes
- VR uses WebXR in the Quest browser over HTTPS. Each opened world must itself implement WebXR for immersive VR.
- Portal's VR interaction / hand tracking requires device testing; opening a world exits the portal's VR session.
- GitHub Pages is case-sensitive; paths and asset URLs should be relative inside each world.
- GitHub Pages will not scan files added only to your local disk: push them to GitHub first.
