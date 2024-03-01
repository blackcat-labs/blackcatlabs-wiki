# MkDocs and Material for MkDocs Notes and Info

This site is  built and hosted using Cloudflare Pages' free plan. These are a couple notes on tweaks I needed to get everything working nicely.

## Finalized Build Command
This command is what's currently working to properly build this site:  
**Build command:** `git fetch --unshallow && pip install mkdocs-material mkdocs-git-revision-date-localized-plugin mkdocs-awesome-pages-plugin; mkdocs build --site-dir public`  
**Build output directory:** `/public`

## Awesome-Pages
Using the [mkdocs-awesome-pages-plugin plugin](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin) for navigation.

[Link to info on how to use this plugin](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin?tab=readme-ov-file#features)

## TimeAgo/Revision Date
Because these docs are hosted in a Git repo, we can use the [mkdocs-git-revision-date-localized-plugin plugin](https://github.com/timvink/mkdocs-git-revision-date-localized-plugin) to note for each page when it was last edited/revised.

Because Cloudflare Page's build pipeline by default fetches only the latest revision, we have to add `git fetch --unshallow &&` to the CF build command, to have it fetch the full repo.

## Slack notifications on build
To set up the repo so that we get a Slack notification in `#deploys_static-sites`, we're using the [cloudflare-pages-slack-notification GitHub Action](https://github.com/marketplace/actions/cloudflare-pages-slack-notification).

See [.github/workflows/cf-pages-deploy-slack.yml](https://github.com/blackcat-labs/blackcatlabs-wiki/blob/main/.github/workflows/cf-pages-deploy-slack.yml) for the full working file.

CF account ID and API token: :simple-1password: `CF API token - GitHub Actions > Pages Read` in the `CI/CD` vault.  
Slack webhook for `#deploys_static-sites` channel: :simple-1password: `Slack Webhook - CF Pages Deploy > deploys_static-sites` in the `CI/CD` vault.