# Changelog

All notable changes to Hippo are documented in this file.

## [v0.1.0-alpha.6] - 2026-05-17


### Features

- Add Dream Journal ([bb86138](https://github.com/Forja-Labs-Mx/hippo/commit/bb8613868d201c618d3dbebe66b2067101780181))


### Fixes

- Omit temperature for gpt-5-nano ([97d9891](https://github.com/Forja-Labs-Mx/hippo/commit/97d989180011844e4c1ef32bc94435871839df9e))
- List grouped project sessions ([b25c3ac](https://github.com/Forja-Labs-Mx/hippo/commit/b25c3ac245ecb7050cc3bc33de7896ac0ed93b4d))
- Enforce journal append-only schema ([9147472](https://github.com/Forja-Labs-Mx/hippo/commit/9147472ccbe546e231f6ce7fb55edb1114dabbc3))


### Other

- Reduce MCP tool count with entity routers ([17e86c1](https://github.com/Forja-Labs-Mx/hippo/commit/17e86c1913b4cfeb43d3b4efaf5dc800baefd23f))
- Address MCP toolset review feedback ([bc3abb9](https://github.com/Forja-Labs-Mx/hippo/commit/bc3abb9ac461e56f5d96627c1c70fe2863ac1260))
## [v0.1.0-alpha.5] - 2026-05-17


### Documentation

- Close HIP-93 acceptance ([d0b896a](https://github.com/Forja-Labs-Mx/hippo/commit/d0b896a8bb050f45a299e9f6685796cc5eb05b25))
- Clarify beta close tracking ([dad519d](https://github.com/Forja-Labs-Mx/hippo/commit/dad519db11d6d122f77b22e58a256adcbafa3c56))


### Features

- Enable Astro view transitions across pages ([e276add](https://github.com/Forja-Labs-Mx/hippo/commit/e276add2de83fc44d760cfa50e429ab29554e858))
- Add OG image and Twitter large-summary card ([332458b](https://github.com/Forja-Labs-Mx/hippo/commit/332458b954161b730ac6d475f72c2843da755a76))
- Make landing and anatomy pages mobile-responsive ([f7a4f39](https://github.com/Forja-Labs-Mx/hippo/commit/f7a4f39a1c7fd5d152e1ee24195a10db41b384ff))
- Dispatch prompt embedding jobs ([49b7ec3](https://github.com/Forja-Labs-Mx/hippo/commit/49b7ec3d7d201ddb2e766d4242210d77c4bceed5))
- Expose learning tools ([23ed5ce](https://github.com/Forja-Labs-Mx/hippo/commit/23ed5ce1b6b9750dabbd49381d466354ac94d086))
- Enqueue prompt embedding jobs ([1fecdda](https://github.com/Forja-Labs-Mx/hippo/commit/1fecdda3b8e3f7ec1960faa54063e6fd373a7aaf))
- Embed learnings through job runner ([fc55912](https://github.com/Forja-Labs-Mx/hippo/commit/fc55912eb8fbf73ffc2aafa6652e463ae689e6ae))
- Split agents step into independent MCP + skill installs ([5ccac9e](https://github.com/Forja-Labs-Mx/hippo/commit/5ccac9ee331cc004d9f0f78577b0f9c2020c717c))
- Upgrade local identity when remote is added ([8c7dcc0](https://github.com/Forja-Labs-Mx/hippo/commit/8c7dcc0f9bf1b75ed36cf3fbe413d8816ec07c98))
- Partition learnings in retrieval ([63b8028](https://github.com/Forja-Labs-Mx/hippo/commit/63b8028f5f2f0377ce5384690641e9453cc664d4))
- Add :prompts command palette ([bb6f112](https://github.com/Forja-Labs-Mx/hippo/commit/bb6f1128b568fa6d5c4072f46ec1bbb8d4682f71))
- Activate Learnings tab with restricted verb surface ([d2c84e8](https://github.com/Forja-Labs-Mx/hippo/commit/d2c84e8bf848db936ca2c1847f0f99733fb34af9))
- Memory detail prompt panels + linked-prompt filter chip ([2f3da09](https://github.com/Forja-Labs-Mx/hippo/commit/2f3da09471d8968b3b2a6ee99c9f308984948f61))


### Fixes

- Rerun anatomy reveal script on view transitions ([f1c6ef3](https://github.com/Forja-Labs-Mx/hippo/commit/f1c6ef3edb1e4e160e33c8b92901ad2c54e8a053))
- Use absolute OG image URLs ([684ef92](https://github.com/Forja-Labs-Mx/hippo/commit/684ef9203182f3201a9565548cca6af9c261207b))
- Guard OG image metadata ([1585b40](https://github.com/Forja-Labs-Mx/hippo/commit/1585b403619756cdae9eb39068b3976515cf4759))
- Abort prior hero run before the mobile early-return ([4df7f3a](https://github.com/Forja-Labs-Mx/hippo/commit/4df7f3a999b6f83cf40946eede79dcafcafbd18d))
- Carry content hash in embedding queue ([e24948e](https://github.com/Forja-Labs-Mx/hippo/commit/e24948ece91c97850d71db2816e1407090c5b48c))
- Clarify embedding enqueue semantics ([f73182c](https://github.com/Forja-Labs-Mx/hippo/commit/f73182c8374a67962d9f27bd5a630757244d6b72))
- Skip dangling embedding jobs ([e1597d3](https://github.com/Forja-Labs-Mx/hippo/commit/e1597d36d739425d51869f884b4b2f03154bd872))
- Use monotonic token for learnings sources view ([0f1143b](https://github.com/Forja-Labs-Mx/hippo/commit/0f1143b8828873c16498a5a287504c254c1c2ae9))
- Enforce session + linked-prompt chips during text search ([e9622ae](https://github.com/Forja-Labs-Mx/hippo/commit/e9622ae8b14cd747793c95a847c0f47494a7c62c))


### Tests

- Assert prompt session start id ([55f4b34](https://github.com/Forja-Labs-Mx/hippo/commit/55f4b34254348f9de26809350771fed5d8199c8d))
- Expand sqlite repo coverage ([d078b4f](https://github.com/Forja-Labs-Mx/hippo/commit/d078b4f04a4ebfed642e3f0f3b0886799334da2d))
## [v0.1.0-alpha.4] - 2026-05-15


### Chores

- Add MIT license publication guard ([b7369c8](https://github.com/Forja-Labs-Mx/hippo/commit/b7369c8e490eb8256a2571f1ff0e0a072a3bb8e2))
- Rename repo port file ([9aa5b47](https://github.com/Forja-Labs-Mx/hippo/commit/9aa5b476df786f6c1badcacd6a40aec6fe545c31))
- Prepare v0.1.0-alpha.4 ([164a0f5](https://github.com/Forja-Labs-Mx/hippo/commit/164a0f54857d02028b2b0ecfe38fe63ab3af8ec4))


### Features

- Summarize closed sessions ([0645703](https://github.com/Forja-Labs-Mx/hippo/commit/06457033bf8313d717f1234d8cc9b40bc5de3b42))
- Expose session tools ([40dade1](https://github.com/Forja-Labs-Mx/hippo/commit/40dade1238d04570de58ff1aa6f579a97894895a))
- Sessions tab + session filter chip + session sort (HIP-71) ([86bbc6e](https://github.com/Forja-Labs-Mx/hippo/commit/86bbc6eb41ae18b0e226df506744c8875be42d6d))
- Add learning service adapters ([8d456ee](https://github.com/Forja-Labs-Mx/hippo/commit/8d456ee6bc32a94a949e0f1fb5e6148532774807))
- Add memory new and edit forms ([593af2b](https://github.com/Forja-Labs-Mx/hippo/commit/593af2ba100ca9d77bede36167ba0fd86d8b6695))
- Add /anatomy long-form field manual page ([bde3b31](https://github.com/Forja-Labs-Mx/hippo/commit/bde3b319b430ed073c0ee73a7c4c543902a68702))
- Add prompt tools ([4b38d91](https://github.com/Forja-Labs-Mx/hippo/commit/4b38d91500bd38594ba7c412b04935f010179cf7))
- Add memory relate and promote sub-modals (HIP-61) ([879a1df](https://github.com/Forja-Labs-Mx/hippo/commit/879a1dfde72adaa40b77456a89165194435a80de))
- Deprioritize prompt results ([d77f9ad](https://github.com/Forja-Labs-Mx/hippo/commit/d77f9ad47d285a3c52ede3eb0bac4bc31dab49ff))
- Add topic-key suggest dropdown on new-memory form (HIP-84) ([e7afd6d](https://github.com/Forja-Labs-Mx/hippo/commit/e7afd6d429e0e0c14c1836a2d0ed26a1f52941dc))
- Synthesize learnings from memory clusters ([b1fad24](https://github.com/Forja-Labs-Mx/hippo/commit/b1fad24ed778aecebd1dca634368f789a5d4d236))
- Reframe agent-guidance harness to decision-point + sessions-first (ADR-0046) ([522c5e2](https://github.com/Forja-Labs-Mx/hippo/commit/522c5e2dcfc9990be9c19b3ba48b02e2b94afc31))


### Fixes

- Guard session summary attempts ([85e4383](https://github.com/Forja-Labs-Mx/hippo/commit/85e4383ec2a20445bd1d75ce5f24a37a2cc866a1))
- Enforce dream-only writes ([15dec28](https://github.com/Forja-Labs-Mx/hippo/commit/15dec2891b5a59494d23b43e789f7a68e3f3da60))
- Keep edit draft on conflict cancel ([d75513d](https://github.com/Forja-Labs-Mx/hippo/commit/d75513d87486e0b760a0ee62a57afcb39ebfb37e))
- Make memory forms non-destructive while saving ([22fc256](https://github.com/Forja-Labs-Mx/hippo/commit/22fc25651360eef486b8d668655eba7ea3dcc039))
- Guard memory form without pinned project ([29f62ae](https://github.com/Forja-Labs-Mx/hippo/commit/29f62aefb48ee43ba72c4442200e677b030759a8))
- Exclude generated db code from errcheck ([d24d994](https://github.com/Forja-Labs-Mx/hippo/commit/d24d994b8690dd954b0407b936c56a199bfb399e))
- Bound suggester ctx and cap dropdown rows (HIP-84) ([ad593c1](https://github.com/Forja-Labs-Mx/hippo/commit/ad593c189112550de522d4ff9eead3b70ceffd7a))
- Link sources for protected learnings ([1b720d7](https://github.com/Forja-Labs-Mx/hippo/commit/1b720d7549189cf0ee0da21e31fa12a1a32f2bcc))
- Address CodeRabbit review on the harness reframe ([784003f](https://github.com/Forja-Labs-Mx/hippo/commit/784003f0ef4f7c842f5060853300f296891f4fd3))


### Other

- Add doctor drift checks ([668e1f8](https://github.com/Forja-Labs-Mx/hippo/commit/668e1f8cee0d01608d7ad764cd6d6246bbae4e03))
- Handle YAML single-quoted provider values ([07e7768](https://github.com/Forja-Labs-Mx/hippo/commit/07e7768a812718f88e58e48bd5d45539e30a05e7))
- Update hippo skills version ([1d56aea](https://github.com/Forja-Labs-Mx/hippo/commit/1d56aeaa2aceeeb898397d8f261909b1307cd974))


### Refactoring

- Address CodeRabbit feedback on HIP-71 + textui helpers ([ea45d0c](https://github.com/Forja-Labs-Mx/hippo/commit/ea45d0c0a9970edb72eee3ea7df802663a038f4d))
## [v0.1.0-alpha.3] - 2026-05-15


### CI

- Mirror docs to hippo-releases on every release ([f789bbd](https://github.com/Forja-Labs-Mx/hippo/commit/f789bbdccdc4b016d87ddd86e41e57edb00c67a4))
- Extract mirror-docs to a typed bun script ([d345242](https://github.com/Forja-Labs-Mx/hippo/commit/d34524201fa776a03df45b8932d57dcc6c3e6f4b))
- Harden mirror-docs git calls with timeout + prompt suppression ([98243f5](https://github.com/Forja-Labs-Mx/hippo/commit/98243f547843efe5763e5a9b349ca9f7249ba7b7))


### Chores

- Refresh OpenAI setup models ([ed96f3b](https://github.com/Forja-Labs-Mx/hippo/commit/ed96f3bdcb94f61bdd4adf79b428cdc2c2208d06))
- Change contact email to hello@forjalabs.com ([3a54318](https://github.com/Forja-Labs-Mx/hippo/commit/3a54318bd084b78d646c52f0ef8a0ffa9a48759a))
- Drop the #ffb3ff hex from the home colophon ([f6b35d3](https://github.com/Forja-Labs-Mx/hippo/commit/f6b35d338f04f1857291a4bb1a89eda5225493a0))
- Scrub Co-Authored-By trailers ([17885aa](https://github.com/Forja-Labs-Mx/hippo/commit/17885aab657e7d5be6564e3f73f8f4d71eaac5d2))
- Drop the typography colophon from the home outro ([cde38e2](https://github.com/Forja-Labs-Mx/hippo/commit/cde38e2550a47977b0a50327d08c2058187f7b4e))
- Pin npm dependency versions ([84e4778](https://github.com/Forja-Labs-Mx/hippo/commit/84e477801b356f728552e70243b631f828e46421))
- Prepare v0.1.0-alpha.3 ([17216ff](https://github.com/Forja-Labs-Mx/hippo/commit/17216ff237fddbe4ffc5cfbe86581690aaee221d))


### Documentation

- Add onboarding TUI redesign sub-plan ([a353fb5](https://github.com/Forja-Labs-Mx/hippo/commit/a353fb561745ddee96030361351e2565be5930b7))
- Add ADR-0044 for init TUI design parity ([b346b34](https://github.com/Forja-Labs-Mx/hippo/commit/b346b3457779bac556ad2eb8c759fa9cdccd8467))
- Clarify TUI receives DefaultNameSource alongside DefaultName ([5124eef](https://github.com/Forja-Labs-Mx/hippo/commit/5124eef158a18e12c26360198f8e38eb21222e7c))


### Features

- Redesign onboarding TUI and skip re-entry of existing keys ([5d0a884](https://github.com/Forja-Labs-Mx/hippo/commit/5d0a8841ba537a4c42e2884bd590b65dc693c450))
- Populate review tab ([bd41752](https://github.com/Forja-Labs-Mx/hippo/commit/bd417520310e6f816cd46f14df85ebd2a97e48ad))
- Add memory filter chips ([cb19719](https://github.com/Forja-Labs-Mx/hippo/commit/cb1971976d0fe43157eac0ec545f9ebfd3a7bc48))
- Add memory archive verbs ([419377c](https://github.com/Forja-Labs-Mx/hippo/commit/419377c3ef8f044efab32c079c29873f40788345))
- Add beta prompt migration ([1fc5a2c](https://github.com/Forja-Labs-Mx/hippo/commit/1fc5a2c2094e249a178b890a01102e1874764d2c))
- Support multi-fire Dream with Times []TimeOfDay ([c8256f5](https://github.com/Forja-Labs-Mx/hippo/commit/c8256f50663060c64c64ad160c1aa18a93c274ae))
- Add SegmentedControl widget and agentpolicy global install helpers ([4d84bed](https://github.com/Forja-Labs-Mx/hippo/commit/4d84bed68dccb5507d5e274b89300b998f9fcc13))
- Teach compact agent memory style ([99973fd](https://github.com/Forja-Labs-Mx/hippo/commit/99973fd685763c0a1499e0b3618fb27efeab0961))
- Wire Review tab a/w/d verbs to hippo_judge ([9871e84](https://github.com/Forja-Labs-Mx/hippo/commit/9871e843ce0d9c9348ae9e674e1f3bf162f7d3de))
- Add prompt models ([6e005ba](https://github.com/Forja-Labs-Mx/hippo/commit/6e005badcbb10ef717660c7884044d26123d691e))
- Rewrite Setup TUI as 5-step arrow-driven flow ([458c4cb](https://github.com/Forja-Labs-Mx/hippo/commit/458c4cbd91637f467e0502aa4c745f855f842d34))
- Add topic key suggestions ([2329877](https://github.com/Forja-Labs-Mx/hippo/commit/2329877bf8b77c531ed60c872512d9f978c297ca))
- Extract chrome package and migrate Setup onto it ([7e1f71a](https://github.com/Forja-Labs-Mx/hippo/commit/7e1f71a43dd76741f982490e03adbff686a0657d))
- Add session service memstore ([ca7ac5d](https://github.com/Forja-Labs-Mx/hippo/commit/ca7ac5d659fc27fe3b9b6b1252b663920346238c))
- Add sqlite session repo ([b826b87](https://github.com/Forja-Labs-Mx/hippo/commit/b826b878ed473353b798f4ba341e733e1b130d33))
- Derive init default name from git origin ([5d5f314](https://github.com/Forja-Labs-Mx/hippo/commit/5d5f314010bf20fd584cf3ca1e8969734980c4ed))
- Add learnings migration ([9f2d34e](https://github.com/Forja-Labs-Mx/hippo/commit/9f2d34e0a8f6871261c78dfc70fbdc4779fb17e5))
- Rewrite init wizard as 4-step flow on chrome ([f49dd90](https://github.com/Forja-Labs-Mx/hippo/commit/f49dd909b5e8f7ea2a3a62a77cb1581ae9c6a3ac))
- Stamp memories with session context ([0bbcfaf](https://github.com/Forja-Labs-Mx/hippo/commit/0bbcfaf946f52751192407096e5b0eb973ca5b97))
- Add / search bar, ranker cycling, and empty state ([627a0d7](https://github.com/Forja-Labs-Mx/hippo/commit/627a0d781d2100c321bb1f4bbf0f89a91b2b409f))
- Add learning models ([0567b6a](https://github.com/Forja-Labs-Mx/hippo/commit/0567b6a739007b43e1568bb9bff9ed5d0592173a))
- Scaffold marketing site with five distinct designs ([d9d15e6](https://github.com/Forja-Labs-Mx/hippo/commit/d9d15e6981b009459b5b312140fe198ac9e3e814))
- Add Download/Docs/GitHub/Roadmap/Changelog CTAs to each design ([6048de9](https://github.com/Forja-Labs-Mx/hippo/commit/6048de96d5e4cabd372332a7052e03031f1fee23))
- Elevate Download + Documentation to the hero on every design ([2b6cee5](https://github.com/Forja-Labs-Mx/hippo/commit/2b6cee51e9660e33b7a27acee0a0532b08de1df0))
- Extract /3 seahorse curl as Hippo logo + favicon ([76bd032](https://github.com/Forja-Labs-Mx/hippo/commit/76bd032ebd55901efb8293c843e01d44243ea7b0))
- Render the real CHANGELOG.md at build time on /changelog ([e6b5484](https://github.com/Forja-Labs-Mx/hippo/commit/e6b54842ac45f1d45059db5c2976e69de3a7ffdf))
- Drive Download pill version from /CHANGELOG.md too ([ca30cbc](https://github.com/Forja-Labs-Mx/hippo/commit/ca30cbc8f2e4ac0d8da5597af86143e20439f591))
- /download page replaces direct-to-GitHub Download CTAs ([7a80f2f](https://github.com/Forja-Labs-Mx/hippo/commit/7a80f2fc0289527d061b0f5633b0bb5a0f268430))
- Add hippo doctor reconciliation ([93188c6](https://github.com/Forja-Labs-Mx/hippo/commit/93188c685931e3a3c264d7bc604eccb412a7e323))
- Reject closed-session adds ([ac3dd12](https://github.com/Forja-Labs-Mx/hippo/commit/ac3dd12ec02a22ed62eb9c82dcc609436a8b9a2c))
- Add memories sort menu (HIP-57) ([e3e7af6](https://github.com/Forja-Labs-Mx/hippo/commit/e3e7af674d9a58bf97cb5f0e5616df87e4f05ed9))
- Full memory detail panel (HIP-58) ([1965aa4](https://github.com/Forja-Labs-Mx/hippo/commit/1965aa404f9d288f4fbc4cdfdb1929f051b344a6))


### Fixes

- Trim keyring secret before prefilling wizard ([9e71a37](https://github.com/Forja-Labs-Mx/hippo/commit/9e71a37c7322b512cd4d9d2d441598e27afad17b))
- Align go module path with repository ([c9912de](https://github.com/Forja-Labs-Mx/hippo/commit/c9912de277329e5da6cd906000a02151b741cce1))
- Use repository module imports ([ec9c4c4](https://github.com/Forja-Labs-Mx/hippo/commit/ec9c4c4b93f748d2385efead1761d840a94e129f))
- Reject inverted date filters ([bd34b9e](https://github.com/Forja-Labs-Mx/hippo/commit/bd34b9e9cc6e7286e0593829e4246ea5d320cfc4))
- Pair EndMarker search from after BeginMarker ([8827980](https://github.com/Forja-Labs-Mx/hippo/commit/882798022894e1b8db066b28cfd398c9df1d0514))
- Decrement Review badge even when row was filtered out ([91463e9](https://github.com/Forja-Labs-Mx/hippo/commit/91463e91c96ae4eb15a07fdd45170e870e6a69fa))
- Allow leaving dream phases with arrows ([4c7125d](https://github.com/Forja-Labs-Mx/hippo/commit/4c7125dcede80bdbba0efed9add268f78d07a1d7))
- Match topic key project flag ([42c47f4](https://github.com/Forja-Labs-Mx/hippo/commit/42c47f4eb8a8d1135638878cda160fc649a3995f))
- Expose list pagination cursor ([25866e6](https://github.com/Forja-Labs-Mx/hippo/commit/25866e66a4e25e25f40e7f99a5b74d175a9dacbc))
- Validate topic key suggestions ([fad7d49](https://github.com/Forja-Labs-Mx/hippo/commit/fad7d49437bf693eb7a238137d2477e254da3fb7))
- Address learnings migration review ([c22c8ca](https://github.com/Forja-Labs-Mx/hippo/commit/c22c8ca5f1dff80b75fc70515e12d511be032ab7))
- Wire embedder + overfetch in TUI search adapter ([76b72bf](https://github.com/Forja-Labs-Mx/hippo/commit/76b72bf2bc6eca0d0e780600ba146ce5a98926cc))
- Fail fast on embedder setup errors in hippo ui ([ab0a152](https://github.com/Forja-Labs-Mx/hippo/commit/ab0a1528e03a71c97599be8815b33e203a0f92ef))
- Publish artifacts to public repos ([a39ad4f](https://github.com/Forja-Labs-Mx/hippo/commit/a39ad4f47c45fad807f2d506c28af94725cd5aaf))
- Ignore zero optional timestamps ([b59285d](https://github.com/Forja-Labs-Mx/hippo/commit/b59285d0480a75c2173e9f3717991d583e0eace5))
- Auto-run migrations for configured databases ([e174a3a](https://github.com/Forja-Labs-Mx/hippo/commit/e174a3a7d0baff8e32fd6d46bde5b70180454ef5))
- Synapse cursor disappears after scroll back into hero ([6378224](https://github.com/Forja-Labs-Mx/hippo/commit/6378224bd833827b3b6d58d4e9bb3522deef1855))
- Ground every copy claim in README, ADRs, and source ([b586778](https://github.com/Forja-Labs-Mx/hippo/commit/b586778b1ab8ba5a8d414035e334e362fcb52be1))
- Shift Synapse gravity well right so graph clears the headline ([3510a32](https://github.com/Forja-Labs-Mx/hippo/commit/3510a32bee2430adb7a0ad2ed37db4a4fb2239fb))
- Address CodeRabbit review (dev host binding + link affordance) ([980bf90](https://github.com/Forja-Labs-Mx/hippo/commit/980bf90a6ab9e8109333bda005fde6c8a57a07f9))
- /download "From source code" — access by request ([28b7046](https://github.com/Forja-Labs-Mx/hippo/commit/28b70464211d1e19396cb94463d429de3d9e14e8))
- Make the custom cursor snap to the pointer ([7df5782](https://github.com/Forja-Labs-Mx/hippo/commit/7df5782ae70dbca41382fc5b439e0288aae1b254))
- Repoint live pages from hippo to hippo-releases ([f7caf84](https://github.com/Forja-Labs-Mx/hippo/commit/f7caf84af3a84e2778c30177af5c45c979337651))
- /download source-code paragraph names the right repo ([dc74b98](https://github.com/Forja-Labs-Mx/hippo/commit/dc74b98e379e0294ced520920cb47d1d408f3c1d))
- Route keys to sort modal before filters ([be06f60](https://github.com/Forja-Labs-Mx/hippo/commit/be06f60a7855edf55fe34ae57e11aee79ed303ef))
- Install Bun for Railway ([ee59ddf](https://github.com/Forja-Labs-Mx/hippo/commit/ee59ddf357237c7c4f0206ca6ceba12879484dd0))
- Serve Railway site with Caddy ([361cb32](https://github.com/Forja-Labs-Mx/hippo/commit/361cb32d4f4357a38ee0eaf05e2b08994b655ed3))
- Harden Caddy container ([50e61ab](https://github.com/Forja-Labs-Mx/hippo/commit/50e61ab8e0a90459decb6aa91193def8e1fc1585))
- Narrow Railway trusted proxy range ([f61d417](https://github.com/Forja-Labs-Mx/hippo/commit/f61d417f08a3a90b48ce602c0daf13cdf315272c))


### Other

- Add scheduled Dream failure notifications ([6558a38](https://github.com/Forja-Labs-Mx/hippo/commit/6558a385213973c7246c1caed47c40a51768f2b1))
- Fix Dream run migration version ([aa684dd](https://github.com/Forja-Labs-Mx/hippo/commit/aa684dd6de6718bb176ddcaca03a660d57b76128))
- Harden configured database path loading ([c21eb6c](https://github.com/Forja-Labs-Mx/hippo/commit/c21eb6c96ed2c6f66432225aecd67793e414e607))
- Add Cursor and OpenCode setup support ([ae389d9](https://github.com/Forja-Labs-Mx/hippo/commit/ae389d9af22daac9c3e3c26aef4b1b839dac4790))
- Add security audit skill ([b9d90af](https://github.com/Forja-Labs-Mx/hippo/commit/b9d90af457a293d66428fd654e7cf51f8ad10829))
- Share project skill files across agents ([1a5d64f](https://github.com/Forja-Labs-Mx/hippo/commit/1a5d64f054d58aec07e0471d90b6f28b9f12ca4f))
- Configure Railway ([a2538e4](https://github.com/Forja-Labs-Mx/hippo/commit/a2538e4838e823913bc9acb932d8dd88d92aefd3))
- Improve Hippo memory search guidance ([54e2a38](https://github.com/Forja-Labs-Mx/hippo/commit/54e2a38516268409264be99b13dcc586ba80dd2b))


### Refactoring

- Key per-query maps by (text, want_id) ([3d440b8](https://github.com/Forja-Labs-Mx/hippo/commit/3d440b86ca57559661d3b969d3ee915216acc791))
- Polish Synapse — scoped hover, refined pulses, hero reveal ([8861675](https://github.com/Forja-Labs-Mx/hippo/commit/8861675d048a1f2cef1516001c6c42b3fa70d546))
- Promote /5 to /, archive designs 1-4, add /roadmap ([55d3ca1](https://github.com/Forja-Labs-Mx/hippo/commit/55d3ca16bfdea09f3ab2f90046078c422cfb5ae7))


### Tests

- Clarify concurrent close capture ([09f7a8e](https://github.com/Forja-Labs-Mx/hippo/commit/09f7a8e5a04486b8fb43103040b832d662f66cb5))
## [v0.1.0-alpha.2] - 2026-05-13


### Chores

- Prepare v0.1.0-alpha.2 ([3666a27](https://github.com/Forja-Labs-Mx/hippo/commit/3666a2751ebb3ccabbc3238348ac5c6e553f2c9c))


### Fixes

- Allow git-cliff to read PR metadata ([adfeaf4](https://github.com/Forja-Labs-Mx/hippo/commit/adfeaf4dd025b6f0f48aa966ddae4a884303348c))
- Make TUI collect credentials safely ([28eba12](https://github.com/Forja-Labs-Mx/hippo/commit/28eba1246e815893e583a21341663de4c266bd89))
## [v0.1.0-alpha.1] - 2026-05-13


### CI

- Add govulncheck ([9bb8c56](https://github.com/Forja-Labs-Mx/hippo/commit/9bb8c56479140fd1f5c45944127cb351627729bf))
- Serialize parallel golangci-lint runners ([d6fb37e](https://github.com/Forja-Labs-Mx/hippo/commit/d6fb37eacab12af6cb9f3c636dcd3878c5039917))
- Add mac and linux release pipeline ([5bb6e4a](https://github.com/Forja-Labs-Mx/hippo/commit/5bb6e4a6c819909b1048095791563478b9615aaa))
- Publish from merged release PRs ([20ac630](https://github.com/Forja-Labs-Mx/hippo/commit/20ac6303cce20c27ae82db6dc2920ad3950d458a))
- Restrict manual publishing to main ([678a29e](https://github.com/Forja-Labs-Mx/hippo/commit/678a29ea8e931a65a4227fc53eabef243e94099f))
- Harden release workflow ([076714b](https://github.com/Forja-Labs-Mx/hippo/commit/076714bb22b7d1984cd8c6a5959f36abd0dd8345))


### Chores

- Upgrade go to 1.26 ([#12](https://github.com/Forja-Labs-Mx/hippo/issues/12)) ([e0640e9](https://github.com/Forja-Labs-Mx/hippo/commit/e0640e97d07a6d8a1cf1493aaa0be68b939e11ac))
- Replace tdd skill ([3b61514](https://github.com/Forja-Labs-Mx/hippo/commit/3b615148fab2e01b43a216abd7f741aab77c194c))
- Restore tdd anti-patterns reference ([b404358](https://github.com/Forja-Labs-Mx/hippo/commit/b4043584534d4a881193204c5318a712fd622c03))
- Add diagnosis and docs grilling skills ([4c9e1f3](https://github.com/Forja-Labs-Mx/hippo/commit/4c9e1f3023c743337adae22cef07b883762762b4))
- Update hippo skills ([4f74bf5](https://github.com/Forja-Labs-Mx/hippo/commit/4f74bf5bb3460fa9bb7b63b73f9dd7dd155433fd))
- Prepare v0.1.0-alpha.1 ([3721e6f](https://github.com/Forja-Labs-Mx/hippo/commit/3721e6fcd17c335a7a7363625ece2c4c5049d455))


### Documentation

- Clarify project identity fallback ([254b7cd](https://github.com/Forja-Labs-Mx/hippo/commit/254b7cd2a6309cea9ad1b1c237085587668be77f))
- Mark Alpha milestone as shipped ([b4bb0fa](https://github.com/Forja-Labs-Mx/hippo/commit/b4bb0fa5721e9396ec0636b295515d867646c56b))
- Replace MCP tool wildcards with shipped names ([efebf02](https://github.com/Forja-Labs-Mx/hippo/commit/efebf0209b48077d9e9cc56261ed037367b471fb))
- Add language hints to layout fences ([87b381e](https://github.com/Forja-Labs-Mx/hippo/commit/87b381e5c72101ee8b95275a7715b57632188935))
- Capture post-Alpha enhancements in README, roadmap, and ADRs ([208383c](https://github.com/Forja-Labs-Mx/hippo/commit/208383c8db34132596d1a6302a606a2f5ef33cf0))
- Land Beta plan + ADRs 0037–0042; promote ADR-0027 ([a977152](https://github.com/Forja-Labs-Mx/hippo/commit/a9771522d6a0021fe81434eb62147ca17f2a155d))
- Address CodeRabbit review on PR #64 ([e8f93e2](https://github.com/Forja-Labs-Mx/hippo/commit/e8f93e2ceec227c60a86594b4a9f58009c934c9e))
- Clarify widget lifecycle contract ([b1532f1](https://github.com/Forja-Labs-Mx/hippo/commit/b1532f104b7a6537d0b4ef9fbbcf853b0d3614c1))
- Clarify timestamp model boundary ([88208ae](https://github.com/Forja-Labs-Mx/hippo/commit/88208ae4cbb68494112f15a6d6bedaafb3437ab5))
- Define work episode boundary ([15e2cb0](https://github.com/Forja-Labs-Mx/hippo/commit/15e2cb0840fd8385aa44af45198100017ea44532))
- Clarify closed-session rejection ([8077141](https://github.com/Forja-Labs-Mx/hippo/commit/80771419dbad9b68e9184cb2c5ccbbc41c9937f3))
- Align SKILL.md session-summary rule with reference ([3e257e4](https://github.com/Forja-Labs-Mx/hippo/commit/3e257e410a7310afa8f9b678a5d427f7486ac8d9))


### Features

- Scaffold Hippo CLI foundation ([#7](https://github.com/Forja-Labs-Mx/hippo/issues/7)) ([1e93f45](https://github.com/Forja-Labs-Mx/hippo/commit/1e93f45a622d8e4ff101362833d9d98776ae3a7a))
- Add foundation primitives ([#8](https://github.com/Forja-Labs-Mx/hippo/issues/8)) ([3ed9bed](https://github.com/Forja-Labs-Mx/hippo/commit/3ed9bedfc14b880b3e7026e564efcb5d63239106))
- Add identity domain models ([#9](https://github.com/Forja-Labs-Mx/hippo/issues/9)) ([4b59d1a](https://github.com/Forja-Labs-Mx/hippo/commit/4b59d1ab3d8ce55fa1f9a58b8a9cb8c9ce85b3de))
- Add in-memory project service ([#10](https://github.com/Forja-Labs-Mx/hippo/issues/10)) ([0b372fa](https://github.com/Forja-Labs-Mx/hippo/commit/0b372fac8e246f2b1e5c3b8bf7d0ea3e2c3320f9))
- Add go-guidelines skill and install skill-creator ([#13](https://github.com/Forja-Labs-Mx/hippo/issues/13)) ([57b0e8a](https://github.com/Forja-Labs-Mx/hippo/commit/57b0e8ab5b44b4df94b66627172c97b236c75326))
- Add slice 4 domain models ([#14](https://github.com/Forja-Labs-Mx/hippo/issues/14)) ([f1988a2](https://github.com/Forja-Labs-Mx/hippo/commit/f1988a27bb081c063e12f1b964b96526f33c738b))
- Add in-memory CRUD service ([#15](https://github.com/Forja-Labs-Mx/hippo/issues/15)) ([9a6e198](https://github.com/Forja-Labs-Mx/hippo/commit/9a6e198fbb70decfc0b3ab375a89d7b76c8f0246))
- Add in-memory preference service ([#16](https://github.com/Forja-Labs-Mx/hippo/issues/16)) ([edba4e4](https://github.com/Forja-Labs-Mx/hippo/commit/edba4e498387d9976420bbf1af94c73a9ec91d5d))
- Add SQLite migration foundation ([#17](https://github.com/Forja-Labs-Mx/hippo/issues/17)) ([1863b0e](https://github.com/Forja-Labs-Mx/hippo/commit/1863b0ed5dc7ebf65c68a86cdd0a2453bf806313))
- Add sqlite repo adapters ([#19](https://github.com/Forja-Labs-Mx/hippo/issues/19)) ([f2901a7](https://github.com/Forja-Labs-Mx/hippo/commit/f2901a7da62a5650974addd626d93d7ed2bf9eac))
- Add FTS keyword search repo ([#20](https://github.com/Forja-Labs-Mx/hippo/issues/20)) ([2c1ce2d](https://github.com/Forja-Labs-Mx/hippo/commit/2c1ce2daf5ae221181fadf09b44b61b6c2923989))
- Add OpenAI-compatible embedder ([#21](https://github.com/Forja-Labs-Mx/hippo/issues/21)) ([9698879](https://github.com/Forja-Labs-Mx/hippo/commit/96988794976c2cf79915b6d46909fafd5e14ead4))
- Add hybrid cosine reranking ([f73ee74](https://github.com/Forja-Labs-Mx/hippo/commit/f73ee74c4fb23f1371b74750d0936d795a3d1cb2))
- Add setup and project init commands ([189ea30](https://github.com/Forja-Labs-Mx/hippo/commit/189ea30bcb9d51e72e9dd0d4af7c8362e38ac263))
- Add retrieval and audit tools ([87e038e](https://github.com/Forja-Labs-Mx/hippo/commit/87e038e0a7806167b9a836f8fb00e5fefef373ec))
- Add deterministic maintenance phases ([e4dfd67](https://github.com/Forja-Labs-Mx/hippo/commit/e4dfd679ea7a31c111ae85f58d9c1513223b923b))
- Add LLM phases and judge workflow ([1b24a92](https://github.com/Forja-Labs-Mx/hippo/commit/1b24a9281136ea56a1e1d2aee254bb1d9917db2a))
- Add scheduler installers ([e7782f7](https://github.com/Forja-Labs-Mx/hippo/commit/e7782f75e4b9b63a3284e84e8d519d982d9c7c7d))
- Add --dry-run preview mode to dream run ([885f0f2](https://github.com/Forja-Labs-Mx/hippo/commit/885f0f2bf63abe6cbfb4fb52b8f51c0ff5ed565e))
- Wire production services ([241674f](https://github.com/Forja-Labs-Mx/hippo/commit/241674f3c5d2b8ad6492e7b08a24bdddf8c4b4b2))
- Audit project and preference mutations ([5cebab3](https://github.com/Forja-Labs-Mx/hippo/commit/5cebab35fb62a37fbc6f65693c5210418750992c))
- Add dream review promotion surfaces ([880e3a2](https://github.com/Forja-Labs-Mx/hippo/commit/880e3a20d4ae628b7248ca44758918be8cafaea2))
- Add ambient Hippo agent memory guidance ([21b0858](https://github.com/Forja-Labs-Mx/hippo/commit/21b08580ba759c1863f5de22bb01a999917688bf))
- Score promotions with reinforcement ([de5d0ab](https://github.com/Forja-Labs-Mx/hippo/commit/de5d0ab11c4ee110dba537a1487eb6c9b07566b7))
- Add project groups service API ([f050e2a](https://github.com/Forja-Labs-Mx/hippo/commit/f050e2a60eff08ca9b357888e1ff594772189d95))
- Allow grouped project read visibility ([11901ec](https://github.com/Forja-Labs-Mx/hippo/commit/11901ecc2ddb9fa9f84a7878038bb3dcfe41e46d))
- Score promotions with project group context ([fa8921d](https://github.com/Forja-Labs-Mx/hippo/commit/fa8921dfbe39819dcd1d70722f015d8ec3f3c06c))
- Add group CLI and MCP tools ([66757bf](https://github.com/Forja-Labs-Mx/hippo/commit/66757bf706de3e81383131c2f8431b32db7ba92e))
- Guide users through provider, MCP agent, and Dream install ([d51519b](https://github.com/Forja-Labs-Mx/hippo/commit/d51519b6da1671dd21b2e8f582484cd6d69aa786))
- Add project listing and search filters ([c46c15b](https://github.com/Forja-Labs-Mx/hippo/commit/c46c15bb204a95ff2b17e59a56dedc4b0b3b972a))
- Scaffold widgets package with text + step primitives (HIP-44) ([68f957e](https://github.com/Forja-Labs-Mx/hippo/commit/68f957ef495b216fc34c37f732748e237604dbac))
- Add filtered list and unarchive ([f60c849](https://github.com/Forja-Labs-Mx/hippo/commit/f60c84967478157f94875d7bfb505d2594fcb1f2))
- Add beta sessions migration ([843d85f](https://github.com/Forja-Labs-Mx/hippo/commit/843d85f970f14532a817b47a7b8ce9d83850ee90))
- Add open closed lifecycle model ([f65951b](https://github.com/Forja-Labs-Mx/hippo/commit/f65951bade39a72d5827a4671dc0d5885a2583f4))
- Add selection modal chip widgets ([3ccc288](https://github.com/Forja-Labs-Mx/hippo/commit/3ccc288391696b8469af748b6ae0e872382958d6))
- List pending review suggestions ([b563f1b](https://github.com/Forja-Labs-Mx/hippo/commit/b563f1b37a4ee8574a16e0cbcf03d404579e2167))
- Add debug shell command ([439184c](https://github.com/Forja-Labs-Mx/hippo/commit/439184ce7f58e26b69c320867b177531b8d2b12d))
- Add init TUI shell ([66ad172](https://github.com/Forja-Labs-Mx/hippo/commit/66ad1729d49bb217e85df4aa294d467d1139da45))
- Add setup TUI wrapper ([f7839b9](https://github.com/Forja-Labs-Mx/hippo/commit/f7839b93d01e60000a8213f7bd9de752509818b8))
- Rewrite hippo-memory skill to teach a model, not a checklist ([23e9ca2](https://github.com/Forja-Labs-Mx/hippo/commit/23e9ca2dd25bd40e7433cfa9910365a980922c41))
- Add memories master-detail list ([6c4a4d8](https://github.com/Forja-Labs-Mx/hippo/commit/6c4a4d8a747d0c193f5e45e7e6d46b7199f38e2f))
- Add project init wizard ([7ed1adb](https://github.com/Forja-Labs-Mx/hippo/commit/7ed1adb3eb02c3936f4370b24996633d1097e4af))
- Add setup TUI wizard ([441bc7e](https://github.com/Forja-Labs-Mx/hippo/commit/441bc7ededffc0bf2884c638b523807b93b9a205))


### Fixes

- Address project init review feedback ([acf7490](https://github.com/Forja-Labs-Mx/hippo/commit/acf7490195e7bb6dca381091a102200a1e504df5))
- Validate retrieval tool inputs ([369cc9d](https://github.com/Forja-Labs-Mx/hippo/commit/369cc9dc459066d91ff3825fb3c792b2e1ccce21))
- Validate run flag bounds ([ef88fe0](https://github.com/Forja-Labs-Mx/hippo/commit/ef88fe09c9ac2a88f130c860c64c6cda752922bc))
- Stabilize promotion idempotency key ([add4cdf](https://github.com/Forja-Labs-Mx/hippo/commit/add4cdfb42c4da246487642a3ec52b76f9e36c97))
- Address HIP-24 review hardening comments ([7cbaf29](https://github.com/Forja-Labs-Mx/hippo/commit/7cbaf2959ecf437b736e4e06ea57ba729f11951c))
- Fix embedding rebuild database path ([8f7ed20](https://github.com/Forja-Labs-Mx/hippo/commit/8f7ed20bba0f8e17d5406da38f4d228bb0ae2667))
- Align CLI project identity resolution ([cc4ea0a](https://github.com/Forja-Labs-Mx/hippo/commit/cc4ea0a77a6785c6bda55b0c2cc97fcdb502e2fb))
- Address project identity review feedback ([fc344a3](https://github.com/Forja-Labs-Mx/hippo/commit/fc344a35c37780bbcf14d7e83b2973d193d8e774))
- Propagate git remote resolution errors ([44d9abd](https://github.com/Forja-Labs-Mx/hippo/commit/44d9abd537cc2641c531b23d1e40ba47634ab6c4))
- Enforce access scope in raw SQL queries ([88eba66](https://github.com/Forja-Labs-Mx/hippo/commit/88eba6624937d51b0f9206799fc65c98b7ceea66))
- Report scoped memory update misses ([55a54fb](https://github.com/Forja-Labs-Mx/hippo/commit/55a54fbc90248b1f870359dd5ccb5c56975a6ce1))
- Wake embedding ticker after commit ([c3e41b7](https://github.com/Forja-Labs-Mx/hippo/commit/c3e41b7cee8fd1c008342442ae731f24ec543730))
- Register hippo judge in production ([a9312c2](https://github.com/Forja-Labs-Mx/hippo/commit/a9312c2733fe955fcbebcf0ac795bd2810d574d4))
- Pass audit service in integration wiring ([9a0c5f7](https://github.com/Forja-Labs-Mx/hippo/commit/9a0c5f73f32271ffdf544ad3493958b8f88f9031))
- Avoid unredacted JSON fallback ([14555be](https://github.com/Forja-Labs-Mx/hippo/commit/14555be6b424861f32bc8c992bb21c655d85796e))
- Return relations from memory get ([b30f98a](https://github.com/Forja-Labs-Mx/hippo/commit/b30f98ac3b392c7f466a798b6f0a981509df2ced))
- Validate dream review promotion inputs ([a8b9d7e](https://github.com/Forja-Labs-Mx/hippo/commit/a8b9d7ede9aee3149c39164078923807e414f140))
- Harden dream review service guards ([186038d](https://github.com/Forja-Labs-Mx/hippo/commit/186038d8756ff35bce34f3de815d6e21a3a4478b))
- Default to setup database ([b190e63](https://github.com/Forja-Labs-Mx/hippo/commit/b190e6308572133162af86fb34056d06190b5fab))
- Recover malformed Hippo agent blocks ([add3eea](https://github.com/Forja-Labs-Mx/hippo/commit/add3eea4469a7785ed3d68b7546b36df31e4ba05))
- Dedupe promotion suggestions ([6b143d5](https://github.com/Forja-Labs-Mx/hippo/commit/6b143d542d32ea7ad8e780cd8eb5914165415b86))
- Address group review feedback ([6fe7bbb](https://github.com/Forja-Labs-Mx/hippo/commit/6fe7bbb1a0da36d22fce7f375b4edcc5ee33c1c8))
- Reject invalid --agent values before running setup ([9c2c384](https://github.com/Forja-Labs-Mx/hippo/commit/9c2c384d1c3aad2baccaf5a17525b7a15e516621))
- Scope project listing ([2352944](https://github.com/Forja-Labs-Mx/hippo/commit/2352944fd9852950546f7675e6580fdc0cf5d0c3))
- Include group-readable projects ([99763f9](https://github.com/Forja-Labs-Mx/hippo/commit/99763f9c9ff7bd8d9ec60eb469f66b00634c0cb6))
- Sequence sessions migration after tui audit ([d28f15c](https://github.com/Forja-Labs-Mx/hippo/commit/d28f15c34c8082552716cdf7140a49908e2472a4))
- Page review suggestions in sqlite ([61db6fc](https://github.com/Forja-Labs-Mx/hippo/commit/61db6fc92b8918153fed7c31c29acc8bd0084ad3))
- Report setup TUI config load errors ([9799816](https://github.com/Forja-Labs-Mx/hippo/commit/9799816431ab0d81b4c5c6257227b35af9f09dcf))
- Address HIP-49 review feedback ([cb32e9e](https://github.com/Forja-Labs-Mx/hippo/commit/cb32e9e7c59a3dfcfb15a41b27773271aa372fec))
- Fallback for broad keyword queries ([161575b](https://github.com/Forja-Labs-Mx/hippo/commit/161575b9d0c427e0f9ac1e321cea6c3776f76786))


### Other

- Initial commit ([7831c6d](https://github.com/Forja-Labs-Mx/hippo/commit/7831c6df8749942316d521ce274c605d4dc9ea0b))
- Initial commit ([3fa5c11](https://github.com/Forja-Labs-Mx/hippo/commit/3fa5c111e02edef3c07d2012e40b0927b744eda7))
- Add Hippo Alpha design docs: README, plan, ADRs, roadmap

Lands the full Alpha design in docs/. The plan (docs/plans/alpha/) is
sectioned across context, architecture, data model, build order (21
TDD slices), testing & verification, and out-of-scope, plus a
single-document abstract. 32 ADRs in docs/adr/ capture every
load-bearing decision: service-oriented + ports & adapters, pure-Go
SQLite stack with FTS5 external-content, BLOB embeddings + in-Go
cosine, AccessContext-enforced scope isolation, MCP transport split,
progressive-disclosure retrieval, topic-key upsert, store-layer
redaction, idempotency primitive, single-threaded concurrency
posture, TxManager port with reentrant context propagation +
after-commit hooks, domain primitives (DomainError, ValueObject,
constructor pattern), Learnings as a Beta entity, and cross-project
memory elevation. Roadmap places Alpha → Beta → 1.0 milestones with
explicit scope and acceptance signals. README orients new readers.
No code changes — implementation will follow per the Build Order
slices. ([91fa22c](https://github.com/Forja-Labs-Mx/hippo/commit/91fa22cf56f622016495b9ff5ae3be041b7e95d2))
- Document canonical alpha schema ([#2](https://github.com/Forja-Labs-Mx/hippo/issues/2)) ([c3339d7](https://github.com/Forja-Labs-Mx/hippo/commit/c3339d71de7d55e74f314b311ac98075681b0318))
- [codex] Move Hippo to Bun/Turborepo monorepo ([#3](https://github.com/Forja-Labs-Mx/hippo/issues/3))

* Move Hippo app into apps workspace

* Configure Bun Turborepo monorepo

* Add turborepo agent skill ([727790e](https://github.com/Forja-Labs-Mx/hippo/commit/727790e5f9665d134cafd090c96d35d2cec766ee))
- Add PR creation workflow ([#4](https://github.com/Forja-Labs-Mx/hippo/issues/4)) ([fdfb7c4](https://github.com/Forja-Labs-Mx/hippo/commit/fdfb7c46e85c8dd67b121847b4d2cd5549ead93a))
- Configure go quality tasks ([#5](https://github.com/Forja-Labs-Mx/hippo/issues/5)) ([db68126](https://github.com/Forja-Labs-Mx/hippo/commit/db68126d7c30621eb44d01170ebcfe6b816d85cc))
- Configure lefthook checks ([#6](https://github.com/Forja-Labs-Mx/hippo/issues/6)) ([e3ffb73](https://github.com/Forja-Labs-Mx/hippo/commit/e3ffb732891b15f5f0e15ce8c185113127b0b0a7))
- Add Turbo-backed GitHub Actions CI ([#11](https://github.com/Forja-Labs-Mx/hippo/issues/11))

* Add Turbo-backed GitHub Actions CI

* Harden Turbo CI cache checks ([0b859cb](https://github.com/Forja-Labs-Mx/hippo/commit/0b859cb5c44a06d01be2e3316945c5daede30858))
- Implement embedding job queue ([#22](https://github.com/Forja-Labs-Mx/hippo/issues/22))

* Implement embedding job queue

* Address embedding queue review feedback ([5cd3668](https://github.com/Forja-Labs-Mx/hippo/commit/5cd3668f1867151bf990ed9c0945ac19a61d3572))
- Add memory search and ask CLI commands ([eb4aaaf](https://github.com/Forja-Labs-Mx/hippo/commit/eb4aaafa65d412c8a32a3ade27f40753ab21f889))
- Add MCP memory tools ([400feef](https://github.com/Forja-Labs-Mx/hippo/commit/400feefde1c5021cb4e7403bafe8b59023223a1d))
- Address MCP review feedback ([eec936c](https://github.com/Forja-Labs-Mx/hippo/commit/eec936cf8f0d7173b209fcedcca07640ff575d23))
- Add LLM-backed memory structuring

- Introduce OpenAI and Anthropic text providers
- Auto-structure raw memory input through the MCP tool
- Add structured memory path and tests ([cbf840e](https://github.com/Forja-Labs-Mx/hippo/commit/cbf840e9563eb3fb0cd0ed42f7103267a3db3b50))
- Tighten memory structuring validation

- Require complete structured fields before skipping LLM structuring
- Reject structured output missing category, body, or metadata
- Add tests for partial raw input and missing required fields ([93e1a82](https://github.com/Forja-Labs-Mx/hippo/commit/93e1a8234d78c5fe81d8eb80b76c2d6b982a0ed7))
- Migrate workflows to Blacksmith ([1daface](https://github.com/Forja-Labs-Mx/hippo/commit/1daface73f68cf77de741a4bcd80dcf73adbdeeb))
- Wire text provider config into runtime ([423ef2d](https://github.com/Forja-Labs-Mx/hippo/commit/423ef2de5e86d34740babaf25792af5f4bfe7eab))
- Address text provider config review feedback ([af73489](https://github.com/Forja-Labs-Mx/hippo/commit/af73489ee9b63d1b6a54c8187cb88e0c5cab4d7a))
- Add agent promotion suggestion flow ([ea1578a](https://github.com/Forja-Labs-Mx/hippo/commit/ea1578ab3c9f1a1509efbd2fab8b699e42c807ee))
- Split Hippo into app and core workspaces ([0a751be](https://github.com/Forja-Labs-Mx/hippo/commit/0a751be935d4d78500022316272b7d96dd4e6419))
- Add repository context ([7e10ef3](https://github.com/Forja-Labs-Mx/hippo/commit/7e10ef386e5ddc6d6d4d91cd8ba83fd8c0dcd075))
- Add hippo skills and AGENTS reference ([9cb2d69](https://github.com/Forja-Labs-Mx/hippo/commit/9cb2d69b68fb9e9e4dd0a81bc6cf6d8d86f9aa91))
- Address memory list review comments ([1b00018](https://github.com/Forja-Labs-Mx/hippo/commit/1b00018d835f2a33d10a03b3cd79d0ecb552d077))
- Prevent silent audit rollback data loss ([7c7103c](https://github.com/Forja-Labs-Mx/hippo/commit/7c7103c9a38394c1d8a5c770da6f0a6208c5a96d))
- Add frontend design skill ([9061dab](https://github.com/Forja-Labs-Mx/hippo/commit/9061daba9f1901276ddf6850be04cc64e1819e09))
- Migrate workflows to Blacksmith ([ed118cf](https://github.com/Forja-Labs-Mx/hippo/commit/ed118cf9008a1142b9c5efaafacc59d73e22c6c5))


### Refactoring

- Refactor audit and memory repos ([#18](https://github.com/Forja-Labs-Mx/hippo/issues/18)) ([b34de69](https://github.com/Forja-Labs-Mx/hippo/commit/b34de69d926c4b7e5c51ae76ce51f09ea3131284))
- Unify rerank score and drop dead bounds param ([b0beefc](https://github.com/Forja-Labs-Mx/hippo/commit/b0beefc3458b7cd3beb24714440f3f668bdbb9e8))
- Simplify hybrid search service ([3efeabc](https://github.com/Forja-Labs-Mx/hippo/commit/3efeabcc6f670d6fa851f6d1a0436802fced82a3))
- Move sqlite repo queries to sqlc ([e6c97d5](https://github.com/Forja-Labs-Mx/hippo/commit/e6c97d5a3e4abccb2ad4bd0cb3e30efea847a7fa))
- Reuse cosine helper and trim redundant code ([ea33a99](https://github.com/Forja-Labs-Mx/hippo/commit/ea33a9976d7d1d925222a9789482fc24f4cc576d))
- Simplify HIP-24 hardening helpers ([8fad335](https://github.com/Forja-Labs-Mx/hippo/commit/8fad335303bd2abcbaafdd2548aaeb03dcfd8744))
- Streamline dream review memory lookup ([0f52fd9](https://github.com/Forja-Labs-Mx/hippo/commit/0f52fd98acaa2462dda774792baaee2211e2d3d6))
- Drop redundant sorts and inline helper ([40c626f](https://github.com/Forja-Labs-Mx/hippo/commit/40c626f5d7cf2c763d5e41cf3d59b46e7f47c922))


### Tests

- Harden project and setup assertions ([40aeec9](https://github.com/Forja-Labs-Mx/hippo/commit/40aeec9f958118f587bf6aa931b781fa3ae2cc9b))
- Add HIP-24 security hardening coverage ([6f07af8](https://github.com/Forja-Labs-Mx/hippo/commit/6f07af8b23ca48ba17acfe08979293950ec32b7a))
- Add integration test infrastructure ([2ea95fe](https://github.com/Forja-Labs-Mx/hippo/commit/2ea95fe15614e63b4e1742e63d7c52e846f71540))
- Tighten helper failure paths ([4b2776c](https://github.com/Forja-Labs-Mx/hippo/commit/4b2776cd3e307b0eb3aef9ad06b5d0a76397ff84))
- Require complete Hippo agent markers ([df94296](https://github.com/Forja-Labs-Mx/hippo/commit/df94296407b35060a137503873a795bbf5df2909))
- Add grouped visibility regression matrix ([76686b8](https://github.com/Forja-Labs-Mx/hippo/commit/76686b88655cfec46518f08ce281ba6ab106a037))
- Tighten ui help assertion ([90b6d67](https://github.com/Forja-Labs-Mx/hippo/commit/90b6d6759c89581629b91d59b567460c78ad3b61))
- Force TTY for no-tui setup coverage ([4a781d2](https://github.com/Forja-Labs-Mx/hippo/commit/4a781d284a25edf6e5a57339bec91c6ed5fa2571))
- Assert setup TUI skips installer path ([ab03ace](https://github.com/Forja-Labs-Mx/hippo/commit/ab03acea9259a988334c43174f9b852165ddc270))
- Require uncommented setup provider config ([1d3000d](https://github.com/Forja-Labs-Mx/hippo/commit/1d3000d869ce8ef8a6f1a948097cc4f96aa6dc6b))
- Assert staged group save callback ([aacbd9f](https://github.com/Forja-Labs-Mx/hippo/commit/aacbd9f9eb1529ed2b22b33ac209beb82f33a130))
