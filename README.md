AR — NFT Marker AR demo

This repository contains a marker-based AR scene using A-Frame + AR.js. It has three NFT markers and associated 3D models:

- `img/School.png` -> `markers/School.*` -> `3D/Pupil.glb`
- `img/Class.png`  -> `markers/Class.*`  -> `3D/Book.glb`
- `img/Gym.png`    -> `markers/Gym.*`    -> `3D/Ball.glb`

Quick local test

1. Serve the `AR` folder on your machine (Python):

```bash
cd "/Users/pavel/Documents/University/Year 4/VR/Lab_2/AR"
python3 -m http.server 8000
```

2. Open `http://localhost:8000/index.html` in a modern browser (Chrome/Firefox) and allow camera permissions.
3. Point the camera at the printed images (or another screen showing the images) to see the models.

Notes about NFT support

- The page uses `<a-nft>` elements which require an AR.js build that supports NFT. If you see errors about `a-nft` not being recognized, replace the AR.js script with an NFT-enabled build. I can patch `index.html` to use the correct bundle if needed.

Deploy to Render.com (static site)

1. Push this repository to your GitHub account (already done).
2. Create a new Static Site on Render.com and connect it to your GitHub repo.
3. Use the `master` branch (or the branch you prefer). Set the `Publish directory` to the repository root (where `index.html` is located).
4. Render will build and publish the site. Once published, open the site URL on your mobile device and allow camera access.

If you want, I can add a small `markers/README.md` describing how to regenerate or replace NFT marker files using the NFT Marker Creator tool.
