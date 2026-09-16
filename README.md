# amnezia-awg3-watch

Watcher for stable AmneziaWG 3.x upstream releases.

- Upstream: `amnezia-vpn/amneziawg-go`
- Current baseline: `v3.1.20260828`
- Checks stable `v3.x` Git tags and waits until the matching Docker Hub image exists.
- Creates a GitHub Release only when a newer stable upstream version is detected.
- Does **not** build images and does **not** update the VPS automatically.

Production AWG3 on `v.sim-kin.ru` is managed separately in `/opt/amnezia3` and must be updated manually only after review/testing.
