# Building MkDocs Site on Cloudflare Pages

This site is built and hosted using Cloudflare Pages' free plan. These are a couple notes on tweaks I needed to get everything working nicely.

## Finalized Build Command
This command is what's currently working to properly build this site:  
**Build command:** `git fetch --unshallow && pip install mkdocs-material mkdocs-git-revision-date-localized-plugin; mkdocs build --site-dir public`  
**Build output directory:** `/public`

## TimeAgo 
Because these docs are hosted in a Git repo, we can use the [mkdocs-git-revision-date-localized-plugin plugin](https://github.com/timvink/mkdocs-git-revision-date-localized-plugin) to note for each page when it was last edited/revised.

Because Cloudflare Page's build pipeline by default fetches only the latest revision, we have to add `git fetch --unshallow &&` to the CF build command, to have it fetch the full repo.

## Slack notifications on build
To set up the repo so that we get a Slack notification in `#deploys_static-sites`, we're using the [cloudflare-pages-slack-notification GitHub Action](https://github.com/marketplace/actions/cloudflare-pages-slack-notification).

See [.github/workflows/cf-pages-deploy-slack.yml](https://github.com/blackcat-labs/blackcatlabs-wiki/blob/main/.github/workflows/cf-pages-deploy-slack.yml) for the full working file.

CF account ID and API token: [:simple-1password: 1Password Link](https://start.1password.com/open/i?a=B5NVCNGFJBCCLCDCN5FKFPGVBI&v=6kbovd7ircvwntr34wd4glqq6y&i=kmjq5co7mymutlfz3jg43hb734&h=thhsh.1password.com)  
Slack webhook for `#deploys_static-sites` channel: [:simple-1password: 1Password Link](https://start.1password.com/open/i?a=B5NVCNGFJBCCLCDCN5FKFPGVBI&v=6kbovd7ircvwntr34wd4glqq6y&i=ufg7cmoggpjm2ohsgmkk7up5bm&h=thhsh.1password.com)