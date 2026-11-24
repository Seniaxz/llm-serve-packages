# llm_serve extension packages

This is the official signed distribution repository for first-party llm_serve plugins and engine packages, including betas. User-created plugins are not accepted in this repository. Community plugins will have a separate repository. The llm_serve Core source is hosted in its private repository.

## Dansk

Dette er det officielle signerede katalog for llm_serve-førstepartsplugins og enginepakker, inklusive betaer. Brugerbyggede plugins må ikke indsendes eller udgives her. De får et særskilt community-repo.

## Initial evaluation releases

`playground-1.6.0` and `benchmarking-1.6.0` are standalone first-party UI packages for the llm_serve plugin host API 1. Each contains only `plugin.json` and `ui.html`; neither contains the Core program, model weights, accounts, credentials, databases, test fixtures, or SDK/CUDA libraries. The initial artifacts were distributed as evaluation releases. Playground's anonymous signed GitHub catalog download, installation, activation and disable have been exercised through the actual Package Manager UI without rebuilding Core or the main UI during installation.

The package embeds the license texts and version inventory of its bundled third-party dependencies in the `third-party-notices` JSON element in `ui.html`. The npm distribution of react-remove-scroll-bar 2.3.8 omits its LICENSE file; its MIT declaration is accompanied by the copyright holder's repository license pinned to commit 8ca9ba5ea52de03308fe8ced94f7b159a44d28ff, with that provenance retained in the notice.

First-party components are distributed with the copyright holder's authorization. This repository does not assert an open-source license for the first-party implementation or for the private Core. Third-party components remain governed by their respective embedded licenses. No SDK or native engine redistribution is authorized by this initial release.

## Verification

`catalog/index.sig` is a detached 64-byte Ed25519 signature over the exact bytes of `catalog/index.json`. `public-key.json` contains the public verification key. A consumer must pin the key through a trusted channel, verify the signature before parsing or publishing metadata, enforce revision/expiry and package length/hash, and validate the inner manifest and every payload before installation. Downloading a key beside an artifact is not independent trust establishment.

Signing keys remain local, encrypted with Windows DPAPI for the publishing user's account; no private key is stored in this repository. Public downloads must not require a GitHub token. Offline import must enforce the same trust and integrity checks. Install only explicitly selected packages; preserve prior working versions and user data.
