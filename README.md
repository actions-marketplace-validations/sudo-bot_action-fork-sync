# Sync your forks

This action locks a pull-request

## Example usage

```yml
  - name: sync my fork
    uses: sudo-bot/action-fork-sync@v1.0.1
    with:
        branches: master, STABLE, next
        source-url: "https://${{ secrets.BOT_TOKEN }}:x-oauth-basic@github.com/orgname/officialproject.git"
        # Give repo scope to token and access to myname/officialproject-fork for a token user != myname (eg: a bot)
        fork-url: "https://${{ secrets.BOT_TOKEN }}:x-oauth-basic@github.com/myname/officialproject-fork.git"
        dry-run: "true" # remove this line to make sync effective
        clone-depth: "100" # optional, defaults to 100
        sync-method: "fast-forward" # optional, defaults to "fast-forward". Can be "rebase", "merge" or "fast-forward".
```
