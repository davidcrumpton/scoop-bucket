# Scoop Bucket — davidcrumpton

```powershell
scoop bucket add davidcrumpton https://github.com/davidcrumpton/scoop-bucket
scoop install mcwsd
```

## mcwsd

[`mcwsd`](https://github.com/davidcrumpton/mcwsd) is a workspace daemon that
provisions throwaway development environments for coding agents behind a small
HTTP API. The Windows build supports the container-based runtimes that have a
Windows client (Docker Desktop, Podman Desktop, Kubernetes).

```powershell
mcwsd token   # generate a client token, then set MCWSD_TOKEN
mcwsd daemon --plugin "$env:SCOOP\apps\mcwsd\current\plugins\docker.js" `
  --workspace-auth-mode=scoped --port 9080
```

Upgrade with `scoop update mcwsd`.

## Maintenance

Manifests in `bucket/` are **generated automatically** by GoReleaser from the
release workflow in [davidcrumpton/mcwsd](https://github.com/davidcrumpton/mcwsd).
Do not edit them by hand — changes are overwritten on the next release. Issues
and pull requests belong in the mcwsd repository.
