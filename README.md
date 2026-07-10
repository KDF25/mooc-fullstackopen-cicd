# Full Stack open CI/CD

This repository is used for the CI/CD module of the Full Stack Open course

## Blog app (exercises 21–22)

- Repository: https://github.com/KDF25/mooc-fullstackopen-blog-cicd
- Deployed: https://mooc-fullstackopen-blog-cicd.onrender.com

## Deployed application

https://mooc-fullstackopen-cicd.onrender.com

## Commands

Start by running `npm install` inside the project folder

`npm start` to run the webpack dev server
`npm test` to run tests
`npm run eslint` to run eslint
`npm run build` to make a production build
`npm run start-prod` to run your production build

## Render deployment setup

1. Create a **Web Service** at [render.com](https://render.com) connected to this repository.
2. Use these settings:
   - **Build Command:** `./build_step.sh`
   - **Start Command:** `npm run start-prod`
   - **Branch:** `main`
3. In **Advanced**, turn **Auto-Deploy** off.
4. Run **Manual Deploy** and verify `https://<your-app>.onrender.com/version` returns `1`.
5. Copy the **Deploy Hook** URL from Render settings into GitHub secret `RENDER_DEPLOY_HOOK`.
6. Set **Health Check Path** to `/health` in Render settings.
7. Optional: set **Deployment policy** to **Override** for faster recovery from failed deploys.

## GitHub secrets (chapter 6)

- `RENDER_DEPLOY_HOOK` — Render deploy hook URL
- `DISCORD_WEBHOOK` — Discord webhook from course channel `fullstack_webhook` (do not commit)
