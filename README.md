
## Query workflows
```
❯ curl \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/workflows
```

### Trigger an action without parameter(s)
Using workflow path to trigger
```
❯ curl \
  -X POST \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/workflows/manual-event.yml/dispatches \
  -d '{"ref":"main"}'
```
OR (using workflow id)
```
❯ curl \
  -X POST \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/workflows/14022730/dispatches \
  -d '{"ref":"main"}'
```

### Trigger an action with parameter(s)
```
❯ curl \
  -X POST \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/workflows/manual-event.yml/dispatches \
  -d '{"ref":"main", "inputs": {"param": "Work"}}'
```

### Disable a workflow
```
curl \
  -X PUT \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/workflows/manual-event.yml/disable
```

### Enable a workflow
```
curl \
  -X PUT \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/workflows/manual-event.yml/enable
```

### List all jobs of a workflow (NOT YET READY)
```
curl \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/jobs
```
https://github.community/t/job-id-is-string-in-github-job-but-integer-in-actions-api/139060
