# amnezia-awg3-watch

Watcher for stable AmneziaWG 3.x upstream releases.

- Upstream: `amnezia-vpn/amneziawg-go`
- Current baseline: `v3.1.20260828`
- Checks stable `v3.x` Git tags and waits until the matching Docker Hub image exists.
- Creates a GitHub Release only when a newer stable upstream version is detected.
- Does **not** build images and does **not** update the VPS automatically.

Production AWG3 on `v.sim-kin.ru` is managed separately in `/opt/amnezia3` and must be updated manually only after review/testing.

## Scheduled workflow maintenance

GitHub may automatically disable scheduled workflows after 60 days without repository activity. If GitHub sends a warning about `Watch AmneziaWG 3.x releases`, check the workflow on the [Actions page](https://github.com/Krezi-777/amnezia-awg3-watch/actions/workflows/watch-awg3.yml) and re-enable it there if it has been disabled.

This watcher runs on a daily schedule (`03:17 UTC`) and can also be started manually (`workflow_dispatch`). A repository documentation commit refreshes repository activity, but does not guarantee the workflow will stay enabled indefinitely without further activity. Monitor the Actions page and GitHub notification emails periodically.
