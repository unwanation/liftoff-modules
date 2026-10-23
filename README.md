# liftoff-modules

The module registry of [liftoff](https://github.com/unwanation/liftoff).
Every release here is one version of one module: the WebAssembly component
`<name>-<version>.wasm`, its minisign signature and the registry's
`index.json` (the index of the previous release plus this version).

`liftoffd` and local mode of `lof` read
`https://api.github.com/repos/unwanation/liftoff-modules/releases` by default
and check each component against the SHA-256 in the index and the signature
of the key pinned in their binaries (`REGISTRY_PUBLIC_KEY`).

Releases are published by the `Modules` workflow of the liftoff repository
on a tag `modules/<crate>/vX.Y.Z`; nothing is committed here by hand.
See [docs/MODULES.md](https://github.com/unwanation/liftoff/blob/main/docs/MODULES.md).
