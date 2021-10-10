

❯ curl \
  -X POST \
  -H "Authorization: token <token>" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/lifuzu/playwithaction/actions/workflows/14022537/dispatches \
  -d '{"ref":"ref", "param": "Work"}'