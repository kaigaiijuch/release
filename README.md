[![release](https://github.com/kaigaiijuch/release/actions/workflows/release.yml/badge.svg)](https://github.com/kaigaiijuch/release/actions/workflows/release.yml)

# release

It will download the artifact of `WEBSITE_REPO_NAME` by GitHub workflow and commit/make a pull-request to `PAGES_REPO_NAME`

## Usage

```bash
$ bin/run
```

### via GitHub Actions

trigger [the action](.github/workflows/release.yml) by dispatch event.

```bash
curl -L \
  -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${RELEASE_REPO_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/kaigaiijuch/release/dispatches \
  -d '{"event_type":"run_release", "client_payload": {
    "commit_message": "commit_message",
    "commit_url": ""
    }
  }'
```

`RELEASE_REPO_TOKEN` can get from [github token page](https://github.com/settings/tokens/new?scopes=repo), detail is [here](https://docs.github.com/en/rest/reference/repos#create-a-repository-dispatch-event)

## Environment Variables

* GITHUB_TOKEN: your_github_token (required)
it can be created from [github token page](https://github.com/settings/tokens/new?scopes=repo) it needs with repo scope

* WEBSITE_REPO_NAME: (default: kaigaiijuch/website)

* PAGES_REPO_NAME: (default: kaigaiijuch/kaigaiijuch.github.io)

the static website repo. it should have `docs` directory that serves static files.
