# llm_serve extension packages

This is the official signed distribution repository for first-party llm_serve plugins and engine packages, including betas. User-created plugins are not accepted in this repository. Community plugins will have a separate repository. The llm_serve Core source is hosted in its private repository.

## Dansk

Dette er det officielle signerede katalog for llm_serve-førstepartsplugins og enginepakker, inklusive betaer. Brugerbyggede plugins må ikke indsendes eller udgives her. De får et særskilt community-repo.

## Licensing and upstream components

The catalogue distributes official first-party llm_serve packages, including betas. User-created plugins will have a separate community repository.

llm_serve integrates versions made available by upstream publishers such as Intel, AMD and NVIDIA. A third-party component is included only when its applicable terms permit redistribution in that form. Copyrights, trademarks and other intellectual property rights remain with their respective holders. Use, modification and redistribution are governed by the terms applicable to each component and version. See the licence files and third-party notices shipped with the package.

llm_serve is responsible for its own integration and distribution as required by applicable law. Upstream publishers control their own products, drivers, updates and support. To the extent permitted by applicable law, llm_serve assumes no liability for those publishers' independent acts, omissions or product decisions. Mandatory rights and liabilities under applicable law are unaffected.

## Licenser og komponentansvar

Kataloget distribuerer officielle llm_serve-førstepartspakker, inklusive betaer. Brugerbyggede plugins får et særskilt community-repo.

llm_serve integrerer versioner, som de oprindelige udgivere, herunder Intel, AMD og NVIDIA, stiller til rådighed. Vi medtager kun en tredjepartskomponent i det omfang, de gældende vilkår tillader distribution i den pågældende form. Ophavsret, varemærker og øvrige immaterielle rettigheder tilhører de respektive rettighedshavere. Brug, ændring og videredistribution følger vilkårene for hver komponent og version. Se de licensfiler og tredjepartsmeddelelser, der følger med pakken.

llm_serve har ansvar for sin egen integration og distribution efter gældende ret. De oprindelige udgivere bestemmer selv over deres produkter, drivere, opdateringer og support. I det omfang gældende ret tillader det, påtager llm_serve sig ikke ansvar for disse udgiveres selvstændige handlinger, undladelser eller produktbeslutninger. Ufravigelige rettigheder og ansvar efter gældende ret gælder fortsat.

[OpenVINO-licens](https://github.com/openvinotoolkit/openvino/blob/master/LICENSE) · [FastFlowLM-licensvilkår](https://github.com/ROCm/FastFlowLM#license) · [NVIDIA CUDA-vilkår](https://docs.nvidia.com/cuda/eula/index.html)

## Initial evaluation releases

`playground-1.6.0` and `benchmarking-1.6.0` are standalone first-party UI packages for the llm_serve plugin host API 1. Each contains only `plugin.json` and `ui.html`; neither contains the Core program, model weights, accounts, credentials, databases, test fixtures, or SDK/CUDA libraries. The initial artifacts were distributed as evaluation releases. Playground's anonymous signed GitHub catalog download, installation, activation and disable have been exercised through the actual Package Manager UI without rebuilding Core or the main UI during installation.

The package embeds the license texts and version inventory of its bundled third-party dependencies in the `third-party-notices` JSON element in `ui.html`. The npm distribution of react-remove-scroll-bar 2.3.8 omits its LICENSE file; its MIT declaration is accompanied by the copyright holder's repository license pinned to commit 8ca9ba5ea52de03308fe8ced94f7b159a44d28ff, with that provenance retained in the notice.

First-party components are distributed with the copyright holder's authorization. This repository does not assert an open-source license for the first-party implementation or for the private Core. Third-party components remain governed by their respective embedded licenses. No SDK or native engine redistribution is authorized by this initial release.

## Verification

`catalog/index.sig` is a detached 64-byte Ed25519 signature over the exact bytes of `catalog/index.json`. `public-key.json` contains the public verification key. A consumer must pin the key through a trusted channel, verify the signature before parsing or publishing metadata, enforce revision/expiry and package length/hash, and validate the inner manifest and every payload before installation. Downloading a key beside an artifact is not independent trust establishment.

Signing keys remain local, encrypted with Windows DPAPI for the publishing user's account; no private key is stored in this repository. Public downloads must not require a GitHub token. Offline import must enforce the same trust and integrity checks. Install only explicitly selected packages; preserve prior working versions and user data.
