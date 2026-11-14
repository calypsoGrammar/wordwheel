# <a href='https://crhisgbibon.github.io/wordwheel/' target='_blank'>word wheel</a>

share score and letter combo
global daily
stats tracker

grades

100% = Diamond
80-99% = 5 star
60-79% = 4 star
40-59% = 3 star
20-39% = 2 star
0-19% = 1 star

Get 9 letter word = Ruby - red
Get 8 letter word = Emerald - green
Get 7 letter word = Sapphire - blue

## Deployment

The site is published to GitHub Pages at <https://calypsogrammar.github.io/wordwheel/> by hand: Actions → **deploy** → Run workflow, with **Dry run** unticked (a dry run builds and checks without publishing). `.github/workflows/deploy.yml` uses the shared Pages deploy in `calypsoGrammar/deploy-workflows`: it builds `dist/` with `npm ci` and `npm run build` from a commit on `main` whose CI `build` job passed, and publishes it. Merging to `main` does not publish. To roll back, run the same workflow with an earlier commit as `ref`, or tick **rollback** to publish the `stable` tag (maintained by `stable.yml`); a rollback holds later deploys until cleared (Actions → stable → Run workflow → `clear-hold`). The Pages source must be "GitHub Actions".
The committed `dist/` folder is not what is published: the deploy builds a fresh `dist/` from source.
