# release

## Usage

```bash
$ bin/run
```

## Environment Variables

* GITHUB_TOKEN: your_github_token (required)
it can be created from [github token page](https://github.com/settings/tokens/new?scopes=repo) it needs with repo scope

* WEBSITE_REPO_NAME: (default: kaigaiijuch/website)
website generator. it should have `bin/build` and output `public` directory.

* WEBSITE_DATA_REPO_NAME: (default: kaigaiijuch/website_data)
website data repo. it should have `data` directory that contains data files, and map to `data` directory in website repo.

* PAGES_REPO_NAME: (default: kaigaiijuch/kaigaiijuch.github.io)

the static website repo. it should have `docs` directory that serve static files.
