# release

It will download the artifact of `WEBSITE_REPO_NAME` by GitHub workflow and commit/make a pull-request to `PAGES_REPO_NAME`

## Usage

```bash
$ bin/run
```

## Environment Variables

* GITHUB_TOKEN: your_github_token (required)
it can be created from [github token page](https://github.com/settings/tokens/new?scopes=repo) it needs with repo scope

* WEBSITE_REPO_NAME: (default: kaigaiijuch/website)

* PAGES_REPO_NAME: (default: kaigaiijuch/kaigaiijuch.github.io)

the static website repo. it should have `docs` directory that serves static files.
