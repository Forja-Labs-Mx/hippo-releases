# Changelog

All notable changes to Hippo are documented in this file.

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


### Fixes

- Allow git-cliff to read PR metadata ([cb81b0a](https://github.com/Forja-Labs-Mx/hippo/commit/cb81b0a47086a7af8d14998171bdabc44b43e53a))
- Make TUI collect credentials safely ([db38717](https://github.com/Forja-Labs-Mx/hippo/commit/db387176f391a16c752f674bb35799ed42def4dc))

## [v0.1.0-alpha.1] - 2026-05-13


### CI

- Add govulncheck ([956c504](https://github.com/Forja-Labs-Mx/hippo/commit/956c504f8c0e5f10ea930ccb7dad44a8e3a6f220))
- Serialize parallel golangci-lint runners ([e0682d5](https://github.com/Forja-Labs-Mx/hippo/commit/e0682d5513a9c31a60588336b37226eefee8faaa))
- Add mac and linux release pipeline ([21d940b](https://github.com/Forja-Labs-Mx/hippo/commit/21d940b19ac90048cc3f992591e28122d6490818))
- Publish from merged release PRs ([8681c55](https://github.com/Forja-Labs-Mx/hippo/commit/8681c55a70504061727a2281599cd4fbaede3331))
- Restrict manual publishing to main ([bcf07ab](https://github.com/Forja-Labs-Mx/hippo/commit/bcf07ab4be253b7672c155cfaa6a800644814f77))
- Harden release workflow ([d81ca77](https://github.com/Forja-Labs-Mx/hippo/commit/d81ca77e102979113f6782222d283b5ec7c86ba4))


### Chores

- Upgrade go to 1.26 ([#12](https://github.com/Forja-Labs-Mx/hippo/issues/12)) ([6bafe81](https://github.com/Forja-Labs-Mx/hippo/commit/6bafe81466dde37efe3add0389980ce354074b60))
- Replace tdd skill ([7cbb8c8](https://github.com/Forja-Labs-Mx/hippo/commit/7cbb8c87c44f5da0e5b37db2c48a987dadab8acd))
- Restore tdd anti-patterns reference ([2bec771](https://github.com/Forja-Labs-Mx/hippo/commit/2bec7711021ae3d2e05e87df9f21f96ba872aed1))
- Add diagnosis and docs grilling skills ([9e5f378](https://github.com/Forja-Labs-Mx/hippo/commit/9e5f378201b9ce22e6ade0d62baef3e1cff7bfe5))
- Update hippo skills ([427a723](https://github.com/Forja-Labs-Mx/hippo/commit/427a723a8ed01062811b91efaa1af3e4b44ab138))


### Documentation

- Clarify project identity fallback ([17cd4e1](https://github.com/Forja-Labs-Mx/hippo/commit/17cd4e165efdb1add964e3af91caf024b77f4823))
- Mark Alpha milestone as shipped ([5742e56](https://github.com/Forja-Labs-Mx/hippo/commit/5742e5653974d29457a8976182cb1268cc4d552b))
- Replace MCP tool wildcards with shipped names ([10b9b07](https://github.com/Forja-Labs-Mx/hippo/commit/10b9b07044435aa829687fb19010cc57c434d681))
- Add language hints to layout fences ([15e30c6](https://github.com/Forja-Labs-Mx/hippo/commit/15e30c65cf70195b0e4c20793fad3d4fe16c7bca))
- Capture post-Alpha enhancements in README, roadmap, and ADRs ([ef8af0b](https://github.com/Forja-Labs-Mx/hippo/commit/ef8af0b15b7f405aeae2c8ba343ecf202c9537f4))
- Land Beta plan + ADRs 0037–0042; promote ADR-0027 ([e612aba](https://github.com/Forja-Labs-Mx/hippo/commit/e612aba0b4697d38b0c40df4abbf35e14c704674))
- Address CodeRabbit review on PR #64 ([c0afb67](https://github.com/Forja-Labs-Mx/hippo/commit/c0afb67ccb9d9c2b21440dd6eaa29248e2050780))
- Clarify widget lifecycle contract ([7530f61](https://github.com/Forja-Labs-Mx/hippo/commit/7530f61c3f1bdc04641b62d593a0f78421fc9c75))
- Clarify timestamp model boundary ([05a3b12](https://github.com/Forja-Labs-Mx/hippo/commit/05a3b12b5b0de7d9836cc939bae559fe2c6f82d3))
- Define work episode boundary ([118db82](https://github.com/Forja-Labs-Mx/hippo/commit/118db82481c38e76d993fe853b0afc505e59ad3f))
- Clarify closed-session rejection ([4652710](https://github.com/Forja-Labs-Mx/hippo/commit/4652710ba1112d19cc94083313a7b5c69264bcbb))
- Align SKILL.md session-summary rule with reference ([fc23858](https://github.com/Forja-Labs-Mx/hippo/commit/fc2385859bac365c2e6d2f47a08017068935c9d1))


### Features

- Scaffold Hippo CLI foundation ([#7](https://github.com/Forja-Labs-Mx/hippo/issues/7)) ([f784981](https://github.com/Forja-Labs-Mx/hippo/commit/f784981946698a00651e4950b80695628b095ead))
- Add foundation primitives ([#8](https://github.com/Forja-Labs-Mx/hippo/issues/8)) ([cabf620](https://github.com/Forja-Labs-Mx/hippo/commit/cabf62071715738ba8e4e6f41895489e347c4ffe))
- Add identity domain models ([#9](https://github.com/Forja-Labs-Mx/hippo/issues/9)) ([9846f57](https://github.com/Forja-Labs-Mx/hippo/commit/9846f572440ece7e2f15808329a0a1dd6929665d))
- Add in-memory project service ([#10](https://github.com/Forja-Labs-Mx/hippo/issues/10)) ([71bed9b](https://github.com/Forja-Labs-Mx/hippo/commit/71bed9b3a7b26f38596400ec26a4362c5a077a78))
- Add go-guidelines skill and install skill-creator ([#13](https://github.com/Forja-Labs-Mx/hippo/issues/13)) ([3f104a1](https://github.com/Forja-Labs-Mx/hippo/commit/3f104a1f7a1361d1ac868a3463a9cc218809969e))
- Add slice 4 domain models ([#14](https://github.com/Forja-Labs-Mx/hippo/issues/14)) ([4407aff](https://github.com/Forja-Labs-Mx/hippo/commit/4407affc84d1d5c29d05f0698cbd9b7f390c7efe))
- Add in-memory CRUD service ([#15](https://github.com/Forja-Labs-Mx/hippo/issues/15)) ([d873ef0](https://github.com/Forja-Labs-Mx/hippo/commit/d873ef0f297c282a39063f3fb0753626a38c7090))
- Add in-memory preference service ([#16](https://github.com/Forja-Labs-Mx/hippo/issues/16)) ([ac27004](https://github.com/Forja-Labs-Mx/hippo/commit/ac2700423e1709a9c53a3b28ad024d8a3cd7a03a))
- Add SQLite migration foundation ([#17](https://github.com/Forja-Labs-Mx/hippo/issues/17)) ([fb6adff](https://github.com/Forja-Labs-Mx/hippo/commit/fb6adff16d6f84806bffb90d49135344a70cc184))
- Add sqlite repo adapters ([#19](https://github.com/Forja-Labs-Mx/hippo/issues/19)) ([a8d9de0](https://github.com/Forja-Labs-Mx/hippo/commit/a8d9de006cdee443db030e9b09a8b38a2d503eaf))
- Add FTS keyword search repo ([#20](https://github.com/Forja-Labs-Mx/hippo/issues/20)) ([3299c41](https://github.com/Forja-Labs-Mx/hippo/commit/3299c41b8766b21a45710f2b6bd55b951adbaf30))
- Add OpenAI-compatible embedder ([#21](https://github.com/Forja-Labs-Mx/hippo/issues/21)) ([1327b0e](https://github.com/Forja-Labs-Mx/hippo/commit/1327b0e4bdf3f01b5c22fbb28faca6625c6ff432))
- Add hybrid cosine reranking ([cbb72c8](https://github.com/Forja-Labs-Mx/hippo/commit/cbb72c8f42c2bb678ee8afe10f6a025b1fc79a07))
- Add setup and project init commands ([feca6b2](https://github.com/Forja-Labs-Mx/hippo/commit/feca6b24af512ce1a7843620d20ce0beb0ccd376))
- Add retrieval and audit tools ([f9e47f5](https://github.com/Forja-Labs-Mx/hippo/commit/f9e47f540c36495962da5b94733dbbab9fca1fe1))
- Add deterministic maintenance phases ([143a50f](https://github.com/Forja-Labs-Mx/hippo/commit/143a50f502024c4c8ebbcd799d0f05b177d1d4de))
- Add LLM phases and judge workflow ([21cfd64](https://github.com/Forja-Labs-Mx/hippo/commit/21cfd6463bd72d5863ceba5b2e4a00dd3fbb51aa))
- Add scheduler installers ([65aaebb](https://github.com/Forja-Labs-Mx/hippo/commit/65aaebb0f8992d5c303311bacdce116bd3c2fd03))
- Add --dry-run preview mode to dream run ([208e3d1](https://github.com/Forja-Labs-Mx/hippo/commit/208e3d1e97fa2f9f3a66263fa6788df835a710bb))
- Wire production services ([06614b6](https://github.com/Forja-Labs-Mx/hippo/commit/06614b619fcbad550e8896c92a900f0c9fe88aa1))
- Audit project and preference mutations ([408d94c](https://github.com/Forja-Labs-Mx/hippo/commit/408d94c0a7fe57b669820c59e174a24bc58a5c8f))
- Add dream review promotion surfaces ([81b5d59](https://github.com/Forja-Labs-Mx/hippo/commit/81b5d5929f3c2701e059eaa490ae7da8d4881f6a))
- Add ambient Hippo agent memory guidance ([6c0c1b2](https://github.com/Forja-Labs-Mx/hippo/commit/6c0c1b27632a9bf37f252cf0b327707ff994e984))
- Score promotions with reinforcement ([ce63300](https://github.com/Forja-Labs-Mx/hippo/commit/ce63300a80c1a0f58f90926591eeb6e8259a97e4))
- Add project groups service API ([e487f6f](https://github.com/Forja-Labs-Mx/hippo/commit/e487f6fbc4b5806dafb0eb028fc16a891203e457))
- Allow grouped project read visibility ([2df10c2](https://github.com/Forja-Labs-Mx/hippo/commit/2df10c2bf6686342a919133a3c330f64b1c6cc1b))
- Score promotions with project group context ([59f5976](https://github.com/Forja-Labs-Mx/hippo/commit/59f5976179047bc53a4f7cf37223c028807f8695))
- Add group CLI and MCP tools ([13927eb](https://github.com/Forja-Labs-Mx/hippo/commit/13927eb79f7f98bc92aeac94d7ae10794841a5b5))
- Guide users through provider, MCP agent, and Dream install ([d8088de](https://github.com/Forja-Labs-Mx/hippo/commit/d8088def6827c40fb86539def1618ceb919970dd))
- Add project listing and search filters ([4b78b2d](https://github.com/Forja-Labs-Mx/hippo/commit/4b78b2d11f44943604f20756e2b7ee1280f2e132))
- Scaffold widgets package with text + step primitives (HIP-44) ([dc02689](https://github.com/Forja-Labs-Mx/hippo/commit/dc02689ffef860f04f39a7d96e9da3a0b5c2f396))
- Add filtered list and unarchive ([1581054](https://github.com/Forja-Labs-Mx/hippo/commit/158105444c994764763419ffdc5ea157d8312d45))
- Add beta sessions migration ([ce750ce](https://github.com/Forja-Labs-Mx/hippo/commit/ce750ceceae7c346663579343fe9d6e4d952b78f))
- Add open closed lifecycle model ([d99e5ab](https://github.com/Forja-Labs-Mx/hippo/commit/d99e5ab75bf35d44e78ba2e377813d4bd1b51740))
- Add selection modal chip widgets ([941c305](https://github.com/Forja-Labs-Mx/hippo/commit/941c30540a422480c8888217a6128604a7586923))
- List pending review suggestions ([d82715c](https://github.com/Forja-Labs-Mx/hippo/commit/d82715c83b2849d85fc19eae7d9b9066d61d8dec))
- Add debug shell command ([96d2c9d](https://github.com/Forja-Labs-Mx/hippo/commit/96d2c9dbdc3f6ecd81fa8e583090a5cfca19a950))
- Add init TUI shell ([fb98948](https://github.com/Forja-Labs-Mx/hippo/commit/fb989488abb0d0f8ed14b3d925df572a57cf56ff))
- Add setup TUI wrapper ([41df10c](https://github.com/Forja-Labs-Mx/hippo/commit/41df10ce79f3bd643631e7b8dbf62e528916895b))
- Rewrite hippo-memory skill to teach a model, not a checklist ([ca2dfff](https://github.com/Forja-Labs-Mx/hippo/commit/ca2dfffa22e84f6f58bbd29a3b29ca0e25cc54db))
- Add memories master-detail list ([79d2e06](https://github.com/Forja-Labs-Mx/hippo/commit/79d2e0639dc2f96f6597b38f032dd01f4e898b35))
- Add project init wizard ([92175f3](https://github.com/Forja-Labs-Mx/hippo/commit/92175f3c0ba27007d5bac0d5a76321c6e8008d8a))
- Add setup TUI wizard ([4555ea8](https://github.com/Forja-Labs-Mx/hippo/commit/4555ea843b589cb258615cd4f60b42ced364c699))


### Fixes

- Address project init review feedback ([7e8d5a7](https://github.com/Forja-Labs-Mx/hippo/commit/7e8d5a7c8836562aac882f7d83f3f549f6653e4a))
- Validate retrieval tool inputs ([77c201f](https://github.com/Forja-Labs-Mx/hippo/commit/77c201f6dd3165a9dd4c0346d161b1adc235edb9))
- Validate run flag bounds ([85ca9a2](https://github.com/Forja-Labs-Mx/hippo/commit/85ca9a2487bd779b9ecd728ffa787fcfa4bf68b0))
- Stabilize promotion idempotency key ([6e433f1](https://github.com/Forja-Labs-Mx/hippo/commit/6e433f1b9fd41a8f938302991f4d77a53f7301ca))
- Address HIP-24 review hardening comments ([bf1930f](https://github.com/Forja-Labs-Mx/hippo/commit/bf1930f009c5d6cfd0a5e292e19db6f956f3554d))
- Fix embedding rebuild database path ([5d1ff50](https://github.com/Forja-Labs-Mx/hippo/commit/5d1ff50aa63abda9dd7143acdc82e5efd0a77e16))
- Align CLI project identity resolution ([86b4c05](https://github.com/Forja-Labs-Mx/hippo/commit/86b4c053c81e19e1a19cbc542a2fca1786ab8eca))
- Address project identity review feedback ([1e743f9](https://github.com/Forja-Labs-Mx/hippo/commit/1e743f9cf22665637cb20bb406e61f012f41be4e))
- Propagate git remote resolution errors ([936af58](https://github.com/Forja-Labs-Mx/hippo/commit/936af582ecbacb8d873f23bca8870fe288ac96e2))
- Enforce access scope in raw SQL queries ([d720822](https://github.com/Forja-Labs-Mx/hippo/commit/d720822046a0b1ca32d6d1a5489daffce4dcc9ab))
- Report scoped memory update misses ([c12c8e7](https://github.com/Forja-Labs-Mx/hippo/commit/c12c8e7d6ea7bc7cda1736561636725bfe2a77c3))
- Wake embedding ticker after commit ([26230f2](https://github.com/Forja-Labs-Mx/hippo/commit/26230f26ef745abe0f0f0433ba24b81d17141702))
- Register hippo judge in production ([9c06142](https://github.com/Forja-Labs-Mx/hippo/commit/9c0614226cac3a025ef9d537e094f91e50b9b65d))
- Pass audit service in integration wiring ([8fd1d25](https://github.com/Forja-Labs-Mx/hippo/commit/8fd1d25c3083485d57812f61fdb1ee04b5b2eb00))
- Avoid unredacted JSON fallback ([d4ad979](https://github.com/Forja-Labs-Mx/hippo/commit/d4ad979e2f7aacad344576a187432ec6cbfbcd46))
- Return relations from memory get ([a56cbff](https://github.com/Forja-Labs-Mx/hippo/commit/a56cbff6f5e34631c0cb7946c8039cd44ebed561))
- Validate dream review promotion inputs ([3db689b](https://github.com/Forja-Labs-Mx/hippo/commit/3db689b22b24b700654522cf71f437e87b189691))
- Harden dream review service guards ([9098de4](https://github.com/Forja-Labs-Mx/hippo/commit/9098de4404e2037f4d1a9ebcd61f3cb45afba541))
- Default to setup database ([b2e1e07](https://github.com/Forja-Labs-Mx/hippo/commit/b2e1e079df8894f07c18b3421e0093e781f22d95))
- Recover malformed Hippo agent blocks ([3779d77](https://github.com/Forja-Labs-Mx/hippo/commit/3779d772ee04da5b3d753875dbfa4cf7b31a9418))
- Dedupe promotion suggestions ([2337a4f](https://github.com/Forja-Labs-Mx/hippo/commit/2337a4f4ce3622514d9ea6e519add5dfb5276b48))
- Address group review feedback ([70bb6d2](https://github.com/Forja-Labs-Mx/hippo/commit/70bb6d2c0abae77afddc81fad774905da430664b))
- Reject invalid --agent values before running setup ([670273e](https://github.com/Forja-Labs-Mx/hippo/commit/670273e95e8be3f3a489ca9beb8d9fe551c70a6c))
- Scope project listing ([cb9144c](https://github.com/Forja-Labs-Mx/hippo/commit/cb9144c38b3353ee0bf9b7d3b0394392dff1a0f6))
- Include group-readable projects ([240b33a](https://github.com/Forja-Labs-Mx/hippo/commit/240b33a4b4afcd8ef7f9f7e27e754346dbd68d04))
- Sequence sessions migration after tui audit ([b58ecf4](https://github.com/Forja-Labs-Mx/hippo/commit/b58ecf4fe0f47a751826fa8abf3f1ef0408ab749))
- Page review suggestions in sqlite ([54aca06](https://github.com/Forja-Labs-Mx/hippo/commit/54aca06b01cde4478ff68ee0df4c92b88f5403ca))
- Report setup TUI config load errors ([8b0a2af](https://github.com/Forja-Labs-Mx/hippo/commit/8b0a2afe5e543f14d9e7d1441410aa3bed46f1bc))
- Address HIP-49 review feedback ([95e1b2b](https://github.com/Forja-Labs-Mx/hippo/commit/95e1b2b373167d1049478233d64a561378f19424))
- Fallback for broad keyword queries ([29cb7b1](https://github.com/Forja-Labs-Mx/hippo/commit/29cb7b15dc0ab4a7f9c9bd4e663778b46aff8d87))


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
slices. ([797ebe5](https://github.com/Forja-Labs-Mx/hippo/commit/797ebe5a996780cd9d263aa408238f07f0d8df37))
- Document canonical alpha schema ([#2](https://github.com/Forja-Labs-Mx/hippo/issues/2)) ([9e6a6eb](https://github.com/Forja-Labs-Mx/hippo/commit/9e6a6eb106e29cba55d566c9d467840d02f88025))
- [codex] Move Hippo to Bun/Turborepo monorepo ([#3](https://github.com/Forja-Labs-Mx/hippo/issues/3))

* Move Hippo app into apps workspace

* Configure Bun Turborepo monorepo

* Add turborepo agent skill ([9e6abab](https://github.com/Forja-Labs-Mx/hippo/commit/9e6abab533151819bc650917fe9844b813059241))
- Add PR creation workflow ([#4](https://github.com/Forja-Labs-Mx/hippo/issues/4)) ([a90daa7](https://github.com/Forja-Labs-Mx/hippo/commit/a90daa706474b1d87db0c0cfd997a34308a1d125))
- Configure go quality tasks ([#5](https://github.com/Forja-Labs-Mx/hippo/issues/5)) ([98ba8a2](https://github.com/Forja-Labs-Mx/hippo/commit/98ba8a2cf01fae155744c392f2d21e5100950673))
- Configure lefthook checks ([#6](https://github.com/Forja-Labs-Mx/hippo/issues/6)) ([a77c19b](https://github.com/Forja-Labs-Mx/hippo/commit/a77c19b331a46456044f7b9b26ad0f83ba02555f))
- Add Turbo-backed GitHub Actions CI ([#11](https://github.com/Forja-Labs-Mx/hippo/issues/11))

* Add Turbo-backed GitHub Actions CI

* Harden Turbo CI cache checks ([1799321](https://github.com/Forja-Labs-Mx/hippo/commit/1799321adbe415f91a396e5d033b6884d0396cdf))
- Implement embedding job queue ([#22](https://github.com/Forja-Labs-Mx/hippo/issues/22))

* Implement embedding job queue

* Address embedding queue review feedback ([c68af3b](https://github.com/Forja-Labs-Mx/hippo/commit/c68af3b8839d0b49b0627bea3cbbbb5c1960ca29))
- Add memory search and ask CLI commands ([1ca5832](https://github.com/Forja-Labs-Mx/hippo/commit/1ca5832505151c5d2b51e3d483e7f559fe4e533e))
- Add MCP memory tools ([696c095](https://github.com/Forja-Labs-Mx/hippo/commit/696c095540fefcfde6f3630d9c0f6843f6399300))
- Address MCP review feedback ([e2fa261](https://github.com/Forja-Labs-Mx/hippo/commit/e2fa2611ed491c26e9b344175115d41a15721ca0))
- Add LLM-backed memory structuring

- Introduce OpenAI and Anthropic text providers
- Auto-structure raw memory input through the MCP tool
- Add structured memory path and tests ([eb97bc1](https://github.com/Forja-Labs-Mx/hippo/commit/eb97bc1bf07fb6b350fb5ddbcb1392d0a9266f56))
- Tighten memory structuring validation

- Require complete structured fields before skipping LLM structuring
- Reject structured output missing category, body, or metadata
- Add tests for partial raw input and missing required fields ([1d9327d](https://github.com/Forja-Labs-Mx/hippo/commit/1d9327d3c5408e8d7ab541feb65084320ad38c06))
- Migrate workflows to Blacksmith ([24e3528](https://github.com/Forja-Labs-Mx/hippo/commit/24e3528837850ee0f22397a77dd01c6b7b912109))
- Wire text provider config into runtime ([a1734b3](https://github.com/Forja-Labs-Mx/hippo/commit/a1734b34585c472351a919cff883bd21df6f497f))
- Address text provider config review feedback ([6cc0d50](https://github.com/Forja-Labs-Mx/hippo/commit/6cc0d505b410c38ae35b344402fb4d8ca77fe858))
- Add agent promotion suggestion flow ([bc049bd](https://github.com/Forja-Labs-Mx/hippo/commit/bc049bdff9e8431570d5c98ce43159a28c0f2f1a))
- Split Hippo into app and core workspaces ([9467fd9](https://github.com/Forja-Labs-Mx/hippo/commit/9467fd925e50c258b082810e56b080d47522c87d))
- Add repository context ([90273e8](https://github.com/Forja-Labs-Mx/hippo/commit/90273e8b68912bb93cfe10bbd802a969c5ce078c))
- Add hippo skills and AGENTS reference ([2a80b73](https://github.com/Forja-Labs-Mx/hippo/commit/2a80b736861cdcb5c354ed6eaef3b1dc2a0fda21))
- Address memory list review comments ([6a6e212](https://github.com/Forja-Labs-Mx/hippo/commit/6a6e2126c832d55c44c7cad70dd6ed5fb6c8e560))
- Prevent silent audit rollback data loss ([399568f](https://github.com/Forja-Labs-Mx/hippo/commit/399568f3ce2bfb6abb09a4f2f065019daa08a518))
- Add frontend design skill ([524410e](https://github.com/Forja-Labs-Mx/hippo/commit/524410eced9832795e0ba0b2f0dbdc9b0c666199))


### Refactoring

- Refactor audit and memory repos ([#18](https://github.com/Forja-Labs-Mx/hippo/issues/18)) ([249e2e1](https://github.com/Forja-Labs-Mx/hippo/commit/249e2e19eb432a44797f2d2d6cd6d1399cfa98c2))
- Unify rerank score and drop dead bounds param ([aa31d4f](https://github.com/Forja-Labs-Mx/hippo/commit/aa31d4f3ebac793ce06857238f4a3d08de00962c))
- Simplify hybrid search service ([9b7707b](https://github.com/Forja-Labs-Mx/hippo/commit/9b7707bd52d5b347b44061d2ba3f28182664e465))
- Move sqlite repo queries to sqlc ([2933fe1](https://github.com/Forja-Labs-Mx/hippo/commit/2933fe1fb98e2f3f813748ff39151bd098656649))
- Reuse cosine helper and trim redundant code ([4068cbe](https://github.com/Forja-Labs-Mx/hippo/commit/4068cbe707014d332d4091aeeed51e54092e2c2f))
- Simplify HIP-24 hardening helpers ([5eb05e6](https://github.com/Forja-Labs-Mx/hippo/commit/5eb05e6acda234ce92a05ec0c98246b0e62374fc))
- Streamline dream review memory lookup ([5a6972c](https://github.com/Forja-Labs-Mx/hippo/commit/5a6972c974f432c803f729ad70cc74b1a7c56ad0))
- Drop redundant sorts and inline helper ([6c5dc30](https://github.com/Forja-Labs-Mx/hippo/commit/6c5dc3038bb0c7fccade96a4b6f70b47e0e65fab))


### Tests

- Harden project and setup assertions ([35a12b2](https://github.com/Forja-Labs-Mx/hippo/commit/35a12b26eb2cd3a794c0b58ed75a817922cc7016))
- Add HIP-24 security hardening coverage ([f0506c6](https://github.com/Forja-Labs-Mx/hippo/commit/f0506c69d05bc4700483200604b1a0704547558d))
- Add integration test infrastructure ([7108da0](https://github.com/Forja-Labs-Mx/hippo/commit/7108da06b25e3c794b960c2e33b16c40ebf87f35))
- Tighten helper failure paths ([cac8d33](https://github.com/Forja-Labs-Mx/hippo/commit/cac8d335844725d6b4d85556b8290dcf954c8e1b))
- Require complete Hippo agent markers ([387e4b6](https://github.com/Forja-Labs-Mx/hippo/commit/387e4b6cb875609b975afb78e10dee97e36bc687))
- Add grouped visibility regression matrix ([e096b06](https://github.com/Forja-Labs-Mx/hippo/commit/e096b06ae4911c72802553767e26bcd363a0e8a3))
- Tighten ui help assertion ([a4c99ca](https://github.com/Forja-Labs-Mx/hippo/commit/a4c99cacca4729fd8cd1dee7ab62e9cc97997c88))
- Force TTY for no-tui setup coverage ([4ac8610](https://github.com/Forja-Labs-Mx/hippo/commit/4ac86107dcec2b371ce98f26c1cd7038a4062835))
- Assert setup TUI skips installer path ([0134316](https://github.com/Forja-Labs-Mx/hippo/commit/0134316dfba677ce6ff9478357675c7f11ecd9a1))
- Require uncommented setup provider config ([a858d74](https://github.com/Forja-Labs-Mx/hippo/commit/a858d746c7f01c19e93147ac419f9fee760a4d25))
- Assert staged group save callback ([fc73264](https://github.com/Forja-Labs-Mx/hippo/commit/fc73264061a150b64e58ec9e737c4eff90db2ef9))
