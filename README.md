# llm_serve extension packages

Official distribution metadata and extension artifacts. The llm_serve Core repository remains private and is not mirrored here.

## Evaluation releases

`playground-1.6.0` and `benchmarking-1.6.0` are standalone first-party UI packages for the llm_serve plugin host API 1. Each contains only `plugin.json` and `ui.html`; neither contains the Core program, model weights, accounts, credentials, databases, test fixtures, or SDK/CUDA libraries. Package Manager integration is under development; these are evaluation artifacts, not a claim of independent QA approval. Playground's anonymous signed GitHub catalog download, installation, activation and disable have been exercised through the actual Package Manager UI without rebuilding Core or the main UI during installation.

The package embeds the license texts and version inventory of its bundled third-party dependencies in the `third-party-notices` JSON element in `ui.html`. The npm distribution of react-remove-scroll-bar 2.3.8 omits its LICENSE file; its MIT declaration is accompanied by the copyright holder's repository license pinned to commit 8ca9ba5ea52de03308fe8ced94f7b159a44d28ff, with that provenance retained in the notice.

First-party components are distributed with the copyright holder's authorization. This repository does not assert an open-source license for the first-party implementation or for the private Core. Third-party components remain governed by their respective embedded licenses. No SDK or native engine redistribution is authorized by this initial release.

## Verification

`catalog/index.sig` is a detached 64-byte Ed25519 signature over the exact bytes of `catalog/index.json`. `public-key.json` contains the public verification key. A consumer must pin the key through a trusted channel, verify the signature before parsing or publishing metadata, enforce revision/expiry and package length/hash, and validate the inner manifest and every payload before installation. Downloading a key beside an artifact is not independent trust establishment.

Signing keys remain local, encrypted with Windows DPAPI for the publishing user's account; no private key is stored in this repository. Public downloads must not require a GitHub token. Offline import must enforce the same trust and integrity checks. Install only explicitly selected packages; preserve prior working versions and user data.
