# Arhimed Runtime Lab

Public, non-production experiment for the browser isolation required before any ManimGX adapter can enter ArhimedStudio.

```sh
npm ci
npm run build
npm test
```

The current conclusion is negative for an opaque-origin iframe: ManimGX 0.1.1 requires a Blob module Worker that cannot start in this boundary. See [the experiment report](docs/experiment-report.md) and [fixed dependencies](docs/dependencies.md).

The prepared cross-origin protocol and local feasibility results are documented in [cross-origin-progress.md](docs/cross-origin-progress.md). The final acceptance result is published separately because its runtime must have a different HTTPS origin: [Stage 1 HTTPS-origin report](https://github.com/arhimed-runtime/arhimed-runtime.github.io/blob/main/docs/stage-1-https-origin-report.md). The opaque-origin result remains negative; it was not weakened to obtain this result.
