# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.5.0](https://github.com/dot-asm/cc-rs/compare/cc-v1.4.5...cc-v1.5.0) - 2026-09-25

### Added

- support trim paths with clang-cl.exe ([#1799](https://github.com/dot-asm/cc-rs/pull/1799))
- inherit path remap rules from cargo trim-paths ([#1794](https://github.com/dot-asm/cc-rs/pull/1794))
- add i686-pc-windows-gnullvm prefix detection ([#1283](https://github.com/dot-asm/cc-rs/pull/1283))
- add cargo_output to eliminate last vestiges of stdout pollution ([#1141](https://github.com/dot-asm/cc-rs/pull/1141))
- Query rustc for clang target triples instead of hardcoding them ([#1004](https://github.com/dot-asm/cc-rs/pull/1004))
- move debug logging behind an environment variable ([#972](https://github.com/dot-asm/cc-rs/pull/972))
- Simplify code by using `String::split_ascii_whitespace` ([#558](https://github.com/dot-asm/cc-rs/pull/558))

### Fixed

- Prevent check_exe from dropping flags on the floor. ([#1884](https://github.com/dot-asm/cc-rs/pull/1884))
- update fd handling to use BorrowedFd ([#1882](https://github.com/dot-asm/cc-rs/pull/1882))
- probe flag support without OUT_DIR via tempfile ([#1875](https://github.com/dot-asm/cc-rs/pull/1875))
- run the Android llvm-ar probe in the caller's environment ([#1868](https://github.com/dot-asm/cc-rs/pull/1868))
- honor Build::env overrides in flag support probes ([#1866](https://github.com/dot-asm/cc-rs/pull/1866))
- Infer NEON, not VFPv4, from `neon` in the target name ([#1843](https://github.com/dot-asm/cc-rs/pull/1843))
- fix typo teats -> tests ([#1824](https://github.com/dot-asm/cc-rs/pull/1824))
- fix `-Cforce-frame-pointers`'s corresponding `CFLAGS` ([#1814](https://github.com/dot-asm/cc-rs/pull/1814))
- *(ar)* suppress warnings from `D` modifier probe ([#1700](https://github.com/dot-asm/cc-rs/pull/1700))
- *(ar)* deterministic archives with `D` modifier ([#1697](https://github.com/dot-asm/cc-rs/pull/1697))
- *(#172)* prevent OUT_DIR escape for '..' file paths (#1631)
- fix building for aarch64-apple-visionos-sim on nightly ([#1534](https://github.com/dot-asm/cc-rs/pull/1534))
- fix tests apple_sdkroot_wrong ([#1530](https://github.com/dot-asm/cc-rs/pull/1530))
- add `-mcpu=mvp` and `-mmutable-globals` for `wasm32v1-none` ([#1524](https://github.com/dot-asm/cc-rs/pull/1524))
- fix new clippy lint introduced in rust 1.89.0 ([#1509](https://github.com/dot-asm/cc-rs/pull/1509))
- force windows compiler to run in `out_dir` to prevent artifacts in cwd ([#1415](https://github.com/dot-asm/cc-rs/pull/1415))
- fix finding toolchains when invoked by msbuild ([#1201](https://github.com/dot-asm/cc-rs/pull/1201))
- emscripten build on windows ([#1054](https://github.com/dot-asm/cc-rs/pull/1054))
- fix xcrun sdk version arg ([#1007](https://github.com/dot-asm/cc-rs/pull/1007))
- *(env_tool)* return None if env is empty ([#1021](https://github.com/dot-asm/cc-rs/pull/1021))
- fix llvm-ar as archiver for msvc targets; fix clang-cl detection; fix assembler output flag detection; add clang/clang-cl windows CI ([#1015](https://github.com/dot-asm/cc-rs/pull/1015))
- only print out debug info if `cargo_warnings` is true ([#960](https://github.com/dot-asm/cc-rs/pull/960))
- fix broken intradoc links ([#922](https://github.com/dot-asm/cc-rs/pull/922))
- Add apple tvos support ([#881](https://github.com/dot-asm/cc-rs/pull/881))
- *(flag_check)* never link to avoid false positives ([#839](https://github.com/dot-asm/cc-rs/pull/839))
- fix msbuild from vs2022 not being found
- find_msvc_environment argument order ([#628](https://github.com/dot-asm/cc-rs/pull/628))
- fix some typos ([#604](https://github.com/dot-asm/cc-rs/pull/604))
- fix find_tool and find_vs_version might returns incompatible values ([#488](https://github.com/dot-asm/cc-rs/pull/488))
- fix 2
- fix
- *(flag_check)* Send flag to MSVC telling it not to link
- fix arm-linux-androideabi-gcc -Oz error

### Other

- *(deps)* bump tombi-toml/setup-tombi from 1.2.5 to 1.5.0 ([#1885](https://github.com/dot-asm/cc-rs/pull/1885))
- *(deps)* bump taiki-e/install-action from 2.85.5 to 2.87.2 ([#1886](https://github.com/dot-asm/cc-rs/pull/1886))
- add toml formatting check ([#1879](https://github.com/dot-asm/cc-rs/pull/1879))
- release ([#1874](https://github.com/dot-asm/cc-rs/pull/1874))
- simplify conditional logic using `then` method ([#1860](https://github.com/dot-asm/cc-rs/pull/1860))
- *(cc)* release v1.4.4 ([#1869](https://github.com/dot-asm/cc-rs/pull/1869))
- *(deps)* bump dtolnay/rust-toolchain ([#1862](https://github.com/dot-asm/cc-rs/pull/1862))
- release ([#1858](https://github.com/dot-asm/cc-rs/pull/1858))
- add loongarch64 assembly shim ([#1855](https://github.com/dot-asm/cc-rs/pull/1855))
- *(deps)* bump Swatinem/rust-cache from 2.9.1 to 2.9.2 ([#1853](https://github.com/dot-asm/cc-rs/pull/1853))
- replace rustup installation with actions-rust-lang/setup-rust-toolchain ([#1852](https://github.com/dot-asm/cc-rs/pull/1852))
- use workspace inheritance ([#1850](https://github.com/dot-asm/cc-rs/pull/1850))
- convert to workspace lints ([#1849](https://github.com/dot-asm/cc-rs/pull/1849))
- Update MSRV to 1.65 ([#1834](https://github.com/dot-asm/cc-rs/pull/1834))
- Regenerate target info ([#1848](https://github.com/dot-asm/cc-rs/pull/1848))
- run clippy in more cases ([#1832](https://github.com/dot-asm/cc-rs/pull/1832))
- *(cc)* release v1.4.2 ([#1846](https://github.com/dot-asm/cc-rs/pull/1846))
- do not emit -mno-omit-leaf-frame-pointer if unsupported ([#1845](https://github.com/dot-asm/cc-rs/pull/1845))
- release ([#1841](https://github.com/dot-asm/cc-rs/pull/1841))
- Fix parsing of thumbv7a-vex-v5 ([#1840](https://github.com/dot-asm/cc-rs/pull/1840))
- Regenerate target info ([#1839](https://github.com/dot-asm/cc-rs/pull/1839))
- Read msrv from Cargo.toml ([#1837](https://github.com/dot-asm/cc-rs/pull/1837))
- add `aarch64_be` to `prefix_for_target` ([#1835](https://github.com/dot-asm/cc-rs/pull/1835))
- allow flaky failure of check-motor ([#1836](https://github.com/dot-asm/cc-rs/pull/1836))
- compile all test targets for cross builds ([#1833](https://github.com/dot-asm/cc-rs/pull/1833))
- run clippy on more targets ([#1831](https://github.com/dot-asm/cc-rs/pull/1831))
- fix for minimal-versions ([#1825](https://github.com/dot-asm/cc-rs/pull/1825))
- update Swatinem/rust-cache ([#1830](https://github.com/dot-asm/cc-rs/pull/1830))
- Use lp64d ABI for Managarm riscv64 ([#1829](https://github.com/dot-asm/cc-rs/pull/1829))
- update github actions ([#1826](https://github.com/dot-asm/cc-rs/pull/1826))
- Refactor max_by to max_by_key for clarity ([#1828](https://github.com/dot-asm/cc-rs/pull/1828))
- Make cc work on Motor OS ([#1822](https://github.com/dot-asm/cc-rs/pull/1822))
- fix needless_borrow lint ([#1827](https://github.com/dot-asm/cc-rs/pull/1827))
- fix compilation on Rust 1.64 ([#1823](https://github.com/dot-asm/cc-rs/pull/1823))
- Reformat Cargo.toml ([#1817](https://github.com/dot-asm/cc-rs/pull/1817))
- *(test)* stop assuming about target dir layout ([#1821](https://github.com/dot-asm/cc-rs/pull/1821))
- do not inherit rust-version for dev-tools ([#1815](https://github.com/dot-asm/cc-rs/pull/1815))
- add toml formatting rules ([#1816](https://github.com/dot-asm/cc-rs/pull/1816))
- *(cargo)* remove deprecated package authors field ([#1812](https://github.com/dot-asm/cc-rs/pull/1812))
- workspace inheritance for edition and rust-version ([#1813](https://github.com/dot-asm/cc-rs/pull/1813))
- update edition to 2021 ([#1811](https://github.com/dot-asm/cc-rs/pull/1811))
- Use constant for MSRV in mod read of gen-target-info ([#1810](https://github.com/dot-asm/cc-rs/pull/1810))
- update rust-version to 1.64 ([#1808](https://github.com/dot-asm/cc-rs/pull/1808))
- Bump actions/checkout from 7.0.0 to 7.0.1 ([#1802](https://github.com/dot-asm/cc-rs/pull/1802))
- *(cc)* release v1.4.0 ([#1803](https://github.com/dot-asm/cc-rs/pull/1803))
- Bump release-plz/action from 0.5.130 to 0.5.131 ([#1798](https://github.com/dot-asm/cc-rs/pull/1798))
- *(cc)* release v1.3.0 ([#1796](https://github.com/dot-asm/cc-rs/pull/1796))
- *(cc)* release v1.2.67 ([#1789](https://github.com/dot-asm/cc-rs/pull/1789))
- Bump taiki-e/install-action from 2.81.8 to 2.82.8 ([#1786](https://github.com/dot-asm/cc-rs/pull/1786))
- Fix clippy warning ([#1788](https://github.com/dot-asm/cc-rs/pull/1788))
- Regenerate target info ([#1785](https://github.com/dot-asm/cc-rs/pull/1785))
- Add missing todo for deprecated API
- Add support for `aarch64-unknown-linux-pauthtest` target ([#1713](https://github.com/dot-asm/cc-rs/pull/1713))
- Fix nightly compilation error ([#1783](https://github.com/dot-asm/cc-rs/pull/1783))
- *(cc)* release v1.2.66 ([#1777](https://github.com/dot-asm/cc-rs/pull/1777))
- Fix target parsing ([#1779](https://github.com/dot-asm/cc-rs/pull/1779))
- *(test-wasm)* do not download pre release of wasi-sdk ([#1778](https://github.com/dot-asm/cc-rs/pull/1778))
- Support new QNX targets ([#1775](https://github.com/dot-asm/cc-rs/pull/1775))
- Add kache to the supported compiler wrappers ([#1770](https://github.com/dot-asm/cc-rs/pull/1770))
- Bump actions/checkout from 6.0.3 to 7.0.0 ([#1767](https://github.com/dot-asm/cc-rs/pull/1767))
- *(cc)* release v1.2.65 ([#1764](https://github.com/dot-asm/cc-rs/pull/1764))
- Regenerate target info ([#1763](https://github.com/dot-asm/cc-rs/pull/1763))
- Bump taiki-e/install-action from 2.77.6 to 2.81.8 ([#1758](https://github.com/dot-asm/cc-rs/pull/1758))
- Bump release-plz/action from 0.5.129 to 0.5.130 ([#1759](https://github.com/dot-asm/cc-rs/pull/1759))
- *(cc)* release v1.2.64 ([#1757](https://github.com/dot-asm/cc-rs/pull/1757))
- Add more bare-metal 32-bit Arm support ([#1753](https://github.com/dot-asm/cc-rs/pull/1753))
- Bump actions/checkout from 6.0.2 to 6.0.3 ([#1751](https://github.com/dot-asm/cc-rs/pull/1751))
- Remove unnecessary clone ([#1748](https://github.com/dot-asm/cc-rs/pull/1748))
- Update rusqlite requirement from 0.39.0 to 0.40.0 ([#1744](https://github.com/dot-asm/cc-rs/pull/1744))
- Add default compiler prefixes for thumbv7a/thumbv7r/thumbv8r bare-metal targets ([#1742](https://github.com/dot-asm/cc-rs/pull/1742))
- *(cc)* release v1.2.63 ([#1740](https://github.com/dot-asm/cc-rs/pull/1740))
- Update shlex requirement from 1.3.0 to 2.0.1 ([#1736](https://github.com/dot-asm/cc-rs/pull/1736))
- Bump release-plz/action from 0.5.128 to 0.5.129 ([#1728](https://github.com/dot-asm/cc-rs/pull/1728))
- Bump taiki-e/install-action from 2.75.28 to 2.77.6 ([#1729](https://github.com/dot-asm/cc-rs/pull/1729))
- Bump taiki-e/install-action from 2.75.19 to 2.75.28 ([#1722](https://github.com/dot-asm/cc-rs/pull/1722))
- *(cc)* release v1.2.62 ([#1716](https://github.com/dot-asm/cc-rs/pull/1716))
- Regenerate target info ([#1721](https://github.com/dot-asm/cc-rs/pull/1721))
- Allow exceptions on wasm platforms ([#1714](https://github.com/dot-asm/cc-rs/pull/1714))
- Add relibc env ([#1710](https://github.com/dot-asm/cc-rs/pull/1710))
- recognize sh4 architecture in parse_arch() ([#1712](https://github.com/dot-asm/cc-rs/pull/1712))
- Bump taiki-e/install-action from 2.75.18 to 2.75.19 ([#1709](https://github.com/dot-asm/cc-rs/pull/1709))
- Bump taiki-e/install-action from 2.75.17 to 2.75.18 ([#1708](https://github.com/dot-asm/cc-rs/pull/1708))
- *(cc)* release v1.2.61 ([#1707](https://github.com/dot-asm/cc-rs/pull/1707))
- Bump taiki-e/install-action from 2.75.16 to 2.75.17 ([#1706](https://github.com/dot-asm/cc-rs/pull/1706))
- fix `OutputKind::Capture` documentation ([#1705](https://github.com/dot-asm/cc-rs/pull/1705))
- Bump taiki-e/install-action from 2.75.4 to 2.75.5 ([#1703](https://github.com/dot-asm/cc-rs/pull/1703))
- Hash-pin all actions, apply other suggestions from zizmor ([#1702](https://github.com/dot-asm/cc-rs/pull/1702))
- *(cc)* release v1.2.60 ([#1701](https://github.com/dot-asm/cc-rs/pull/1701))
- *(cc)* release v1.2.59 ([#1699](https://github.com/dot-asm/cc-rs/pull/1699))
- Regenerate target info ([#1698](https://github.com/dot-asm/cc-rs/pull/1698))
- Fix target abi parsing dor sanitiser targets ([#1695](https://github.com/dot-asm/cc-rs/pull/1695))
- *(cc)* release v1.2.58 ([#1694](https://github.com/dot-asm/cc-rs/pull/1694))
- Update Compile-time Requirements to add info about clang-cl.exe ([#1693](https://github.com/dot-asm/cc-rs/pull/1693))
- Update rusqlite requirement from 0.38.0 to 0.39.0 ([#1691](https://github.com/dot-asm/cc-rs/pull/1691))
- *(cc)* release v1.2.57 ([#1681](https://github.com/dot-asm/cc-rs/pull/1681))
- Size archiver batches according to argument length not argument count ([#1689](https://github.com/dot-asm/cc-rs/pull/1689))
- Improve the semantics of `Build::env` ([#1682](https://github.com/dot-asm/cc-rs/pull/1682))
- Use cargo-nextest in main.yml ([#1686](https://github.com/dot-asm/cc-rs/pull/1686))
- Update which requirement from ^4.0 to ^8.0 ([#1683](https://github.com/dot-asm/cc-rs/pull/1683))
- Serialize tests that need environment variables ([#1685](https://github.com/dot-asm/cc-rs/pull/1685))
- Rename job 'regenerate' to 'rustc_target_test' ([#1687](https://github.com/dot-asm/cc-rs/pull/1687))
- Don't run CI twice on every PR ([#1684](https://github.com/dot-asm/cc-rs/pull/1684))
- rename `__set_env` to `env` and make it un-hidden ([#1656](https://github.com/dot-asm/cc-rs/pull/1656))
- *(cc)* release v1.2.56 ([#1677](https://github.com/dot-asm/cc-rs/pull/1677))
- Regenerate target info ([#1676](https://github.com/dot-asm/cc-rs/pull/1676))
- Fix `clang-cl` target when cross-compiling ([#1670](https://github.com/dot-asm/cc-rs/pull/1670))
- release ([#1668](https://github.com/dot-asm/cc-rs/pull/1668))
- Regenerate target info ([#1667](https://github.com/dot-asm/cc-rs/pull/1667))
- Fix RUSTFLAGS typo in test-linker-plugin-lto ([#1665](https://github.com/dot-asm/cc-rs/pull/1665))
- Disable PIC for armv7-sony-vita-newlibeabihf ([#1664](https://github.com/dot-asm/cc-rs/pull/1664))
- Add `find_windows_sdk` API ([#1663](https://github.com/dot-asm/cc-rs/pull/1663))
- *(cc)* release v1.2.54 ([#1662](https://github.com/dot-asm/cc-rs/pull/1662))
- Fix x86_64-unknown-linux-gnuasan parsing ([#1661](https://github.com/dot-asm/cc-rs/pull/1661))
- Regenerate target info ([#1660](https://github.com/dot-asm/cc-rs/pull/1660))
- release ([#1658](https://github.com/dot-asm/cc-rs/pull/1658))
- Add missing RISC-V targets ([#1657](https://github.com/dot-asm/cc-rs/pull/1657))
- Regenerate windows sys bindings ([#1653](https://github.com/dot-asm/cc-rs/pull/1653))
- Update windows-bindgen requirement from 0.65 to 0.66 ([#1652](https://github.com/dot-asm/cc-rs/pull/1652))
- release ([#1651](https://github.com/dot-asm/cc-rs/pull/1651))
- Fix contradictory doc for CC compiler in crate doc ([#1650](https://github.com/dot-asm/cc-rs/pull/1650))
- Have CUDA compilaion check for sbsa-linux when targeting aarch64. ([#1647](https://github.com/dot-asm/cc-rs/pull/1647))
- Update link for -Cdwarf-version; Remove -Z (stabilized in 1.88) ([#1648](https://github.com/dot-asm/cc-rs/pull/1648))
- Fix Build::env_tool to check for .exe on windows ([#1646](https://github.com/dot-asm/cc-rs/pull/1646))
- Fix tool existence check in find_tool method ([#1645](https://github.com/dot-asm/cc-rs/pull/1645))
- Fix SdkInfo::find_tool to check for executable extension ([#1644](https://github.com/dot-asm/cc-rs/pull/1644))
- release ([#1643](https://github.com/dot-asm/cc-rs/pull/1643))
- Regenerate target info ([#1642](https://github.com/dot-asm/cc-rs/pull/1642))
- Update Readmes ([#1641](https://github.com/dot-asm/cc-rs/pull/1641))
- Update rusqlite requirement from 0.37.0 to 0.38.0 ([#1638](https://github.com/dot-asm/cc-rs/pull/1638))
- *(cc)* release v1.2.50 ([#1636](https://github.com/dot-asm/cc-rs/pull/1636))
- Fix #283: Make warnings(false) actually suppress compiler warnings ([#1633](https://github.com/dot-asm/cc-rs/pull/1633))
- *(cc)* release v1.2.49 ([#1628](https://github.com/dot-asm/cc-rs/pull/1628))
- Fix run_output to prevent infinite blocking ([#1627](https://github.com/dot-asm/cc-rs/pull/1627))
- Fix detect_family deadlock ([#1626](https://github.com/dot-asm/cc-rs/pull/1626))
- Fix link in new debug_str doc comment ([#1625](https://github.com/dot-asm/cc-rs/pull/1625))
- Support more of Cargo's debug levels with Build::debug_str ([#1624](https://github.com/dot-asm/cc-rs/pull/1624))
- *(cc)* release v1.2.48 ([#1621](https://github.com/dot-asm/cc-rs/pull/1621))
- Regenerate target info ([#1620](https://github.com/dot-asm/cc-rs/pull/1620))
- Add publish environment for publishing crate ([#1619](https://github.com/dot-asm/cc-rs/pull/1619))
- *(cc)* release v1.2.47 ([#1617](https://github.com/dot-asm/cc-rs/pull/1617))
- add helenos linker identifications ([#1615](https://github.com/dot-asm/cc-rs/pull/1615))
- Bump actions/checkout from 5 to 6 ([#1616](https://github.com/dot-asm/cc-rs/pull/1616))
- release ([#1611](https://github.com/dot-asm/cc-rs/pull/1611))
- Add Visual Studio 2026 support ([#1609](https://github.com/dot-asm/cc-rs/pull/1609))
- *(cc)* release v1.2.45 ([#1607](https://github.com/dot-asm/cc-rs/pull/1607))
- Regenerate target info ([#1606](https://github.com/dot-asm/cc-rs/pull/1606))
- Use a default check for the "env" variable in apple_sdk_name ([#1605](https://github.com/dot-asm/cc-rs/pull/1605))
- *(cc)* release v1.2.44 ([#1603](https://github.com/dot-asm/cc-rs/pull/1603))
- Fix debug assertion for env/abi mismatch ([#1604](https://github.com/dot-asm/cc-rs/pull/1604))
- Update CHANGELOG for version 1.2.43 ([#1602](https://github.com/dot-asm/cc-rs/pull/1602))
- Stop passing an invalid target to `llvm-mingw`'s cross-compilation wrappers ([#1495](https://github.com/dot-asm/cc-rs/pull/1495))
- Mark `static_flag` and `shared_flag` as deprecated ([#1582](https://github.com/dot-asm/cc-rs/pull/1582))
- *(cc)* release v1.2.42 ([#1597](https://github.com/dot-asm/cc-rs/pull/1597))
- Fix check-semver-checks ([#1600](https://github.com/dot-asm/cc-rs/pull/1600))
- minor improvement for docs ([#1598](https://github.com/dot-asm/cc-rs/pull/1598))
- Fix linker-plugin-lto: use `-flto=thin` ([#1594](https://github.com/dot-asm/cc-rs/pull/1594))
- Disable check-buildstd for armv7k-apple-watchos ([#1599](https://github.com/dot-asm/cc-rs/pull/1599))
- Add elf abi to ppc64 targets ([#1596](https://github.com/dot-asm/cc-rs/pull/1596))
- release ([#1593](https://github.com/dot-asm/cc-rs/pull/1593))
- Allow using VCToolsVersion to request a specific msvc version ([#1589](https://github.com/dot-asm/cc-rs/pull/1589))
- Regenerate target info ([#1592](https://github.com/dot-asm/cc-rs/pull/1592))
- Regenerate windows sys bindings ([#1591](https://github.com/dot-asm/cc-rs/pull/1591))
- Update windows-bindgen requirement from 0.64 to 0.65 ([#1590](https://github.com/dot-asm/cc-rs/pull/1590))
- Fix `get_base_archiver_variant` for clang-cl: use `--print-search-dirs` ([#1587](https://github.com/dot-asm/cc-rs/pull/1587))
- release ([#1583](https://github.com/dot-asm/cc-rs/pull/1583))
- Reorder changelog and remove duplicate Unreleased section ([#1579](https://github.com/dot-asm/cc-rs/pull/1579))
- Prefer clang if linker-plugin-lto specified ([#1573](https://github.com/dot-asm/cc-rs/pull/1573))
- Fix building for Mac Catalyst ([#1577](https://github.com/dot-asm/cc-rs/pull/1577))
- Improve ESP microcontroller targets ([#1574](https://github.com/dot-asm/cc-rs/pull/1574))
- Regenerate windows sys bindings ([#1572](https://github.com/dot-asm/cc-rs/pull/1572))
- Update windows-bindgen requirement from 0.63 to 0.64 ([#1571](https://github.com/dot-asm/cc-rs/pull/1571))
- *(cc)* release v1.2.39 ([#1570](https://github.com/dot-asm/cc-rs/pull/1570))
- Fix cross compilation to xtensa-esp32s3-espidf ([#1569](https://github.com/dot-asm/cc-rs/pull/1569))
- Fix autodetect_wasi_compiler: support non utf-8 path ([#1568](https://github.com/dot-asm/cc-rs/pull/1568))
- Regenerate target info ([#1567](https://github.com/dot-asm/cc-rs/pull/1567))
- Fix rustcflags mapping: require -Clinker-plugin-lto for -flto ([#1564](https://github.com/dot-asm/cc-rs/pull/1564))
- Use `$WASI_SDK_PATH` on WASI targets by default ([#1562](https://github.com/dot-asm/cc-rs/pull/1562))
- Fix atomicity violations in concurrent cache operations ([#1559](https://github.com/dot-asm/cc-rs/pull/1559))
- release ([#1558](https://github.com/dot-asm/cc-rs/pull/1558))
- [win] Search the Windows SDK for tools as well ([#1553](https://github.com/dot-asm/cc-rs/pull/1553))
- use release-plz trusted publishing implementation ([#1556](https://github.com/dot-asm/cc-rs/pull/1556))
- *(cc)* release v1.2.37 ([#1555](https://github.com/dot-asm/cc-rs/pull/1555))
- Fix errmsg in RustcCodegenFlags::set_rustc_flag ([#1551](https://github.com/dot-asm/cc-rs/pull/1551))
- propagate stack protector to Linux C compilers ([#1550](https://github.com/dot-asm/cc-rs/pull/1550))
- Extract new fn `run_commands_in_parallel` ([#1549](https://github.com/dot-asm/cc-rs/pull/1549))
- release ([#1542](https://github.com/dot-asm/cc-rs/pull/1542))
- Regenerate windows sys bindings ([#1548](https://github.com/dot-asm/cc-rs/pull/1548))
- Update windows-bindgen requirement from 0.62 to 0.63 ([#1547](https://github.com/dot-asm/cc-rs/pull/1547))
- Add fn get_ucrt_dir for find-msvc-tools ([#1546](https://github.com/dot-asm/cc-rs/pull/1546))
- Regenerate target info ([#1544](https://github.com/dot-asm/cc-rs/pull/1544))
- fix publish.yml ([#1543](https://github.com/dot-asm/cc-rs/pull/1543))
- Replace periods with underscores as well when parsing env variables ([#1541](https://github.com/dot-asm/cc-rs/pull/1541))
- *(cc)* release v1.2.35 ([#1533](https://github.com/dot-asm/cc-rs/pull/1533))
- Fix semver-checks: Add back functino `windows_registry::find` ([#1539](https://github.com/dot-asm/cc-rs/pull/1539))
- fix crates-io trusted publishing in publish.yml ([#1538](https://github.com/dot-asm/cc-rs/pull/1538))
- use trusted publishing in publish.yml ([#1537](https://github.com/dot-asm/cc-rs/pull/1537))
- Regenerate target info ([#1536](https://github.com/dot-asm/cc-rs/pull/1536))
- Optimize Tool::to_command ([#1535](https://github.com/dot-asm/cc-rs/pull/1535))
- Extract windows-find-tools ([#1531](https://github.com/dot-asm/cc-rs/pull/1531))
- Add prefer_clang_cl_over_msvc ([#1516](https://github.com/dot-asm/cc-rs/pull/1516))
- release v1.2.34 ([#1528](https://github.com/dot-asm/cc-rs/pull/1528))
- Optimize parse_version in find_tools.rs ([#1527](https://github.com/dot-asm/cc-rs/pull/1527))
- Fallback to manually searching for tool dir ([#1526](https://github.com/dot-asm/cc-rs/pull/1526))
- release v1.2.33 ([#1522](https://github.com/dot-asm/cc-rs/pull/1522))
- Regenerate target info ([#1521](https://github.com/dot-asm/cc-rs/pull/1521))
- Bump actions/checkout from 4 to 5 ([#1520](https://github.com/dot-asm/cc-rs/pull/1520))
- [win][arm64ec] Add testing for Arm64EC Windows ([#1512](https://github.com/dot-asm/cc-rs/pull/1512))
- Fix gen-windows-sys-binding ([#1518](https://github.com/dot-asm/cc-rs/pull/1518))
- Fix parsing of nigthly targets ([#1517](https://github.com/dot-asm/cc-rs/pull/1517))
- [win][arm64ec] Fix finding assembler and setting is_arm for Arm64EC ([#1511](https://github.com/dot-asm/cc-rs/pull/1511))
- release v1.2.32 ([#1510](https://github.com/dot-asm/cc-rs/pull/1510))
- clarify cargo default if no rerun emitted ([#1508](https://github.com/dot-asm/cc-rs/pull/1508))
- extract compile_objects_sequential ([#1507](https://github.com/dot-asm/cc-rs/pull/1507))
- Windows `find_tools`: add support for finding Clang ([#1506](https://github.com/dot-asm/cc-rs/pull/1506))
- Add m68k-unknown-linux-gnu cross-compile target ([#1505](https://github.com/dot-asm/cc-rs/pull/1505))
- release v1.2.31 ([#1504](https://github.com/dot-asm/cc-rs/pull/1504))
- Add doc for using sccache/ccache etc ([#1502](https://github.com/dot-asm/cc-rs/pull/1502))
- ability to statically link against C++ stdlib ([#1497](https://github.com/dot-asm/cc-rs/pull/1497))
- Add instructions on using sccache ([#1503](https://github.com/dot-asm/cc-rs/pull/1503))
- Add support for recognizing some architectures supported by GCC, but not LLVM. ([#1500](https://github.com/dot-asm/cc-rs/pull/1500))
- release v1.2.30 ([#1498](https://github.com/dot-asm/cc-rs/pull/1498))
- define _REENTRANT by default ([#1496](https://github.com/dot-asm/cc-rs/pull/1496))
- Update rusqlite requirement from 0.36.0 to 0.37.0 ([#1494](https://github.com/dot-asm/cc-rs/pull/1494))
- release v1.2.29 ([#1493](https://github.com/dot-asm/cc-rs/pull/1493))
- Fix target parsing for powerpc ([#1490](https://github.com/dot-asm/cc-rs/pull/1490))
- release v1.2.28 ([#1491](https://github.com/dot-asm/cc-rs/pull/1491))
- Recognize `mlibc` environment ([#1488](https://github.com/dot-asm/cc-rs/pull/1488))
- Fix clippy warnings about not using variables in `format!` strings ([#1489](https://github.com/dot-asm/cc-rs/pull/1489))
- release v1.2.27 ([#1486](https://github.com/dot-asm/cc-rs/pull/1486))
- Regenerate windows sys bindings ([#1485](https://github.com/dot-asm/cc-rs/pull/1485))
- Update windows-bindgen requirement from 0.61 to 0.62 ([#1484](https://github.com/dot-asm/cc-rs/pull/1484))
- Regenerate target info ([#1483](https://github.com/dot-asm/cc-rs/pull/1483))
- release v1.2.26 ([#1481](https://github.com/dot-asm/cc-rs/pull/1481))
- Also set `SDKROOT` when building apple platforms ([#1475](https://github.com/dot-asm/cc-rs/pull/1475))
- use windows 2022 in CI ([#1479](https://github.com/dot-asm/cc-rs/pull/1479))
- Detect -Wslash-u-filename warning on clang-cl ([#1477](https://github.com/dot-asm/cc-rs/pull/1477))
- release v1.2.25 ([#1478](https://github.com/dot-asm/cc-rs/pull/1478))
- make `powerp64` use `powerpc64-linux-gnu` prefix ([#1474](https://github.com/dot-asm/cc-rs/pull/1474))
- Update rusqlite requirement from 0.35.0 to 0.36.0 ([#1476](https://github.com/dot-asm/cc-rs/pull/1476))
- release v1.2.24 ([#1472](https://github.com/dot-asm/cc-rs/pull/1472))
- Regenerate windows sys bindings ([#1471](https://github.com/dot-asm/cc-rs/pull/1471))
- release v1.2.23 ([#1470](https://github.com/dot-asm/cc-rs/pull/1470))
- support "vxworks" and "nto" OSes on `get_base_archiver_variant` ([#1456](https://github.com/dot-asm/cc-rs/pull/1456))
- release v1.2.22 ([#1467](https://github.com/dot-asm/cc-rs/pull/1467))
- Add `flags` method to `cc::Build` for adding multiple flags ([#1466](https://github.com/dot-asm/cc-rs/pull/1466))
- release v1.2.21 ([#1464](https://github.com/dot-asm/cc-rs/pull/1464))
- Fix wasm32-unknown-unknown by passing -c ([#1424](https://github.com/dot-asm/cc-rs/pull/1424))
- release v1.2.20 ([#1462](https://github.com/dot-asm/cc-rs/pull/1462))
- Regenerate target info ([#1461](https://github.com/dot-asm/cc-rs/pull/1461))
- Update rusqlite requirement from 0.34.0 to 0.35.0 ([#1460](https://github.com/dot-asm/cc-rs/pull/1460))
- Fix parser.rs on latest rustc nightly ([#1459](https://github.com/dot-asm/cc-rs/pull/1459))
- release v1.2.19 ([#1458](https://github.com/dot-asm/cc-rs/pull/1458))
- Fix musl compilation: Add musl as a prefix fallback ([#1455](https://github.com/dot-asm/cc-rs/pull/1455))
- release v1.2.18 ([#1451](https://github.com/dot-asm/cc-rs/pull/1451))
- Regenerate target info ([#1450](https://github.com/dot-asm/cc-rs/pull/1450))
- Use `std::thread::available_parallelism` for determining the default number of jobs ([#1447](https://github.com/dot-asm/cc-rs/pull/1447))
- Fix mips64-openwrt-linux-musl parsing ([#1449](https://github.com/dot-asm/cc-rs/pull/1449))
- Use compiler prefix `x86_64-linux-musl` ([#1443](https://github.com/dot-asm/cc-rs/pull/1443))
- release v1.2.17 ([#1435](https://github.com/dot-asm/cc-rs/pull/1435))
- Regenerate target info ([#1439](https://github.com/dot-asm/cc-rs/pull/1439))
- Regenerate windows sys bindings ([#1437](https://github.com/dot-asm/cc-rs/pull/1437))
- Update windows-bindgen requirement from 0.60 to 0.61 ([#1436](https://github.com/dot-asm/cc-rs/pull/1436))
- Fix wasm32-wali-linux-musl target parsing ([#1434](https://github.com/dot-asm/cc-rs/pull/1434))
- fix creating issue comment ([#1433](https://github.com/dot-asm/cc-rs/pull/1433))
- Fix failure from cargo not propagating because of pipe ([#1432](https://github.com/dot-asm/cc-rs/pull/1432))
- Parse `rustc` target names ([#1413](https://github.com/dot-asm/cc-rs/pull/1413))
- Regenerate target info ([#1429](https://github.com/dot-asm/cc-rs/pull/1429))
- Added base support for `wasm32-wali-linux-musl` target ([#1373](https://github.com/dot-asm/cc-rs/pull/1373))
- Update rusqlite requirement from 0.33.0 to 0.34.0 ([#1428](https://github.com/dot-asm/cc-rs/pull/1428))
- release v1.2.16 ([#1427](https://github.com/dot-asm/cc-rs/pull/1427))
- use `/arch:SSE2` for `x86` target arch ([#1425](https://github.com/dot-asm/cc-rs/pull/1425))
- Regenerate windows-sys binding ([#1422](https://github.com/dot-asm/cc-rs/pull/1422))
- Fix gen-windows-sys-binding ([#1419](https://github.com/dot-asm/cc-rs/pull/1419))
- Fix regenerate-windows-sys.yml ([#1420](https://github.com/dot-asm/cc-rs/pull/1420))
- Regenerate target info ([#1418](https://github.com/dot-asm/cc-rs/pull/1418))
- Add LIB var when compiling flag_check ([#1417](https://github.com/dot-asm/cc-rs/pull/1417))
- Change flag ordering ([#1403](https://github.com/dot-asm/cc-rs/pull/1403))
- Update windows-bindgen requirement from 0.59 to 0.60 ([#1412](https://github.com/dot-asm/cc-rs/pull/1412))
- Fix archiver detection for musl cross compilation ([#1404](https://github.com/dot-asm/cc-rs/pull/1404))
- release v1.2.15 ([#1408](https://github.com/dot-asm/cc-rs/pull/1408))
- Regenerate target info ([#1406](https://github.com/dot-asm/cc-rs/pull/1406))
- Always read from all `CFLAGS`-style flags ([#1401](https://github.com/dot-asm/cc-rs/pull/1401))
- Simplify the error output on failed `Command` invocation ([#1397](https://github.com/dot-asm/cc-rs/pull/1397))
- release v1.2.14 ([#1400](https://github.com/dot-asm/cc-rs/pull/1400))
- Regenerate target info ([#1398](https://github.com/dot-asm/cc-rs/pull/1398))
- Add support for setting `-gdwarf-{version}` based on RUSTFLAGS ([#1395](https://github.com/dot-asm/cc-rs/pull/1395))
- Add support for alternative network stack io-sock on QNX 7.1 aarch64 and x86_64 ([#1312](https://github.com/dot-asm/cc-rs/pull/1312))
- release v1.2.13 ([#1394](https://github.com/dot-asm/cc-rs/pull/1394))
- Fix cross-compiling for Apple platforms ([#1389](https://github.com/dot-asm/cc-rs/pull/1389))
- release v1.2.12 ([#1387](https://github.com/dot-asm/cc-rs/pull/1387))
- Split impl Build ([#1382](https://github.com/dot-asm/cc-rs/pull/1382))
- ensure `clang --driver-mode=cl` is MSVC- and `clang-cl`-like ([#1381](https://github.com/dot-asm/cc-rs/pull/1381))
- allow specifying `rustc` when generating target information ([#1385](https://github.com/dot-asm/cc-rs/pull/1385))
- Don't specify both `-target` and `-mtargetos=` on Apple targets ([#1384](https://github.com/dot-asm/cc-rs/pull/1384))
- release v1.2.11 ([#1377](https://github.com/dot-asm/cc-rs/pull/1377))
- Fix more flag inheritance ([#1380](https://github.com/dot-asm/cc-rs/pull/1380))
- Include wrapper args. in `stdout` family heuristics to restore classifying `clang --driver-mode=cl` as `Msvc { clang_cl: true }` ([#1378](https://github.com/dot-asm/cc-rs/pull/1378))
- Constrain `-Clto` and `-Cembed-bitcode` flag inheritance to be `clang`-only ([#1379](https://github.com/dot-asm/cc-rs/pull/1379))
- Pass deployment target with `-m*-version-min=` ([#1339](https://github.com/dot-asm/cc-rs/pull/1339))
- Regenerate target info ([#1376](https://github.com/dot-asm/cc-rs/pull/1376))
- Update rusqlite requirement from 0.32.0 to 0.33.0 ([#1374](https://github.com/dot-asm/cc-rs/pull/1374))
- release v1.2.10 ([#1370](https://github.com/dot-asm/cc-rs/pull/1370))
- Fix CC_FORCE_DISABLE=0 evaluating to true ([#1371](https://github.com/dot-asm/cc-rs/pull/1371))
- Regenerate target info ([#1369](https://github.com/dot-asm/cc-rs/pull/1369))
- *(ci)* move ubuntu-20 job to ubuntu-22 ([#1368](https://github.com/dot-asm/cc-rs/pull/1368))
- Make hidden lifetimes explicit. ([#1366](https://github.com/dot-asm/cc-rs/pull/1366))
- release v1.2.9 ([#1365](https://github.com/dot-asm/cc-rs/pull/1365))
- Don't pass inherited PGO flags to GNU compilers ([#1363](https://github.com/dot-asm/cc-rs/pull/1363))
- Adjusted zig cc judgment and avoided zigbuild errors([#1360](https://github.com/dot-asm/cc-rs/pull/1360)) ([#1361](https://github.com/dot-asm/cc-rs/pull/1361))
- Fix compilation on macOS using clang and fix compilation using zig-cc ([#1364](https://github.com/dot-asm/cc-rs/pull/1364))
- release v1.2.8 ([#1355](https://github.com/dot-asm/cc-rs/pull/1355))
- Add `is_like_clang_cl()` getter ([#1357](https://github.com/dot-asm/cc-rs/pull/1357))
- Fix clippy error in lib.rs ([#1356](https://github.com/dot-asm/cc-rs/pull/1356))
- Fix opening PR in regenerate-windows-sys.yml ([#1353](https://github.com/dot-asm/cc-rs/pull/1353))
- Regenerate target info ([#1352](https://github.com/dot-asm/cc-rs/pull/1352))
- Fix opening PR in regenerate-target-info.yml ([#1351](https://github.com/dot-asm/cc-rs/pull/1351))
- Fix compiler family detection issue with clang-cl on macOS ([#1328](https://github.com/dot-asm/cc-rs/pull/1328))
- Run regenerate-windows-sys on Thu ([#1348](https://github.com/dot-asm/cc-rs/pull/1348))
- Run regenerate-target-info on Thu ([#1349](https://github.com/dot-asm/cc-rs/pull/1349))
- Update `windows-bindgen` dependency ([#1347](https://github.com/dot-asm/cc-rs/pull/1347))
- Fix clippy warnings ([#1346](https://github.com/dot-asm/cc-rs/pull/1346))
- Optimize CI ([#1344](https://github.com/dot-asm/cc-rs/pull/1344))
- Fix cuda testing ([#1343](https://github.com/dot-asm/cc-rs/pull/1343))
- release v1.2.7 ([#1341](https://github.com/dot-asm/cc-rs/pull/1341))
- Regenerate target info ([#1342](https://github.com/dot-asm/cc-rs/pull/1342))
- Add "test-pass" job ([#1340](https://github.com/dot-asm/cc-rs/pull/1340))
- Document new supported architecture names in windows::find
- Make is_flag_supported_inner take an &Tool ([#1337](https://github.com/dot-asm/cc-rs/pull/1337))
- Fix is_flag_supported on msvc ([#1336](https://github.com/dot-asm/cc-rs/pull/1336))
- Allow using Visual Studio target names in `find_tool` ([#1335](https://github.com/dot-asm/cc-rs/pull/1335))
- Fix caching ([#1334](https://github.com/dot-asm/cc-rs/pull/1334))
- release v1.2.6 ([#1333](https://github.com/dot-asm/cc-rs/pull/1333))
- Don't inherit the `/Oy` flag for 64-bit targets ([#1330](https://github.com/dot-asm/cc-rs/pull/1330))
- release v1.2.5 ([#1323](https://github.com/dot-asm/cc-rs/pull/1323))
- Check linking when testing if compiler flags are supported ([#1322](https://github.com/dot-asm/cc-rs/pull/1322))
- release v1.2.4 ([#1320](https://github.com/dot-asm/cc-rs/pull/1320))
- Add support for C/C++ compiler for Neutrino QNX: `qcc` ([#1319](https://github.com/dot-asm/cc-rs/pull/1319))
- use -maix64 instead of -m64 ([#1307](https://github.com/dot-asm/cc-rs/pull/1307))
- release v1.2.3 ([#1316](https://github.com/dot-asm/cc-rs/pull/1316))
- Enable manual-run of release-pr.yml ([#1318](https://github.com/dot-asm/cc-rs/pull/1318))
- Improve detection of environment when compiling from msbuild or msvc ([#1310](https://github.com/dot-asm/cc-rs/pull/1310))
- Better error message when failing on unknown targets ([#1313](https://github.com/dot-asm/cc-rs/pull/1313))
- Optimize RustcCodegenFlags ([#1305](https://github.com/dot-asm/cc-rs/pull/1305))
- release v1.2.2 ([#1306](https://github.com/dot-asm/cc-rs/pull/1306))
- Inherit flags from rustc ([#1279](https://github.com/dot-asm/cc-rs/pull/1279))
- Add support for using sccache wrapper with cuda/nvcc ([#1304](https://github.com/dot-asm/cc-rs/pull/1304))
- Fix msvc stdout not shown on error ([#1303](https://github.com/dot-asm/cc-rs/pull/1303))
- Avoid running scheduled jobs on forks ([#1302](https://github.com/dot-asm/cc-rs/pull/1302))
- Regenerate target info ([#1301](https://github.com/dot-asm/cc-rs/pull/1301))
- Fix compilation of C++ code for armv7-unknown-linux-gnueabihf ([#1298](https://github.com/dot-asm/cc-rs/pull/1298))
- Fetch target info from Cargo even if `Build::target` is manually set ([#1299](https://github.com/dot-asm/cc-rs/pull/1299))
- Fix two files with different extensions having the same object name ([#1295](https://github.com/dot-asm/cc-rs/pull/1295))
- Allow disabling cc's ability to compile via env var CC_FORCE_DISABLE ([#1292](https://github.com/dot-asm/cc-rs/pull/1292))
- Regenerate target info ([#1293](https://github.com/dot-asm/cc-rs/pull/1293))
- Cap release at once per week ([#1291](https://github.com/dot-asm/cc-rs/pull/1291))
- release v1.2.1 ([#1289](https://github.com/dot-asm/cc-rs/pull/1289))
- When invoking `cl -?`, set stdin to null ([#1288](https://github.com/dot-asm/cc-rs/pull/1288))
- release v1.1.38 ([#1286](https://github.com/dot-asm/cc-rs/pull/1286))
- Allow only specifying the architecture ([#1285](https://github.com/dot-asm/cc-rs/pull/1285))
- Fix WASM vs. WASI options ([#1284](https://github.com/dot-asm/cc-rs/pull/1284))
- release v1.1.37 ([#1282](https://github.com/dot-asm/cc-rs/pull/1282))
- Use relative directory for obj files hash ([#1270](https://github.com/dot-asm/cc-rs/pull/1270))
- Regenerate target info ([#1280](https://github.com/dot-asm/cc-rs/pull/1280))
- release v1.1.36 ([#1274](https://github.com/dot-asm/cc-rs/pull/1274))
- Fix CUDA build with clang++. ([#1273](https://github.com/dot-asm/cc-rs/pull/1273))
- release v1.1.35 ([#1267](https://github.com/dot-asm/cc-rs/pull/1267))
- Remove support for FRC ([#1268](https://github.com/dot-asm/cc-rs/pull/1268))
- Do not add -fPIC by default on UEFI targets ([#1263](https://github.com/dot-asm/cc-rs/pull/1263))
- Use -windows-gnu for all UEFI targets ([#1264](https://github.com/dot-asm/cc-rs/pull/1264))
- release v1.1.34 ([#1259](https://github.com/dot-asm/cc-rs/pull/1259))
- Remove redundant flags ([#1256](https://github.com/dot-asm/cc-rs/pull/1256))
- release v1.1.33 ([#1258](https://github.com/dot-asm/cc-rs/pull/1258))
- Reduce size of `cc::Build`  and size of generated targets ([#1257](https://github.com/dot-asm/cc-rs/pull/1257))
- release v1.1.32 ([#1250](https://github.com/dot-asm/cc-rs/pull/1250))
- Use `rustc`'s knowledge of LLVM/Clang target triples ([#1252](https://github.com/dot-asm/cc-rs/pull/1252))
- Use Cargo's target information when possible ([#1225](https://github.com/dot-asm/cc-rs/pull/1225))
- release v1.1.31 ([#1248](https://github.com/dot-asm/cc-rs/pull/1248))
- Add comment explaining why cc does not rebuild on env PATH change ([#1247](https://github.com/dot-asm/cc-rs/pull/1247))
- release ([#1246](https://github.com/dot-asm/cc-rs/pull/1246))
- Don't pass -fPIC by default on wasm ([#1245](https://github.com/dot-asm/cc-rs/pull/1245))
- release ([#1244](https://github.com/dot-asm/cc-rs/pull/1244))
- Regenerate target info ([#1243](https://github.com/dot-asm/cc-rs/pull/1243))
- release ([#1239](https://github.com/dot-asm/cc-rs/pull/1239))
- Environment variables: For one accepting boolean, treat "0", "false" and empty env as false ([#1238](https://github.com/dot-asm/cc-rs/pull/1238))
- release ([#1235](https://github.com/dot-asm/cc-rs/pull/1235))
- Revert "Use debug version of MSVC runtime library on debug ([#1231](https://github.com/dot-asm/cc-rs/pull/1231))" ([#1237](https://github.com/dot-asm/cc-rs/pull/1237))
- Disable `CC_ENABLE_DEBUG_OUTPUT` if it is set to "0" ([#1234](https://github.com/dot-asm/cc-rs/pull/1234))
- release ([#1232](https://github.com/dot-asm/cc-rs/pull/1232))
- Use debug version of MSVC runtime library on debug ([#1231](https://github.com/dot-asm/cc-rs/pull/1231))
- release ([#1229](https://github.com/dot-asm/cc-rs/pull/1229))
- Remove incorrect "lib" prefixes in CXXSTDLIB doc comments ([#1228](https://github.com/dot-asm/cc-rs/pull/1228))
- release ([#1223](https://github.com/dot-asm/cc-rs/pull/1223))
- Fix wasm32-wasip1-threads:  shared-memory disallowed due to not compiled with 'atomics' or 'bulk-memory' features ([#1221](https://github.com/dot-asm/cc-rs/pull/1221))
- Reduce the need for the host target triple ([#1224](https://github.com/dot-asm/cc-rs/pull/1224))
- Add auto cancellation for CI jobs ([#1222](https://github.com/dot-asm/cc-rs/pull/1222))
- release ([#1220](https://github.com/dot-asm/cc-rs/pull/1220))
- Update doc for detecting changes/upgrades of compilers ([#1218](https://github.com/dot-asm/cc-rs/pull/1218))
- release ([#1216](https://github.com/dot-asm/cc-rs/pull/1216))
- Don't rerun if PATH changes ([#1215](https://github.com/dot-asm/cc-rs/pull/1215))
- release ([#1213](https://github.com/dot-asm/cc-rs/pull/1213))
- disable pic for targets that end in `-none` ([#1212](https://github.com/dot-asm/cc-rs/pull/1212))
- release ([#1210](https://github.com/dot-asm/cc-rs/pull/1210))
- Add buildcache as known Rust and C/C++ compiler wrapper ([#1209](https://github.com/dot-asm/cc-rs/pull/1209))
- release ([#1208](https://github.com/dot-asm/cc-rs/pull/1208))
- Add support arm64e-apple-darwin ([#1207](https://github.com/dot-asm/cc-rs/pull/1207))
- release ([#1204](https://github.com/dot-asm/cc-rs/pull/1204))
- Fixed unsoundness in `StderrForwarder::forward_available` ([#1203](https://github.com/dot-asm/cc-rs/pull/1203))
- release ([#1202](https://github.com/dot-asm/cc-rs/pull/1202))
- release ([#1199](https://github.com/dot-asm/cc-rs/pull/1199))
- Treat VxWorks wr-cc as a Gnu compiler ([#1198](https://github.com/dot-asm/cc-rs/pull/1198))
- release ([#1195](https://github.com/dot-asm/cc-rs/pull/1195))
- Add -mfloat-abi=hard as a default argument when using any arm/thumb-none-eabihf target ([#1194](https://github.com/dot-asm/cc-rs/pull/1194))
- release ([#1191](https://github.com/dot-asm/cc-rs/pull/1191))
- allow finding tools from path if VisualStudioDir is set
- release ([#1187](https://github.com/dot-asm/cc-rs/pull/1187))
- Fix detect family: should detect emscripten as clang, closes #1185 ([#1186](https://github.com/dot-asm/cc-rs/pull/1186))
- release ([#1184](https://github.com/dot-asm/cc-rs/pull/1184))
- improve docs ([#1183](https://github.com/dot-asm/cc-rs/pull/1183))
- release ([#1182](https://github.com/dot-asm/cc-rs/pull/1182))
- Add support for parsing shell encoded `*FLAGS` ([#1181](https://github.com/dot-asm/cc-rs/pull/1181))
- Replace vector of tuples with BTreeMap which already is sorted and free of duplicates ([#1177](https://github.com/dot-asm/cc-rs/pull/1177))
- release ([#1179](https://github.com/dot-asm/cc-rs/pull/1179))
- Remap Windows targets triples to their LLVM counterparts ([#1176](https://github.com/dot-asm/cc-rs/pull/1176))
- release ([#1178](https://github.com/dot-asm/cc-rs/pull/1178))
- Add custom CC wrapper to the wrapper whitelist ([#1175](https://github.com/dot-asm/cc-rs/pull/1175))
- release ([#1174](https://github.com/dot-asm/cc-rs/pull/1174))
- Fix broken link in docs.rs ([#1173](https://github.com/dot-asm/cc-rs/pull/1173))
- release ([#1168](https://github.com/dot-asm/cc-rs/pull/1168))
- add `.objects` ([#1166](https://github.com/dot-asm/cc-rs/pull/1166))
- release ([#1164](https://github.com/dot-asm/cc-rs/pull/1164))
- Clippy fixes ([#1163](https://github.com/dot-asm/cc-rs/pull/1163))
- release ([#1162](https://github.com/dot-asm/cc-rs/pull/1162))
- Fix cyclic compilation: Use vendored once_cell ([#1154](https://github.com/dot-asm/cc-rs/pull/1154))
- release ([#1161](https://github.com/dot-asm/cc-rs/pull/1161))
- Support compiling on wasm targets (Supersede #1068) ([#1160](https://github.com/dot-asm/cc-rs/pull/1160))
- release ([#1155](https://github.com/dot-asm/cc-rs/pull/1155))
- Reduce msrv to 1.63 ([#1158](https://github.com/dot-asm/cc-rs/pull/1158))
- Revert "Use raw-dylib for windows-sys ([#1137](https://github.com/dot-asm/cc-rs/pull/1137))" ([#1157](https://github.com/dot-asm/cc-rs/pull/1157))
- Fix typos ([#1152](https://github.com/dot-asm/cc-rs/pull/1152))
- Fix `doc_lazy_continuation` lints ([#1153](https://github.com/dot-asm/cc-rs/pull/1153))
- release ([#1151](https://github.com/dot-asm/cc-rs/pull/1151))
- Add empty `jobserver` feature. ([#1150](https://github.com/dot-asm/cc-rs/pull/1150))
- release ([#1149](https://github.com/dot-asm/cc-rs/pull/1149))
- Fix is_flag_supported not respecting emit_rerun_if_env_changed ([#1147](https://github.com/dot-asm/cc-rs/pull/1147)) ([#1148](https://github.com/dot-asm/cc-rs/pull/1148))
- release ([#1145](https://github.com/dot-asm/cc-rs/pull/1145))
- release ([#1142](https://github.com/dot-asm/cc-rs/pull/1142))
- Drop support for Visual Studio 12 (2013) ([#1046](https://github.com/dot-asm/cc-rs/pull/1046))
- Use raw-dylib for windows-sys ([#1137](https://github.com/dot-asm/cc-rs/pull/1137))
- Bump msrv to 1.67 ([#1143](https://github.com/dot-asm/cc-rs/pull/1143))
- Bump msrv to 1.65 ([#1140](https://github.com/dot-asm/cc-rs/pull/1140))
- Fix clippy warnings ([#1138](https://github.com/dot-asm/cc-rs/pull/1138))
- release ([#1136](https://github.com/dot-asm/cc-rs/pull/1136))
- Regenerate windows sys bindings ([#1132](https://github.com/dot-asm/cc-rs/pull/1132))
- Fix generate-windows-sys-bindings ([#1133](https://github.com/dot-asm/cc-rs/pull/1133))
- Fix gen-windows-sys-binding ([#1130](https://github.com/dot-asm/cc-rs/pull/1130))
- Fix gen-windows-sys-binding ([#1127](https://github.com/dot-asm/cc-rs/pull/1127))
- Update windows-bindgen requirement from 0.57 to 0.58 ([#1123](https://github.com/dot-asm/cc-rs/pull/1123))
- release ([#1119](https://github.com/dot-asm/cc-rs/pull/1119))
- Fixed link break about compile-time-requirements ([#1118](https://github.com/dot-asm/cc-rs/pull/1118))
- release ([#1116](https://github.com/dot-asm/cc-rs/pull/1116))
- Fix compilation for wasm: env WASI_SYSROOT should be optional ([#1114](https://github.com/dot-asm/cc-rs/pull/1114))
- release ([#1112](https://github.com/dot-asm/cc-rs/pull/1112))
- Fix invalid wasi targets compatibility ([#1105](https://github.com/dot-asm/cc-rs/pull/1105))
- Speedup regenerate-target-info and regenerate-windows-sys ([#1110](https://github.com/dot-asm/cc-rs/pull/1110))
- release ([#1106](https://github.com/dot-asm/cc-rs/pull/1106))
- Use `Build::getenv` instead of `env::var*` in anywhere that makes sense ([#1103](https://github.com/dot-asm/cc-rs/pull/1103))
- release ([#1102](https://github.com/dot-asm/cc-rs/pull/1102))
- Update publish.yml to use release-plz ([#1101](https://github.com/dot-asm/cc-rs/pull/1101))
- Accpet `OsStr` instead of `str` for flags ([#1100](https://github.com/dot-asm/cc-rs/pull/1100))
- Use `dep:` syntax to avoid implicit features. ([#1099](https://github.com/dot-asm/cc-rs/pull/1099))
- Minor clippy fixes. ([#1098](https://github.com/dot-asm/cc-rs/pull/1098))
- Fix WASI compilation for C++ ([#1083](https://github.com/dot-asm/cc-rs/pull/1083))
- Regenerate windows sys bindings ([#1096](https://github.com/dot-asm/cc-rs/pull/1096))
- Rename regenerate-windows-sys to regenerate-windows-sys.yml ([#1095](https://github.com/dot-asm/cc-rs/pull/1095))
- Create regenerate-windows-sys.yml ([#1094](https://github.com/dot-asm/cc-rs/pull/1094))
- Update windows-bindgen requirement from 0.56 to 0.57 ([#1091](https://github.com/dot-asm/cc-rs/pull/1091))
- Eagerly close tempfile to fix #1082 ([#1087](https://github.com/dot-asm/cc-rs/pull/1087))
- Output msvc.exe in the output directory ([#1090](https://github.com/dot-asm/cc-rs/pull/1090))
- Fix clippy warnings on Windows ([#1088](https://github.com/dot-asm/cc-rs/pull/1088))
- Don't try to free DLL on drop ([#1089](https://github.com/dot-asm/cc-rs/pull/1089))
- Fix panic safety issue in StderrForwarder ([#1079](https://github.com/dot-asm/cc-rs/pull/1079))
- Release cc 1.0.99 ([#1086](https://github.com/dot-asm/cc-rs/pull/1086))
- Allow opt-out the -ccbin flag ([#1085](https://github.com/dot-asm/cc-rs/pull/1085))
- Release cc 1.0.98 ([#1073](https://github.com/dot-asm/cc-rs/pull/1073))
- Fix detect_compiler_family.c not being created ([#1072](https://github.com/dot-asm/cc-rs/pull/1072))
- Fix paths on Mac Catalyst ([#1070](https://github.com/dot-asm/cc-rs/pull/1070))
- Cleanup some deprecated, unused allows ([#1067](https://github.com/dot-asm/cc-rs/pull/1067))
- Release cc 1.0.97 ([#1066](https://github.com/dot-asm/cc-rs/pull/1066))
- Avoid recursive calls into try_get_compiler when items are in the cache ([#1050](https://github.com/dot-asm/cc-rs/pull/1050))
- Bump actions/checkout from 3 to 4 ([#1064](https://github.com/dot-asm/cc-rs/pull/1064))
- Rm unnecessary println in try_get_compiler ([#1063](https://github.com/dot-asm/cc-rs/pull/1063))
- Don't use the value of SDKROOT if it doesn't match the target. ([#1047](https://github.com/dot-asm/cc-rs/pull/1047))
- Run cargo-semver-checks for every PR and commits to main ([#1053](https://github.com/dot-asm/cc-rs/pull/1053))
- Fix commit message in regenerate-target-info.yml ([#1062](https://github.com/dot-asm/cc-rs/pull/1062))
- Regenerate target info ([#1061](https://github.com/dot-asm/cc-rs/pull/1061))
- Fix `regenerate-target-info.yml` ([#1060](https://github.com/dot-asm/cc-rs/pull/1060))
- Fix running gen-target-info in regenerate-target-info.yml ([#1057](https://github.com/dot-asm/cc-rs/pull/1057))
- Fix file extension for pipelime regenerate-target-info ([#1056](https://github.com/dot-asm/cc-rs/pull/1056))
- Create regenerate-target-info ([#1055](https://github.com/dot-asm/cc-rs/pull/1055))
- Release cc 1.0.96 ([#1045](https://github.com/dot-asm/cc-rs/pull/1045))
- Add support for linking against the "spectre-mitigated" CRT ([#673](https://github.com/dot-asm/cc-rs/pull/673))
- Use specified include directories prior to CFLAGS ([#1043](https://github.com/dot-asm/cc-rs/pull/1043))
- Release cc 1.0.95 ([#1038](https://github.com/dot-asm/cc-rs/pull/1038))
- Optimize jobserver `try_acquire` ([#1037](https://github.com/dot-asm/cc-rs/pull/1037))
- Bump msrv to 1.63 ([#1031](https://github.com/dot-asm/cc-rs/pull/1031))
- Update windows-bindgen requirement from 0.55 to 0.56 ([#1035](https://github.com/dot-asm/cc-rs/pull/1035))
- Release cc 1.0.94 ([#1034](https://github.com/dot-asm/cc-rs/pull/1034))
- Release cc-rs 1.0.93 ([#1032](https://github.com/dot-asm/cc-rs/pull/1032))
- Add visionOS support ([#1029](https://github.com/dot-asm/cc-rs/pull/1029))
- Release cc 1.0.92 ([#1028](https://github.com/dot-asm/cc-rs/pull/1028))
- Fix linking with llvm-lib ([#1027](https://github.com/dot-asm/cc-rs/pull/1027))
- Release cc 1.0.91 ([#1024](https://github.com/dot-asm/cc-rs/pull/1024))
- Fix caching of supported compiler flag ([#1002](https://github.com/dot-asm/cc-rs/pull/1002))
- Also shim llvm-ar in the clang_android test on non-Windows ([#1016](https://github.com/dot-asm/cc-rs/pull/1016))
- Fix regression in compiler family detection ([#1014](https://github.com/dot-asm/cc-rs/pull/1014))
- Optimize code based on cargo clippy suggestions ([#1013](https://github.com/dot-asm/cc-rs/pull/1013))
- Fix compile family detection: Use C macros instead of `$compiler -v` ([#1000](https://github.com/dot-asm/cc-rs/pull/1000))
- Fix safety comment for LibraryHandle::get_proc_address ([#1010](https://github.com/dot-asm/cc-rs/pull/1010))
- Add automatic publish on tag creation ([#978](https://github.com/dot-asm/cc-rs/pull/978))
- Accept non utf-8 characters in compiler and archiver ([#998](https://github.com/dot-asm/cc-rs/pull/998))
- Update windows-bindgen requirement from 0.54 to 0.55 ([#999](https://github.com/dot-asm/cc-rs/pull/999))
- Release cc 1.0.90 ([#996](https://github.com/dot-asm/cc-rs/pull/996))
- Merge pull request #993 from djkoloski/fix-riscv-clang-targets
- Drop support for Visual Studio 11 (2012) ([#981](https://github.com/dot-asm/cc-rs/pull/981))
- Fix arm-android compile-ui tests ([#991](https://github.com/dot-asm/cc-rs/pull/991))
- Revert "refactor target flags ([#873](https://github.com/dot-asm/cc-rs/pull/873))" ([#992](https://github.com/dot-asm/cc-rs/pull/992))
- Release cc 1.0.89 ([#988](https://github.com/dot-asm/cc-rs/pull/988))
- Fix make resource failure when cc parallel is enabled ([#985](https://github.com/dot-asm/cc-rs/pull/985))
- Add a public file iterator ([#987](https://github.com/dot-asm/cc-rs/pull/987))
- Use llvm-ar, llvm-ranlib for Android NDK ([#983](https://github.com/dot-asm/cc-rs/pull/983))
- Also support finding Windows tools on non-Windows host ([#907](https://github.com/dot-asm/cc-rs/pull/907))
- Update windows-bindgen requirement from 0.53 to 0.54 ([#982](https://github.com/dot-asm/cc-rs/pull/982))
- refactor target flags ([#873](https://github.com/dot-asm/cc-rs/pull/873))
- Release cc 1.0.88 ([#977](https://github.com/dot-asm/cc-rs/pull/977))
- Fix set_blocking ([#975](https://github.com/dot-asm/cc-rs/pull/975))
- Add `/System/iOSSupport` to header/library search paths on Mac Catalyst ([#961](https://github.com/dot-asm/cc-rs/pull/961))
- Release cc 1.0.87 ([#967](https://github.com/dot-asm/cc-rs/pull/967))
- Fix use of cc with make <4.3: Clear O_NONBLOCK after compilaton ([#966](https://github.com/dot-asm/cc-rs/pull/966))
- add armv8r-none-eabihf ([#836](https://github.com/dot-asm/cc-rs/pull/836))
- Support native ARM64 MSVC toolchain, and fallback to x64 if emulation is available ([#957](https://github.com/dot-asm/cc-rs/pull/957))
- Added tvos-sim support ([#951](https://github.com/dot-asm/cc-rs/pull/951))
- Fix CI (Test) nightly ([#956](https://github.com/dot-asm/cc-rs/pull/956))
- Release cc 1.0.86 ([#952](https://github.com/dot-asm/cc-rs/pull/952))
- Cache compiler versions detected ([#932](https://github.com/dot-asm/cc-rs/pull/932))
- Fix setting O_NONBLOCK in parallel::stderr::set_non_blocking ([#946](https://github.com/dot-asm/cc-rs/pull/946))
- Fix jobserver: Last `--jobserver-auth` wins ([#949](https://github.com/dot-asm/cc-rs/pull/949))
- Run test on aarch64-apple-darwin ([#947](https://github.com/dot-asm/cc-rs/pull/947))
- Merge pull request #944 from rust-lang/NobodyXu-patch-1
- move documentation from README.md to lib.rs ([#921](https://github.com/dot-asm/cc-rs/pull/921))
- Fix default deployment target behavior ([#943](https://github.com/dot-asm/cc-rs/pull/943))
- Fix typos. ([#942](https://github.com/dot-asm/cc-rs/pull/942))
- Remove dependency on pipe, unless parallel ([#940](https://github.com/dot-asm/cc-rs/pull/940))
- Add support for riscv32imac-esp-espidf ([#939](https://github.com/dot-asm/cc-rs/pull/939))
- add comment explaining gcc-shim. ([#935](https://github.com/dot-asm/cc-rs/pull/935))
- move Windows code into a module ([#924](https://github.com/dot-asm/cc-rs/pull/924))
- use full import path in tool module ([#933](https://github.com/dot-asm/cc-rs/pull/933))
- do not publish tests or gcc-shim with crate ([#934](https://github.com/dot-asm/cc-rs/pull/934))
- split Tool and ToolFamily to a new tool module ([#929](https://github.com/dot-asm/cc-rs/pull/929))
- split miscellaneous code into a new command_helpers module ([#931](https://github.com/dot-asm/cc-rs/pull/931))
- move cc-test & gen-windows-sys-binding into workspace ([#927](https://github.com/dot-asm/cc-rs/pull/927))
- move retain_unordered_mut function into parallel module ([#930](https://github.com/dot-asm/cc-rs/pull/930))
- add comment why tvOS CI job is separate from the matrix ([#928](https://github.com/dot-asm/cc-rs/pull/928))
- move src/os_pipe.rs to src/os_pipe/mod.rs ([#925](https://github.com/dot-asm/cc-rs/pull/925))
- do not publish cc-test crate ([#926](https://github.com/dot-asm/cc-rs/pull/926))
- move async_executor and job_token modules into new parallel module ([#923](https://github.com/dot-asm/cc-rs/pull/923))
- Use RUSTC_WRAPPER if no other wrapper is provided ([#918](https://github.com/dot-asm/cc-rs/pull/918))
- Add `cargo_warnings` config to control the use of the cargo warning instruction ([#917](https://github.com/dot-asm/cc-rs/pull/917))
- Add new compile_intermediates function. ([#914](https://github.com/dot-asm/cc-rs/pull/914))
- Merge pull request #910 from dpaoliello/arm64ec
- Link against libc++ on *-linux-ohos
- Add `--` for files in `try_expand`  (like in #514) ([#911](https://github.com/dot-asm/cc-rs/pull/911))
- Some clippy fixes ([#879](https://github.com/dot-asm/cc-rs/pull/879))
- Fix unconditional cargo metadata printing on flag support check ([#908](https://github.com/dot-asm/cc-rs/pull/908))
- Fix Apple deployment version floor when linking C++ ([#901](https://github.com/dot-asm/cc-rs/pull/901))
- Merge pull request #854 from aminya/directory-path
- Release cc v1.0.84 ([#898](https://github.com/dot-asm/cc-rs/pull/898))
- added a function to remove flags ([#885](https://github.com/dot-asm/cc-rs/pull/885))
- Vendor jobserver impl and rm thread spawning in parallel compile_objects ([#889](https://github.com/dot-asm/cc-rs/pull/889))
- Disable msrv checking on macos-latest
- Bump MSRV to 1.53.0 and re-enable macos MSRV check
- Fix msrv CI: Check for `--all-features` ([#890](https://github.com/dot-asm/cc-rs/pull/890))
- Pass -Wno-unused-command-line-argument to clang in `is_flag_supported` ([#886](https://github.com/dot-asm/cc-rs/pull/886))
- Merge pull request #863 from rust-lang/dependabot/github_actions/actions/checkout-4
- Add a TODO for `retain_unordered_mut`
- Fix MSRV: Remove use of `Vec::retain_mut`
- Merge pull request #878 from osiewicz/no_drops_on_implicit_job_token
- Fix `--target` getting passed twice to the Android NDK clang on Windows
- Detect msvc version if there is no default
- minimal maxosx deployment target is 10.9 when cpp ([#872](https://github.com/dot-asm/cc-rs/pull/872))
- Remove -fembed-bitcode flag ([#812](https://github.com/dot-asm/cc-rs/pull/812))
- detect clang/gcc using --version ([#709](https://github.com/dot-asm/cc-rs/pull/709))
- Fix xctoolchain AppleClang to corrrectly use -isysroot ([#703](https://github.com/dot-asm/cc-rs/pull/703))
- Add AppleTVOS support ([#704](https://github.com/dot-asm/cc-rs/pull/704))
- Be more specific about not passing -c to armasm[64].exe. ([#869](https://github.com/dot-asm/cc-rs/pull/869))
- Pass self.definitions to armasm[64].exe. ([#868](https://github.com/dot-asm/cc-rs/pull/868))
- Don't pass compiler flags to MSVC assembers. ([#867](https://github.com/dot-asm/cc-rs/pull/867))
- Use rustc's Apple deployment target defaults when available ([#848](https://github.com/dot-asm/cc-rs/pull/848))
- Separate source args with -- when compiling assembly with clang-cl ([#857](https://github.com/dot-asm/cc-rs/pull/857))
- Release version 1.0.83 ([#861](https://github.com/dot-asm/cc-rs/pull/861))
- Stop using feature "libc/std" ([#860](https://github.com/dot-asm/cc-rs/pull/860))
- Add method for specifying C/C++ standard version ([#761](https://github.com/dot-asm/cc-rs/pull/761))
- Release cc v1.0.82 ([#850](https://github.com/dot-asm/cc-rs/pull/850))
- Fix `Build::compile_objects` perf regression and deadlock ([#849](https://github.com/dot-asm/cc-rs/pull/849))
- Bump version to 1.0.81
- Fix `PrintThread`: Read stderr as bytes instead of str ([#842](https://github.com/dot-asm/cc-rs/pull/842))
- Bump version to 1.0.80 ([#834](https://github.com/dot-asm/cc-rs/pull/834))
- Handle `x86_64h-apple-darwin` target ([#840](https://github.com/dot-asm/cc-rs/pull/840))
- Vendor `windows-sys` crate ([#837](https://github.com/dot-asm/cc-rs/pull/837))
- Harmonize README.md with reality. ([#835](https://github.com/dot-asm/cc-rs/pull/835))
- Disambiguate Windows run-times when using clang to compile. ([#825](https://github.com/dot-asm/cc-rs/pull/825))
- Optimize `Build::compile_objects` on feature parallel ([#833](https://github.com/dot-asm/cc-rs/pull/833))
- Optimize `Build::env_cache`: Store `Option<Arc<str>>` as key ([#832](https://github.com/dot-asm/cc-rs/pull/832))
- Optimize `Build::get_out_dir`: Return `Cow<'_, Path>` ([#831](https://github.com/dot-asm/cc-rs/pull/831))
- Cleanup mod com, registry, setup_config and winapi ([#828](https://github.com/dot-asm/cc-rs/pull/828))
- Fix `Build::compile_objects` deadlock on parallel ([#829](https://github.com/dot-asm/cc-rs/pull/829))
- Use correct ABI on NetBSD/riscv64, and add target entry for same. ([#815](https://github.com/dot-asm/cc-rs/pull/815))
- Remove outdated doc about build parallelism ([#827](https://github.com/dot-asm/cc-rs/pull/827))
- Optimize `cc::Build::try_compile`: Reuse `PrintThread` ([#817](https://github.com/dot-asm/cc-rs/pull/817))
- Optimize `Error::new`: Avoid unnecessary heap alloc ([#823](https://github.com/dot-asm/cc-rs/pull/823))
- Optimize `Build::print`: Avoid unnecessary heap alloc ([#824](https://github.com/dot-asm/cc-rs/pull/824))
- Vendor dependency `os_pipe` ([#822](https://github.com/dot-asm/cc-rs/pull/822))
- Use gnu -o flag for obj out path instead of -Fo when using gcc & g++ on Windows ([#820](https://github.com/dot-asm/cc-rs/pull/820))
- add a function to populate flags from an arbitrary environment variable ([#818](https://github.com/dot-asm/cc-rs/pull/818))
- Merge pull request #780 from NobodyXu/optimize
- Be more stringent about handling Android NDK.
- Merge pull request #806 from NobodyXu/enable-dependabot-for-gha
- Enable dependabot for Github Action Workflows
- Link against libc++ on AIX
- Merge pull request #600 from SallySoul/change-getcpplib-doc
- Refine CUDA documentation.
- Add loongarch64 support
- Default to llvm-ar when compiling for wasm. ([#657](https://github.com/dot-asm/cc-rs/pull/657))
- Change approach for native and cross-compilation with clang++ on FreeBSD ([#794](https://github.com/dot-asm/cc-rs/pull/794))
- Prevent cloning on every `get_xxx()` call ([#793](https://github.com/dot-asm/cc-rs/pull/793))
- Clarify implementation limitations of funcs in doc comment
- Reword `push_cc_arg()` doc comments.
- Append `freebsd-version` to all --target=*-freebsd if executed on FreeBSD. ([#788](https://github.com/dot-asm/cc-rs/pull/788))
- Fix --target cflag on FreeBSD when compiling against clang ([#785](https://github.com/dot-asm/cc-rs/pull/785))
- Speedup `Build::clone`: Use `Arc` instead of `String`/`PathBuf`/`OsString` ([#782](https://github.com/dot-asm/cc-rs/pull/782))
- If a file path references a parent directory, transform it to ensure we keep inside the OUT_DIR ([#786](https://github.com/dot-asm/cc-rs/pull/786))
- Prioritize RUSTC_LINKER over target->cross-compile-prefix table. ([#767](https://github.com/dot-asm/cc-rs/pull/767))
- Make `windows_registry::VsVers` non_exhaustive ([#783](https://github.com/dot-asm/cc-rs/pull/783))
- Bump MSRV to 1.46.0 ([#781](https://github.com/dot-asm/cc-rs/pull/781))
- Prep release 1.0.79
- Fix `gcc-shim`, apply clippy warning & optimizations to it ([#777](https://github.com/dot-asm/cc-rs/pull/777))
- Add support for riscv32imc-esp-espidf ([#776](https://github.com/dot-asm/cc-rs/pull/776))
- Fix `Build::is_flag_supported`: Check exit status of the compiler ([#757](https://github.com/dot-asm/cc-rs/pull/757))
- Expose get_archiver and get_ranlib ([#763](https://github.com/dot-asm/cc-rs/pull/763))
- Fix "-arch arm64" flag for aarch64-ios-sim ([#759](https://github.com/dot-asm/cc-rs/pull/759))
- Update bitcode TODO
- Prep release 1.0.78
- Default to llvm-lib when using clang-cl in msvc environment.
- Map source absolute paths to OUT_DIR as relative. ([#684](https://github.com/dot-asm/cc-rs/pull/684))
- Update CUDA toolchain.
- Refine CUDA support.
- Allow to use clang++ with CUDA compiler.
- Only pass `.asm` files to masm
- Prep release 1.0.77
- Add `Build::asm_flag`
- Use a DWARF version consistent with rustc
- Prep release 1.0.76
- Don't separate files/opt when using msvc assembler
- Prep release 1.0.75
- Fix location of atlmfc directory on MSVC 15+
- Merge pull request #742 from nagisa/ml-debuginfo
- Prefer `-ar` to `-gcc-ar`
- Merge pull request #739 from thomcc/hkey-paranoia
- Adjust comment on HKEY_LOCAL_MACHINE
- Be much more defensive about how windows RegistryKeys are handled
- Prepare release 1.0.74
- Avoid `rerun-if-env-changed` on vars set by cargo for build scripts
- Default `emit_rerun_if_env_changed` to `true`
- Change getenv to only emit metadata once per var
- Run cargo fmt
- Add option to emit `rerun-if-env-changed` metadata
- Use specified compiler in is_flag_supported
- Continue to support binutils ar
- Add LLVM based MinGW targets
- Correctly infer ranlib/ar from cross-gcc
- Add support for riscv32imac-unknown-xous-elf
- Use RUSTC_LINKER's prefix as last resort for prefix_for_target().
- Remove support for to gh-pages
- Fix repository and homepage links in Cargo.toml
- Support native library modifiers (RFC 2951)
- Support clang >13.1 for aarch64-apple-ios-macabi and x86_64-apple-ios-macabi targets
- Use SDKROOT when set.
- force mingw32 test to Windows 2019.
- Merge pull request #677 from dot-asm/nvidia-pub-key-update
- Merge pull request #662 from vladimir-ea/watch_os
- Merge pull request #660 from atouchet/lic
- Merge pull request #514 from ncalexan/dash-dash
- Bump to 1.0.73
- Try to fix CI ([#659](https://github.com/dot-asm/cc-rs/pull/659))
- Fail fast and more helpfully on invalid `compile` argument ([#655](https://github.com/dot-asm/cc-rs/pull/655))
- Add guidance on what string to pass `compile` ([#658](https://github.com/dot-asm/cc-rs/pull/658))
- Fixes #625 Support getting Windows SDK from the environment ([#646](https://github.com/dot-asm/cc-rs/pull/646))
- Identify Visual Studio 2022 by MSBuild ([#648](https://github.com/dot-asm/cc-rs/pull/648))
- Support aarch64-pc-windows-gnu ([#645](https://github.com/dot-asm/cc-rs/pull/645))
- Support riscv64-unknown-openbsd ([#643](https://github.com/dot-asm/cc-rs/pull/643))
- Added arbitrary flag support to try_expand() ([#640](https://github.com/dot-asm/cc-rs/pull/640))
- Support riscv64gc-unknown-freebsd ([#642](https://github.com/dot-asm/cc-rs/pull/642))
- Add armv7 assembly for cc-test ([#629](https://github.com/dot-asm/cc-rs/pull/629))
- Bump to 1.0.72
- Add Visual Studio 17 (2022) ([#632](https://github.com/dot-asm/cc-rs/pull/632))
- Use riscv32-unknown-linux-gnu for target on clang ([#631](https://github.com/dot-asm/cc-rs/pull/631))
- Update CI config for main
- Fix armhf build for GCC-11 ([#627](https://github.com/dot-asm/cc-rs/pull/627))
- Bump to 1.0.71
- add prefixes for x86 to support cross-compiling from non-x86 targets ([#621](https://github.com/dot-asm/cc-rs/pull/621))
- Adds cachepot to the known wrappers set ([#626](https://github.com/dot-asm/cc-rs/pull/626))
- Add SOLID target support ([#609](https://github.com/dot-asm/cc-rs/pull/609))
- Support UEFI: fix object generation type for UEFI target. ([#623](https://github.com/dot-asm/cc-rs/pull/623))
- Bump to 1.0.70
- Address issues with new Catalyst/M1 simulator targets ([#614](https://github.com/dot-asm/cc-rs/pull/614))
- When spawn() fails, include the underlying error in the message. ([#613](https://github.com/dot-asm/cc-rs/pull/613))
- Improve CUDA support ([#612](https://github.com/dot-asm/cc-rs/pull/612))
- allow cachepot als alternative to sccache ([#599](https://github.com/dot-asm/cc-rs/pull/599))
- Bump to 1.0.69
- Use riscv64-unknown-linux-gnu for target on clang. ([#608](https://github.com/dot-asm/cc-rs/pull/608))
- Add `-arch` compiler flag on older macOS systems ([#607](https://github.com/dot-asm/cc-rs/pull/607))
- Probe for ARM64 MSBuild ([#605](https://github.com/dot-asm/cc-rs/pull/605))
- Bump to 1.0.68
- Attempt to use the current environment to find the tool ([#603](https://github.com/dot-asm/cc-rs/pull/603))
- Support finding Visual Studio instances using vswhere.exe ([#597](https://github.com/dot-asm/cc-rs/pull/597))
- Upgrade to GitHub-native Dependabot ([#598](https://github.com/dot-asm/cc-rs/pull/598))
- use the `eprintln` macro ([#591](https://github.com/dot-asm/cc-rs/pull/591))
- Fix typo in `atl_paths` ("atlfmc" --> "atlmfc") ([#592](https://github.com/dot-asm/cc-rs/pull/592))
- Use GNU AR for illumos ([#585](https://github.com/dot-asm/cc-rs/pull/585))
- Bump to 1.0.67
- Match abi and march settings for riscv on linux ([#583](https://github.com/dot-asm/cc-rs/pull/583))
- Pick version for iOS simulator target ([#582](https://github.com/dot-asm/cc-rs/pull/582))
- Fix a typo ([#581](https://github.com/dot-asm/cc-rs/pull/581))
- Replace -ios with apple-ios ([#579](https://github.com/dot-asm/cc-rs/pull/579))
- Avoid checking for overly-broad "cl" substring ([#578](https://github.com/dot-asm/cc-rs/pull/578))
- Use clang when cross-compiling to iOS targets ([#577](https://github.com/dot-asm/cc-rs/pull/577))
- Add an apt-get update
- Some Readme updates ([#575](https://github.com/dot-asm/cc-rs/pull/575))
- Bump to 1.0.66
- Call clang directly when cross-compiling from Windows to Android ([#572](https://github.com/dot-asm/cc-rs/pull/572))
- Split `s` out of the `ar` invocation ([#570](https://github.com/dot-asm/cc-rs/pull/570))
- Bump to 1.0.64
- Switch from the `r` option on `ar` to `q` ([#569](https://github.com/dot-asm/cc-rs/pull/569))
- Bump to 1.0.63
- progressive linking ([#564](https://github.com/dot-asm/cc-rs/pull/564))
- Document CXXSTDLIB and change the Android default ([#561](https://github.com/dot-asm/cc-rs/pull/561))
- Support mips(el)-unknown-linux-musl ([#562](https://github.com/dot-asm/cc-rs/pull/562))
- Bump to 1.0.62
- Show a better message when `xcrun` is missing
- add macos catalyst support ([#556](https://github.com/dot-asm/cc-rs/pull/556))
- exclude `.github` folder from publish ([#553](https://github.com/dot-asm/cc-rs/pull/553))
- Bump to 1.0.61
- Method to add multiple includes: build.includes(...) ([#550](https://github.com/dot-asm/cc-rs/pull/550))
- Bump to 1.0.60
- Apply Darwin target modifications for Clang as well ([#549](https://github.com/dot-asm/cc-rs/pull/549))
- Remove outdated notice ([#548](https://github.com/dot-asm/cc-rs/pull/548))
- use wr-cc for C file, use wr-c++ for CPP file ([#546](https://github.com/dot-asm/cc-rs/pull/546))
- Bump to 1.0.59
- Fix typo: s/compilier/compiler/ ([#544](https://github.com/dot-asm/cc-rs/pull/544))
- Detect standalone android compiler with regex ([#539](https://github.com/dot-asm/cc-rs/pull/539))
- handle wrong SDKROOT for macos->macos build ([#537](https://github.com/dot-asm/cc-rs/pull/537))
- Add arm64e ABI support. ([#534](https://github.com/dot-asm/cc-rs/pull/534))
- Add support for hexagon-unknown-linux-musl-clang ([#533](https://github.com/dot-asm/cc-rs/pull/533))
- Bump to 1.0.58
- Always specify architecture for x86_64 / aarch64 Darwin ([#527](https://github.com/dot-asm/cc-rs/pull/527))
- use push_cc_arg for options add ([#528](https://github.com/dot-asm/cc-rs/pull/528))
- Add -nologo command-line option to Microsoft assembler. ([#525](https://github.com/dot-asm/cc-rs/pull/525))
- Bump to 1.0.57
- Add the host architecture Windows 10 SDK bin directory to the PATH, not the target. ([#524](https://github.com/dot-asm/cc-rs/pull/524))
- Bump to 1.0.56
- Don't set definition flags for MSVC ARM targets ([#518](https://github.com/dot-asm/cc-rs/pull/518))
- Use a search list to find a compatible toolchain ([#521](https://github.com/dot-asm/cc-rs/pull/521))
- Bump to 1.0.55
- Use x86 hosted msvc on arm64 windows ([#522](https://github.com/dot-asm/cc-rs/pull/522))
- Add cross-compiler prefix for armv7 without hf ([#515](https://github.com/dot-asm/cc-rs/pull/515))
- Name wrangling c++ caveat in Readme ([#511](https://github.com/dot-asm/cc-rs/pull/511))
- Add missing README syntax highlighting ([#509](https://github.com/dot-asm/cc-rs/pull/509))
- Fix for multi-component Android compiler paths ([#507](https://github.com/dot-asm/cc-rs/pull/507))
- Bump to 1.0.54
- Find prefixed AR when cross compiling. ([#502](https://github.com/dot-asm/cc-rs/pull/502))
- vs2019 preview search path added ([#501](https://github.com/dot-asm/cc-rs/pull/501))
- In windows_registry::find_tool, set the ToolFamily to Msvc ([#499](https://github.com/dot-asm/cc-rs/pull/499))
- Bump to 1.0.53
- Implement autodetection for default compiler from NDK ([#495](https://github.com/dot-asm/cc-rs/pull/495))
- Check for the right compiler we're testing
- Bump to 1.0.51
- Switch to `output()` from `spawn()` to avoid zombies
- Fix Android clang compiler path when building with Windows host ([#489](https://github.com/dot-asm/cc-rs/pull/489))
- use "gcc" by default on illumos systems ([#487](https://github.com/dot-asm/cc-rs/pull/487))
- Add tool autodetection for armv7a targets ([#479](https://github.com/dot-asm/cc-rs/pull/479))
- Use gnu -o flag for obj out path instead of -Fo when using clang & clang++ on Windows ([#483](https://github.com/dot-asm/cc-rs/pull/483))
- Do not set the -fPIC flag for Windows targets when using clang for CXX builds ([#481](https://github.com/dot-asm/cc-rs/pull/481))
- Add 'armv5te-unknown-linux-musleabi' target support ([#478](https://github.com/dot-asm/cc-rs/pull/478))
- Detect and use sccache by introspecting RUSTC_WRAPPER ([#475](https://github.com/dot-asm/cc-rs/pull/475))
- Update CI installation of Rust on macos
- Clear CFLAGS and CXXFLAGS before tests ([#472](https://github.com/dot-asm/cc-rs/pull/472))
- disable pic for bare metal by default ([#470](https://github.com/dot-asm/cc-rs/pull/470))
- Use medany model ([#467](https://github.com/dot-asm/cc-rs/pull/467))
- Bump to 1.0.50
- Don't depend on `num_cpus` for parallelism
- Bump to 1.0.49
- Add cross prefix for riscv64gc-unknown-linux-gnu => riscv64-linux-gnu ([#465](https://github.com/dot-asm/cc-rs/pull/465))
- Implement std::error::Error for Error ([#464](https://github.com/dot-asm/cc-rs/pull/464))
- Enable -fPIC on non-bare-metal RISC-V ([#461](https://github.com/dot-asm/cc-rs/pull/461))
- Bump to 1.0.48
- Default to double-float ABI on RISC-V Linux ([#460](https://github.com/dot-asm/cc-rs/pull/460))
- Migrate tests to `tempfile` from deprecated `tempdir` ([#457](https://github.com/dot-asm/cc-rs/pull/457))
- Detect clang cl driver mode ([#455](https://github.com/dot-asm/cc-rs/pull/455))
- More fixes for GitHub changes
- Fix Github Actions for recent system changes
- Bump to 1.0.46
- Added public function to add flags to archiver
- Fix typo in lib.rs doc
- add mechanism for forcing frame pointer.
- Fix Windows CI for now
- Bump to 1.0.45
- More jobserver rejiggering
- Bump to 1.0.44
- Fix acquire release typo
- Bump to 1.0.43
- Account for the jobserver implicit token
- Migrate CI to GitHub Actions
- Bump to 1.0.42
- Update to the 2018 edition
- Bump MSRV to 1.31.0
- Rejigger parallel compilation support
- Pass `/Brepro` on MSVC by default ([#437](https://github.com/dot-asm/cc-rs/pull/437))
- Set ZERO_AR_DATE for archiver invocations
- Bump to 1.0.41
- Add `no_default_flags` method ([#435](https://github.com/dot-asm/cc-rs/pull/435))
- Fix a build warning on Windows
- Bump to 1.0.40
- Fix a bad merge typo
- Bump to 1.0.39
- Add CUDA support for MSVC ([#426](https://github.com/dot-asm/cc-rs/pull/426))
- Merge pull request #433 from turboladen/feature/config-ios-version-min
- use wr-c++ instead of vx-cxx
- Merge pull request #430 from laanwj/2019_08_rv_nopic
- Set ABI correctly for 32-bit targets
- Add RISC-V support
- Bump to 1.0.38
- Remove `--test-threads 1` on Azure
- Don't hard link the gcc-shim executable on macOS
- Move env var tests into separate modules
- Improve error reporting
- use vx-cxx
- Add support for vxWorks using vx-cc
- Correct documentation for `Build::debug`
- Merge pull request #398 from chouquette/add_uwp
- Hopefully last fix for CI...
- Don't self-update existing rustup
- Fix some bash syntax
- Pray bash works
- Ok pwsh.exe isn't on the 2015 image
- Try running a different powershell
- Fix scripts for MSVC
- Fix scripts for MSVC
- Still install rustup on older Windows images...
- Don't self-update on Windows
- Attempt to fix CI
- Add find msbuild vs16 logic.
- Merge pull request #410 from ogoffart/master
- Merge pull request #411 from spl/tempdir-in
- Create temp dir in same dir as gcc-shim
- Merge pull request #406 from spl/test-path-fn
- Localize path split and join to one function
- Bump to 1.0.37
- Recognize the "wasm32-wasi" target tuple.
- Bump to 1.0.36
- Fix build with Rust 1.16.0.
- Run the `Minimum Rust` CI job on Windows and fix Linux.
- Run rustfmt
- Tweak error printing
- Add support of MIPS r6, o32 and n64
- Bump to 1.0.35
- Make detection more robust
- Autodetect VS 2019
- Run rustfmt
- More typos...
- Install 32-bit libc++
- Install gcc-multilib for 32-bit compiles on Linux
- Actually execute tests on Linux
- Bump to 1.0.34
- Preserve env vars from `windows_registry` in `lib.exe` detection
- Remove badges from Cargo.toml
- Bump to 1.0.33
- Merge pull request #387 from froydnj/lib-alternatives-on-windows
- Set up CI with Azure Pipelines
- Bump to 1.0.32
- Minimally support Visual Studio 2019.
- use clang for wasm32-unknown-unknown target
- Bump to 1.0.31
- Disable automatic turning off defaults
- Use `self.getenv` instead of `env::var`
- Fix typo in readme.
- Bump to 1.0.30
- Add wasi target definition
- Move addition of default flags to own method
- Insert CFLAGS after default flags; addresses #376
- Disable default args when they may conflict with CFLAGS/CXXFLAGS
- Add enviroment variable to disable default flags: `CRATE_CC_NO_DEFAULTS`
- Don't set duplicate/conflicting optimization flags
- Bump to 1.0.29
- Use --target with non x86/x86_64 clang-cl targets
- Crate category
- Update travis
- Update README
- Update travis config
- Bump to 1.0.28
- Allow(deprecated) to avoid needlessly breaking the Rust ecosystem
- Revert "Update minimum version"
- Revert "Replace future deprecated call"
- Bump to 1.0.27
- Fix a deprecation on Windows
- Update minimum version
- Replace future deprecated call
- Add the Armv8-M targets
- Merge pull request #361 from piersfinlayson/master
- Correctly handle both hard and soft floating point
- Generate valid sintructions on ARMv6 (see rust-lang/rust issue #50583)
- Remove readme testing
- exclude CI files
- Merge pull request #331 from nmlgc/master
- Fall back on finding devenv and MSBuild via the previous registry-based method
- find_tool_in_vs15_path(): Filter nonexistent executables
- Find devenv and MSBuild via SetupConfiguration rather than registry keys
- Split MSVC 15 instance iterator retrieval into a separate function
- Bump to 1.0.18
- Pass cc_wrapper_args to all compiler invocations
- Stray println
- special case for devenv.exe
- Set explicit host when checking supported flags.
- Don't override host when checking supported flags.
- Bump to 1.0.17
- Merge pull request #321 from hsivonen/neon
- Bump to 1.0.16
- Add new cppwinrt folder to Windows 10 SDK includes.
- Bump to 1.0.15
- Fix i586-pc-windows-msvc on clang-cl
- Version 1.0.14
- Pass -m32 and -m64 for clang-cl
- make extra_warning_flags return an Option
- bump minor version
- add option to enable/disable -Wextra on gcc/clang
- Remove rustfmt builder
- Bump to 1.0.12
- Don't classify `clang` as MSVC
- Bump to 1.0.11
- Run `cargo fmt`
- Fix compile on stable
- Set env vars for clang-cl invocations
- Detect `clang-cl` correctly
- Bump to 1.0.10
- Allow overwriting the default cpp_link_stdlib
- Pass -static depending on crt-static on linux too.
- Bump to 1.0.9
- cargo fmt
- Support CC env vars like `CC='cc -foo'`
- Bump to 1.0.8
- rustfmt
- Merge pull request #306 from jdm/parallel-supported-flags2
- Extend critical section to encompass full supported flags check.
- Msvc needs /O1 (which implies /Os) to generate smallest binaries
- Run `cargo fmt`
- Handle paths to ccache-like wrappers
- Add icecc to ccache-like whitelist
- Bump to 1.0.7
- Trim spaces around env vars
- Bump to 1.0.6
- Some tweaks for iOS
- Bump to 1.0.5
- Pass lib.exe arguments though a file when the arg list is too long.
- Add sparc-unknown-linux-gnu cross-compile target
- Add powerpc-unknown-linux-gnuspe cross-compile target
- Merge pull request #285 from ratake/master
- Fix compiling C++ libraries on iOS
- Simplify the parallel Result with collect()
- Only build the threadpool if customized
- Update to rayon 1.0
- Merge pull request #282 from Mrmaxmeier/cache-is_flag_supported
- document new is_flag_supported behaviour
- reuse result of previous is_flag_supported-calls
- Doc
- Make is_flag_supported public
- Don't treat 'x86_64-unknown-cloudabi-cc' as being MSVC.
- Add support for {armv4t,armv5te}-unknown-linux-gnueabi
- Pick the right compiler for CloudABI.
- Don't export `Object` for now
- Merge remote-tracking branch 'upstream/master' into peterhj-cuda
- Cleanup after merging with latest master.
- Merge remote-tracking branch 'origin/master' into peterhj-cuda-devel
- Clarify wording of license information in README.
- Fix a typo in the docs
- Bump to 1.0.3
- tests for no-ccache environments
- rename cc to cc_wrapper
- actually using ccache for compiler command
- merged
- env_tool returning additional param for ccache case
- Separated cflags and command args
- Add a homepage to Cargo.toml
- Bump to 1.0.1
- Add -mx32 to x86_64-unknown-linux-gnux32
- Fix badges
- Add custom flags after -Wall
- Use `cmd /c emar.bat` on Windows emscripten
- Merge pull request #244 from makotokato/android-thumb2
- Update Travis/AppVeyor configs
- Note that this is a rename crate
- Bump to 1.0.0
- Fix tests from rename
- Rename the crate to `cc`
- Bump to 0.3.54
- Only pass -Oz to clang
- Execute `cmd` directory for bat scripts on Windows
- Add sccache to the whitelist of ccache-like compilers
- Add tests for flag_if_supported in C++ mode.
- Fix flag_if_supported for C++ sources.
- Defer flag checks until compile() is called.
- Switch MSVC from /Wall to /W4
- Don't capitalize library names
- Bump to 0.3.53
- Correct lookup of `DEBUG`
- Bump to 0.3.52
- Add useful derives for `VsVers`
- Explain emitted cargo metadata
- Fix non-delimited library names
- Merge branch 'try-refactor' of https://github.com/marco9999/gcc-rs
- Add Config as alias for Build
- Rename `Config` type to `Build`
- Merge branch 'into-option-str' of https://github.com/laumann/gcc-rs
- Merge pull request #229 from opilar/bugfix/debug-env
- Merge pull request #228 from opilar/feature/common-std-libs
- Merge pull request #216 from opilar/feature/warning-control
- Merge pull request #207 from opilar/feature/link-set-stdlib-examples
- Fix examples
- cpp_link_stdlib/cpp_set_stdlib examples
- Merge pull request #203 from opilar/feature/tool-derive
- Merge pull request #201 from opilar/feature/shared-static-flag-doc
- Merge pull request #202 from opilar/feature/include-define-flag-docs
- Tests compilation
- Include/define/flag docs
- Minor style updates
- bump rayon to 0.8
- Bump to 0.3.51
- Merge pull request #134 from jakllsch/netbsd
- Fix nmake tests
- add shared_flag and static_flag
- Bump to 0.3.50
- Merge pull request #166 from brson/vs2017
- Only add the 'host dylib path' to the MSVC 2017 PATH
- Bump to 0.3.49
- Merge pull request #164 from brson/vs2017
- Fix MSVC 2017 cross-compilation
- Bump to 0.3.48
- Add forwards compat with `VsVers`
- Merge pull request #163 from brson/vs2017
- Update msbuild discovery for 2017
- Be more precise about MSVC names
- Add MSVC 2017 detection
- Bump to 0.3.46
- Explicitly set static crt
- Fixing emscripten on windows to use the right files.
- Fix confusion with uclibc triplets
- Merge pull request #152 from nodakai/patch-1
- Support for the FRC target
- Merge pull request #146 from neosilky/clippy-fixes
- Remove reference in favour for dereferencing variable
- Switch to better fallback methods
- Remove .ok() call as .expect() can be called on Result
- Switch single string constant to char constant
- Remove explicit return statements
- Update to rayon 0.7
- Merge pull request #148 from pietro/android-arm-flags
- Attempt to fix CI
- Bump to 0.3.45
- Don't drop stdout on the floor by default
- Bump to 0.3.44
- Wait for child threads to finish
- add sparcv9-sun-solaris cross-compile target
- Default to gnu compilers on Solaris
- Update pic docs
- Fix tests
- Bump to 0.3.43
- Pass -fPIC on 32-bit
- Fix suprious warning for cpp
- Update README; `cargo build -jN` will set/override $NUM_JOBS for you.
- Update metadata
- Bump to 0.3.42
- Add a method to macro-expand source files
- Fix nits
- Add support for clang
- Use arm toolchain for armv7 on Android
- Upgrade to rayon 0.6
- Bump to 0.3.41
- Ran rustfmt
- rayon 0.5
- No install step on 1.6.0
- Fix compat with older Rust
- Bump to 0.3.40
- Add -melf_i386 to i686 musl
- Add toolchain prefix for sparc64-unknown-netbsd target
- Bump to 0.3.39
- Pass /MT for crt-static on MSVC
- Revert emitting atls.lib cargo metadata
- Add ATL/MFC workaround for linker
- Add ATL/MFC detection for MSVC
- Specify FPU for thumv7em-none-eabihf
- use armv6s-m instead of armv6-m
- Really fix nightly tests
- Fix tests on nightly
- Update travis token
- Add default cpp_link_stdlib for FreeBSD target
- Don't pass SAFESEH to cl.exe
- Bump to 0.3.38
- Don't pass `u` to `ar`
- Trim right - from CROSS_COMPILE
- More flags for armv7 android
- Bump to 0.3.37
- Add support for i586 msvc
- Bump to 0.3.36
- Add mips64 target prefixes
- Merge pull request #106 from jdub/cross-compile
- CROSS_COMPILE is explicit, use it before fallbacks
- Support CROSS_COMPILE environment variable
- add prefix and flags for Cortex-M targets
- Fix build with opt-levels s/z (issue #102)
- Add toolchain prefix mappings for s390x
- Use correct ar for emscripten
- Support emscripten
- Support 'z' and 's' optimization levels
- Add i686 musl cross target
- Add some NetBSD target to toolchain prefix mappings
- sort lookup table of target to prefix mappings
- Bump to 0.3.35
- Move output directory creation out of parallel code
- Add weight to the gcc parallel tasks
- Bump to 0.3.33
- Fix travis config
- Clarify the name in the README
- Add a note about parallel compilation in the README
- Move rayon to an off-by-default feature
- Fix travis testing of README
- Configure rayon according to NUM_JOBS
- Merge pull request #92 from nipunn1313/rayon
- Delete existing archives before assembling them
- Reduce number of scopes a bit, don't require UTF-8
- Emit cargo warnings when compilers emit warnings
- Bump to 0.3.32
- Fix relying on Windows 8/8.1 SDKs
- Work when input files are absolute paths
- Pass -march=i686 for i686 Linux
- Bump to 0.3.31
- Ensure the `rc` tool works
- Bump to 0.3.30
- Remove stray `pub`
- Bump to 0.3.29
- Update MSVC probing logic
- Use `Path::exists`
- Bump to 0.3.28
- Pass -m32/-march=pentium for i586 linux
- Pass /safeseh and /arch:IA32 for i586-pc-windows-msvc
- Bump to 0.3.27
- Use rustup to install extra targets
- Specially recognize ccache/distcc
- Touch up the README slightly
- Add support for ARM MUSL cross-compilers.
- Bump to 0.3.26
- Fix a typo
- Try to set Platform for MSBuild
- Add MSBuild executable name
- Add support for finding msbuild
- Bump to 0.3.25
- Force arm-*-*-gnueabihf targets to armv6
- Add support for MIPS little-endian targets
- Bump to 0.3.24
- Apparently safeseh is lowercase to ml.exe ...
- Pass SAFESEH to i686 MSVC tools
- Bump to 0.3.23
- Drop winapi/advapi32 deps
- Remove out-of-date link in README.md
- Bump to 0.3.22
- Merge pull request #70 from peterhj/peterhj-nvcc
- Preliminary support for building CUDA C files with nvcc.
- Pass -m64 for powerpc64
- Add default compilers for powerpc linux
- Switch back from stable -> 1.5.0
- Update travis script
- Move travis from 1.0.0 -> stable
- Add `pic` method to override default emission of `-fPIC`
- Bump to 0.3.21
- Don't include the colon in /Fo for MSVC
- Fix typos
- Bump to 0.3.20
- Handle rumprun-netbsd for cross compiles
- Use MD when compiling C files
- Fix version check
- Update CI
- Yet another attempt to fix nightly CI
- Another attempt at fixing nightly
- Try to fix nightly builds
- Fall back to copy if hard linking fails
- Clean whitespace
- Bump to 0.3.19
- Pass -static when compiling for MUSL
- Bump to 0.3.18
- Add .exe on the end of the windows gcc
- Test both GNU targets on appveyor
- Bump to 0.3.17
- Attempt to use a cross compiler by default
- Don't print anything if cargo_metadata is false
- Add the ability to learn about the compiler being run
- Bump to 0.3.16
- .ok.expect() so it compiles in older versions
- don't println! on hard-link failure
- If hard-linking fails, try to copy (in assemble())
- Bump to 0.3.15
- Inform clang when we're building for iOS
- Bump to 0.3.14
- Don't need -fPIC on windows-gnu
- Update README.md
- Tweak some style here and there
- Rename link() to cargo_metadata() and cover all the cargo:… flags.
- Actually add the rust side of the test
- Test whether optional linking works
- Add an option to disabled automatic linking of the produced binary.
- Add the ability to configure an archiver as well
- Add the option to specify a compiler
- Try fixing CI on appveyor
- Add the ability to at least somewhat test weird platforms
- Re-enable OSX builds
- Disable OSX builds while they're tested
- Update lib.rs
- Update GH_TOKEN env var
- Bump to 0.3.13
- Add some more UCRT include paths
- Bump to 0.3.12
- Don't pass the -mwin32 flag by default on Windows
- Use the registry for the Windows Kits 10.0 folder
- Bump to 0.3.11
- Try to detect the Universal CRT on MSVC installs
- Try to fix asm syntax for msvc 32-bit
- Add 32-bit MSVC assembly
- Test on 32-bit msvc
- Bump to 0.3.10
- Start probing for MSVC tools
- Fix compile
- Test gcc-test with --release as well
- Avoid usage of cfg!
- Use 0.3 in docs
- Bump to 0.3.9
- Fix 32-bit C++ travis
- Add a C++ test
- Add tests for define and include
- Add tests for compiling assembly
- Fix CI
- Test 32-bit on travis
- Add a crate to test gcc
- Compile '*.asm' files on MSVC with ml/ml64
- Touch up the README
- Merge pull request #49 from jdub/debug
- Perform debug builds under debug profile
- Test on MinGW and MSVC
- Bump to 0.3.8
- re-add support for -stdlib
- simplify cpp stdlib handling, don't use -stdlib=
- Bump to 0.3.7
- Pass /MD on windows
- Create foo.lib files for MSVC
- Bump to 0.3.6
- Don't pass -stdlib by default on MSVC
- Add support for MSVC
- Test on rust 1.0.0, nightly, and beta
- Allow choosing which C++ standard library to use
- Add appveyor build status to README
- Bump to 0.3.5
- Link to https
- Merge pull request #37 from vadimcn/windows-help
- Fix up Windows Notes.
- Add appveyor config
- Bump to 0.3.4
- Merge pull request #31 from KokaKiwi/gxx
- Link C++ standard library dynamically.
- Replace function pointers with direct calls.
- Add C++ library compilation support.
- Bump to 0.3.3
- Bump to 0.3.2
- Upgrade to rustc 1.0.0-dev (e98e39133 2015-03-20) (built 2015-03-20)
- Use new dedicated metadata for Cargo
- Update to rust master
- Fixup some warnings
- Update to cargo master
- Add a root doc url
- Reduce features in use
- Fix looking at CFLAGS
- Move off std::old_io
- fixed aarch64 compilation
- Bump to 0.2.1
- Fix README example
- Move to a builder-style interface
- Move to var_string
- Add a build-dependencies keyword
- Add some feature gates
- Bump to 0.1.7
- Fix README and add travis config
- Bump to 0.1.6
- Update to new compiler flag syntax
- Merge pull request #22 from alexcrichton/update
- Bump to 0.1.4
- Format Show and String split
- Put all emitted -L paths into the native path only
- Additional archs for iOS
- Add -mwin32 on Windows targets
- Support for additional flags for gcc
- Set default gcc/ar based on target when compiling android target.
- Bump version number
- Remove uneeded feature
- Don't fail when all envs are unset. Also log envs checked.
- Merge pull request #11 from SerhoLiu/fix-readme-link
- Fix README link failed
- Support use of namespaced environment variables based on TARGET and HOST
- Tweak wording around gcc on windows
- Add Windows notes
- Bump to 0.1.0
- Improve error messages slightly around running commands
- Add some metadata and bump the version number
- Support for iOS compilation
- Allow specification of additional objects to link in
- Be sure to link statically against archives assembled
- Create output directory if it doesn't exist
- Add possibility to pass -D flags
- Add passing include directories when compiling
- Be sure to compile with -fPIC
- Add a README/licenses
- Initial commit
- Initial commit

## [1.4.5](https://github.com/rust-lang/cc-rs/compare/cc-v1.4.4...cc-v1.4.5) - 2026-09-04

### Fixed

- probe flag support without OUT_DIR via tempfile ([#1875](https://github.com/rust-lang/cc-rs/pull/1875))

### Other

- simplify conditional logic using `then` method ([#1860](https://github.com/rust-lang/cc-rs/pull/1860))

### Fixed

- Probe flag support without `OUT_DIR` via tempfile, so `flag_if_supported` no longer silently drops flags outside Cargo build scripts ([#1875](https://github.com/rust-lang/cc-rs/pull/1875))

## [1.4.4](https://github.com/rust-lang/cc-rs/compare/cc-v1.4.3...cc-v1.4.4) - 2026-08-21

### Fixed

- honour `Build::env` overrides in Android llvm-ar probe ([#1868](https://github.com/rust-lang/cc-rs/pull/1868))
- honour `Build::env` overrides in flag support and compiler family detection probes ([#1866](https://github.com/rust-lang/cc-rs/pull/1866))

## [1.4.3](https://github.com/rust-lang/cc-rs/compare/cc-v1.4.2...cc-v1.4.3) - 2026-08-14

### Other

- Update MSRV to 1.65 ([#1834](https://github.com/rust-lang/cc-rs/pull/1834))
- Regenerate target info ([#1848](https://github.com/rust-lang/cc-rs/pull/1848))

## [1.4.2](https://github.com/rust-lang/cc-rs/compare/cc-v1.4.1...cc-v1.4.2) - 2026-08-08

### Fixed

- Infer NEON, not VFPv4, from `neon` in the target name ([#1843](https://github.com/rust-lang/cc-rs/pull/1843))
- do not emit `-mno-omit-leaf-frame-pointer` if unsupported ([#1845](https://github.com/rust-lang/cc-rs/pull/1845))

## [1.4.1](https://github.com/rust-lang/cc-rs/compare/cc-v1.4.0...cc-v1.4.1) - 2026-08-07

### Fixed

- Fix `-Cforce-frame-pointers`'s corresponding `CFLAGS` ([#1814](https://github.com/rust-lang/cc-rs/pull/1814))
- Fix parsing of thumbv7a-vex-v5 ([#1840](https://github.com/rust-lang/cc-rs/pull/1840))

### Other

- Regenerate target info ([#1839](https://github.com/rust-lang/cc-rs/pull/1839))
- Add `aarch64_be` to `prefix_for_target` ([#1835](https://github.com/rust-lang/cc-rs/pull/1835))
- Use lp64d ABI for Managarm riscv64 ([#1829](https://github.com/rust-lang/cc-rs/pull/1829))
- Make cc work on Motor OS ([#1822](https://github.com/rust-lang/cc-rs/pull/1822))
- Update edition to 2021 ([#1811](https://github.com/rust-lang/cc-rs/pull/1811))
- Update MSRV to 1.64 ([#1808](https://github.com/rust-lang/cc-rs/pull/1808))

## [1.4.0](https://github.com/rust-lang/cc-rs/compare/cc-v1.3.0...cc-v1.4.0) - 2026-07-24

### Added

- support trim paths with clang-cl.exe ([#1799](https://github.com/rust-lang/cc-rs/pull/1799))

## [1.3.0](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.67...cc-v1.3.0) - 2026-07-18

### Added

- inherit path remap rules from cargo trim-paths ([#1794](https://github.com/rust-lang/cc-rs/pull/1794))

## [1.2.67](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.66...cc-v1.2.67) - 2026-07-11

### Other

- Fix clippy warning ([#1788](https://github.com/rust-lang/cc-rs/pull/1788))
- Regenerate target info ([#1785](https://github.com/rust-lang/cc-rs/pull/1785))
- Add support for `aarch64-unknown-linux-pauthtest` target ([#1713](https://github.com/rust-lang/cc-rs/pull/1713))
- Fix nightly compilation error ([#1783](https://github.com/rust-lang/cc-rs/pull/1783))

## [1.2.66](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.65...cc-v1.2.66) - 2026-07-05

### Other

- Fix target parsing for aarch64-unknown-linux-pauthtest ([#1779](https://github.com/rust-lang/cc-rs/pull/1779))
- Support new QNX targets ([#1775](https://github.com/rust-lang/cc-rs/pull/1775))
- Add kache to the supported compiler wrappers ([#1770](https://github.com/rust-lang/cc-rs/pull/1770))

## [1.2.65](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.64...cc-v1.2.65) - 2026-06-19

### Other

- Regenerate target info ([#1763](https://github.com/rust-lang/cc-rs/pull/1763))

## [1.2.64](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.63...cc-v1.2.64) - 2026-06-12

### Other

- Add more bare-metal 32-bit Arm support ([#1753](https://github.com/rust-lang/cc-rs/pull/1753))
- Remove unnecessary clone ([#1748](https://github.com/rust-lang/cc-rs/pull/1748))
- Add default compiler prefixes for thumbv7a/thumbv7r/thumbv8r bare-metal targets ([#1742](https://github.com/rust-lang/cc-rs/pull/1742))

## [1.2.63](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.62...cc-v1.2.63) - 2026-05-29

### Other

- Update shlex requirement from 1.3.0 to 2.0.1 ([#1736](https://github.com/rust-lang/cc-rs/pull/1736))

## [1.2.62](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.61...cc-v1.2.62) - 2026-05-08

### Other

- Regenerate target info ([#1721](https://github.com/rust-lang/cc-rs/pull/1721))
- Allow exceptions on wasm platforms ([#1714](https://github.com/rust-lang/cc-rs/pull/1714))
- Add relibc env ([#1710](https://github.com/rust-lang/cc-rs/pull/1710))
- recognize sh4 architecture in parse_arch() ([#1712](https://github.com/rust-lang/cc-rs/pull/1712))

## [1.2.61](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.60...cc-v1.2.61) - 2026-04-24

### Other

- fix `OutputKind::Capture` documentation ([#1705](https://github.com/rust-lang/cc-rs/pull/1705))

## [1.2.60](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.59...cc-v1.2.60) - 2026-04-10

### Fixed

- *(ar)* suppress warnings from `D` modifier probe ([#1700](https://github.com/rust-lang/cc-rs/pull/1700))

## [1.2.59](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.58...cc-v1.2.59) - 2026-04-03

### Fixed

- *(ar)* deterministic archives with `D` modifier ([#1697](https://github.com/rust-lang/cc-rs/pull/1697))

### Other

- Regenerate target info ([#1698](https://github.com/rust-lang/cc-rs/pull/1698))
- Fix target abi parsing for sanitiser targets ([#1695](https://github.com/rust-lang/cc-rs/pull/1695))

## [1.2.58](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.57...cc-v1.2.58) - 2026-03-27

### Other

- Update Compile-time Requirements to add info about clang-cl.exe ([#1693](https://github.com/rust-lang/cc-rs/pull/1693))

## [1.2.57](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.56...cc-v1.2.57) - 2026-03-13

### Other

- Size archiver batches according to argument length not argument count ([#1689](https://github.com/rust-lang/cc-rs/pull/1689))
- Added `Build::env` for setting environment variables of compiler invocations and other child processes ([#1656](https://github.com/rust-lang/cc-rs/pull/1656) [#1682](https://github.com/rust-lang/cc-rs/pull/1682))

## [1.2.56](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.55...cc-v1.2.56) - 2026-02-13

### Other

- Regenerate target info ([#1676](https://github.com/rust-lang/cc-rs/pull/1676))
- Fix `clang-cl` target when cross-compiling ([#1670](https://github.com/rust-lang/cc-rs/pull/1670))

## [1.2.55](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.54...cc-v1.2.55) - 2026-01-30

### Other

- Regenerate target info ([#1667](https://github.com/rust-lang/cc-rs/pull/1667))
- Fix RUSTFLAGS typo in test-linker-plugin-lto ([#1665](https://github.com/rust-lang/cc-rs/pull/1665))
- Disable PIC for armv7-sony-vita-newlibeabihf ([#1664](https://github.com/rust-lang/cc-rs/pull/1664))

## [1.2.54](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.53...cc-v1.2.54) - 2026-01-23

### Other

- Fix x86_64-unknown-linux-gnuasan parsing ([#1661](https://github.com/rust-lang/cc-rs/pull/1661))
- Regenerate target info ([#1660](https://github.com/rust-lang/cc-rs/pull/1660))

## [1.2.53](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.52...cc-v1.2.53) - 2026-01-16

### Other

- Add missing RISC-V targets ([#1657](https://github.com/rust-lang/cc-rs/pull/1657))

## [1.2.52](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.51...cc-v1.2.52) - 2026-01-09

### Other

- Fix contradictory doc for CC compiler in crate doc ([#1650](https://github.com/rust-lang/cc-rs/pull/1650))
- Have CUDA compilaion check for sbsa-linux when targeting aarch64. ([#1647](https://github.com/rust-lang/cc-rs/pull/1647))
- Update link for -Cdwarf-version; Remove -Z (stabilized in 1.88) ([#1648](https://github.com/rust-lang/cc-rs/pull/1648))
- Fix Build::env_tool to check for .exe on windows ([#1646](https://github.com/rust-lang/cc-rs/pull/1646))

## [1.2.51](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.50...cc-v1.2.51) - 2025-12-26

### Other

- Regenerate target info ([#1642](https://github.com/rust-lang/cc-rs/pull/1642))
- Update Readmes ([#1641](https://github.com/rust-lang/cc-rs/pull/1641))

## [1.2.50](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.49...cc-v1.2.50) - 2025-12-19

### Other

- Add tests for `OUT_DIR` escape for '..' file paths (#1631)
- Fix #283: Make warnings(false) actually suppress compiler warnings ([#1633](https://github.com/rust-lang/cc-rs/pull/1633))

## [1.2.49](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.48...cc-v1.2.49) - 2025-12-06

### Other

- Fix run_output to prevent infinite blocking ([#1627](https://github.com/rust-lang/cc-rs/pull/1627))
- Fix detect_family deadlock ([#1626](https://github.com/rust-lang/cc-rs/pull/1626))
- Fix link in new debug_str doc comment ([#1625](https://github.com/rust-lang/cc-rs/pull/1625))
- Support more of Cargo's debug levels with Build::debug_str ([#1624](https://github.com/rust-lang/cc-rs/pull/1624))

## [1.2.48](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.47...cc-v1.2.48) - 2025-11-28

### Other

- Regenerate target info ([#1620](https://github.com/rust-lang/cc-rs/pull/1620))

## [1.2.47](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.46...cc-v1.2.47) - 2025-11-21

### Other

- add helenos linker identifications ([#1615](https://github.com/rust-lang/cc-rs/pull/1615))

## [1.2.46](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.45...cc-v1.2.46) - 2025-11-14

### Other

- Add Visual Studio 2026 support ([#1609](https://github.com/rust-lang/cc-rs/pull/1609))

## [1.2.45](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.44...cc-v1.2.45) - 2025-11-07

### Other

- Regenerate target info ([#1606](https://github.com/rust-lang/cc-rs/pull/1606))
- Use a default check for the "env" variable in apple_sdk_name ([#1605](https://github.com/rust-lang/cc-rs/pull/1605))

## [1.2.44](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.43...cc-v1.2.44) - 2025-10-31

### Other

- Fix debug assertion for env/abi mismatch ([#1604](https://github.com/rust-lang/cc-rs/pull/1604))
- Update CHANGELOG for version 1.2.43 ([#1602](https://github.com/rust-lang/cc-rs/pull/1602))
- Stop passing an invalid target to `llvm-mingw`'s cross-compilation wrappers ([#1495](https://github.com/rust-lang/cc-rs/pull/1495))

## [1.2.43](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.42...cc-v1.2.43) - 2025-10-24

### Other

- Mark `static_flag` and `shared_flag` as deprecated ([#1582](https://github.com/rust-lang/cc-rs/pull/1582))

## [1.2.42](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.41...cc-v1.2.42) - 2025-10-24

### Other

- Fix check-semver-checks ([#1600](https://github.com/rust-lang/cc-rs/pull/1600))
- minor improvement for docs ([#1598](https://github.com/rust-lang/cc-rs/pull/1598))
- Fix linker-plugin-lto: use `-flto=thin` ([#1594](https://github.com/rust-lang/cc-rs/pull/1594))
- Disable check-buildstd for armv7k-apple-watchos ([#1599](https://github.com/rust-lang/cc-rs/pull/1599))
- Add elf abi to ppc64 targets ([#1596](https://github.com/rust-lang/cc-rs/pull/1596))

## [1.2.41](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.40...cc-v1.2.41) - 2025-10-10

### Other

- Allow using VCToolsVersion to request a specific msvc version ([#1589](https://github.com/rust-lang/cc-rs/pull/1589))
- Regenerate target info ([#1592](https://github.com/rust-lang/cc-rs/pull/1592))
- Regenerate windows sys bindings ([#1591](https://github.com/rust-lang/cc-rs/pull/1591))
- Update windows-bindgen requirement from 0.64 to 0.65 ([#1590](https://github.com/rust-lang/cc-rs/pull/1590))
- Fix `get_base_archiver_variant` for clang-cl: use `--print-search-dirs` ([#1587](https://github.com/rust-lang/cc-rs/pull/1587))

## [1.2.40](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.39...cc-v1.2.40) - 2025-10-03

### Other

- Reorder changelog and remove duplicate Unreleased section ([#1579](https://github.com/rust-lang/cc-rs/pull/1579))
- Prefer clang if linker-plugin-lto specified ([#1573](https://github.com/rust-lang/cc-rs/pull/1573))
- Fix building for Mac Catalyst ([#1577](https://github.com/rust-lang/cc-rs/pull/1577))
- Improve ESP microcontroller targets ([#1574](https://github.com/rust-lang/cc-rs/pull/1574))

## [1.2.39](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.38...cc-v1.2.39) - 2025-09-26

### Other

- Fix cross compilation to xtensa-esp32s3-espidf ([#1569](https://github.com/rust-lang/cc-rs/pull/1569))
- Fix autodetect_wasi_compiler: support non utf-8 path ([#1568](https://github.com/rust-lang/cc-rs/pull/1568))
- Regenerate target info ([#1567](https://github.com/rust-lang/cc-rs/pull/1567))
- Fix rustcflags mapping: require -Clinker-plugin-lto for -flto ([#1564](https://github.com/rust-lang/cc-rs/pull/1564))
- Use `$WASI_SDK_PATH` on WASI targets by default ([#1562](https://github.com/rust-lang/cc-rs/pull/1562))
- Fix atomicity violations in concurrent cache operations ([#1559](https://github.com/rust-lang/cc-rs/pull/1559))

## [1.2.38](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.37...cc-v1.2.38) - 2025-09-19

### Other

- updated the following local packages: find-msvc-tools

## [1.2.37](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.36...cc-v1.2.37) - 2025-09-12

### Other

- Fix errmsg in RustcCodegenFlags::set_rustc_flag ([#1551](https://github.com/rust-lang/cc-rs/pull/1551))
- propagate stack protector to Linux C compilers ([#1550](https://github.com/rust-lang/cc-rs/pull/1550))
- Extract new fn `run_commands_in_parallel` ([#1549](https://github.com/rust-lang/cc-rs/pull/1549))

## [1.2.36](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.35...cc-v1.2.36) - 2025-09-05

### Other

- Regenerate windows sys bindings ([#1548](https://github.com/rust-lang/cc-rs/pull/1548))
- Update windows-bindgen requirement from 0.62 to 0.63 ([#1547](https://github.com/rust-lang/cc-rs/pull/1547))
- Add fn get_ucrt_dir for find-msvc-tools ([#1546](https://github.com/rust-lang/cc-rs/pull/1546))
- Regenerate target info ([#1544](https://github.com/rust-lang/cc-rs/pull/1544))
- fix publish.yml ([#1543](https://github.com/rust-lang/cc-rs/pull/1543))
- Replace periods with underscores as well when parsing env variables ([#1541](https://github.com/rust-lang/cc-rs/pull/1541))

## [1.2.35](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.34...cc-v1.2.35) - 2025-09-01

### Fixed

- fix building for aarch64-apple-visionos-sim on nightly ([#1534](https://github.com/rust-lang/cc-rs/pull/1534))
- fix tests apple_sdkroot_wrong ([#1530](https://github.com/rust-lang/cc-rs/pull/1530))

### Other

- Regenerate target info ([#1536](https://github.com/rust-lang/cc-rs/pull/1536))
- Optimize Tool::to_command ([#1535](https://github.com/rust-lang/cc-rs/pull/1535))
- Extract find-msvc-tools ([#1531](https://github.com/rust-lang/cc-rs/pull/1531))
- Add prefer_clang_cl_over_msvc ([#1516](https://github.com/rust-lang/cc-rs/pull/1516))

## [1.2.34](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.33...cc-v1.2.34) - 2025-08-22

### Fixed

- add `-mcpu=mvp` and `-mmutable-globals` for `wasm32v1-none` ([#1524](https://github.com/rust-lang/cc-rs/pull/1524))

### Other

- Optimize parse_version in find_tools.rs ([#1527](https://github.com/rust-lang/cc-rs/pull/1527))
- Fallback to manually searching for tool dir ([#1526](https://github.com/rust-lang/cc-rs/pull/1526))

## [1.2.33](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.32...cc-v1.2.33) - 2025-08-15

### Other

- Regenerate target info ([#1521](https://github.com/rust-lang/cc-rs/pull/1521))
- [win][arm64ec] Add testing for Arm64EC Windows ([#1512](https://github.com/rust-lang/cc-rs/pull/1512))
- Fix parsing of nigthly targets ([#1517](https://github.com/rust-lang/cc-rs/pull/1517))
- [win][arm64ec] Fix finding assembler and setting is_arm for Arm64EC ([#1511](https://github.com/rust-lang/cc-rs/pull/1511))

## [1.2.32](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.31...cc-v1.2.32) - 2025-08-08

### Fixed

- fix new clippy lint introduced in rust 1.89.0 ([#1509](https://github.com/rust-lang/cc-rs/pull/1509))

### Other

- clarify cargo default if no rerun emitted ([#1508](https://github.com/rust-lang/cc-rs/pull/1508))
- extract compile_objects_sequential ([#1507](https://github.com/rust-lang/cc-rs/pull/1507))
- Windows `find_tools`: add support for finding Clang ([#1506](https://github.com/rust-lang/cc-rs/pull/1506))
- Add m68k-unknown-linux-gnu cross-compile target ([#1505](https://github.com/rust-lang/cc-rs/pull/1505))

## [1.2.31](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.30...cc-v1.2.31) - 2025-08-01

### Other

- Add doc for using sccache/ccache etc ([#1502](https://github.com/rust-lang/cc-rs/pull/1502))
- ability to statically link against C++ stdlib ([#1497](https://github.com/rust-lang/cc-rs/pull/1497))
- Add instructions on using sccache ([#1503](https://github.com/rust-lang/cc-rs/pull/1503))
- Add support for recognizing some architectures supported by GCC, but not LLVM. ([#1500](https://github.com/rust-lang/cc-rs/pull/1500))

## [1.2.30](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.29...cc-v1.2.30) - 2025-07-18

### Other

- define _REENTRANT by default ([#1496](https://github.com/rust-lang/cc-rs/pull/1496))

## [1.2.29](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.28...cc-v1.2.29) - 2025-07-05

### Other

- Fix target parsing for powerpc ([#1490](https://github.com/rust-lang/cc-rs/pull/1490))

## [1.2.28](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.27...cc-v1.2.28) - 2025-07-04

### Other

- Recognize `mlibc` environment ([#1488](https://github.com/rust-lang/cc-rs/pull/1488))
- Fix clippy warnings about not using variables in `format!` strings ([#1489](https://github.com/rust-lang/cc-rs/pull/1489))

## [1.2.27](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.26...cc-v1.2.27) - 2025-06-13

### Other

- Regenerate windows sys bindings ([#1485](https://github.com/rust-lang/cc-rs/pull/1485))
- Update windows-bindgen requirement from 0.61 to 0.62 ([#1484](https://github.com/rust-lang/cc-rs/pull/1484))
- Regenerate target info ([#1483](https://github.com/rust-lang/cc-rs/pull/1483))

## [1.2.26](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.25...cc-v1.2.26) - 2025-06-06

### Other

- Also set `SDKROOT` when building apple platforms ([#1475](https://github.com/rust-lang/cc-rs/pull/1475))
- use windows 2022 in CI ([#1479](https://github.com/rust-lang/cc-rs/pull/1479))
- Detect -Wslash-u-filename warning on clang-cl ([#1477](https://github.com/rust-lang/cc-rs/pull/1477))

## [1.2.25](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.24...cc-v1.2.25) - 2025-05-30

### Other

- make `powerp64` use `powerpc64-linux-gnu` prefix ([#1474](https://github.com/rust-lang/cc-rs/pull/1474))

## [1.2.24](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.23...cc-v1.2.24) - 2025-05-23

### Other

- Regenerate windows sys bindings ([#1471](https://github.com/rust-lang/cc-rs/pull/1471))

## [1.2.23](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.22...cc-v1.2.23) - 2025-05-16

### Other

- support "vxworks" and "nto" OSes on `get_base_archiver_variant` ([#1456](https://github.com/rust-lang/cc-rs/pull/1456))

## [1.2.22](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.21...cc-v1.2.22) - 2025-05-09

### Other

- Add `flags` method to `cc::Build` for adding multiple flags ([#1466](https://github.com/rust-lang/cc-rs/pull/1466))

## [1.2.21](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.20...cc-v1.2.21) - 2025-05-02

### Other

- Fix wasm32-unknown-unknown by passing -c ([#1424](https://github.com/rust-lang/cc-rs/pull/1424))

## [1.2.20](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.19...cc-v1.2.20) - 2025-04-25

### Other

- Regenerate target info ([#1461](https://github.com/rust-lang/cc-rs/pull/1461))
- Fix parser.rs on latest rustc nightly ([#1459](https://github.com/rust-lang/cc-rs/pull/1459))

## [1.2.19](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.18...cc-v1.2.19) - 2025-04-11

### Other

- Fix musl compilation: Add musl as a prefix fallback ([#1455](https://github.com/rust-lang/cc-rs/pull/1455))

## [1.2.18](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.17...cc-v1.2.18) - 2025-04-04

### Other

- Regenerate target info ([#1450](https://github.com/rust-lang/cc-rs/pull/1450))
- Use `std::thread::available_parallelism` for determining the default number of jobs ([#1447](https://github.com/rust-lang/cc-rs/pull/1447))
- Fix mips64-openwrt-linux-musl parsing ([#1449](https://github.com/rust-lang/cc-rs/pull/1449))
- Use compiler prefix `x86_64-linux-musl` ([#1443](https://github.com/rust-lang/cc-rs/pull/1443))

## [1.2.17](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.16...cc-v1.2.17) - 2025-03-21

### Other

- Regenerate target info ([#1439](https://github.com/rust-lang/cc-rs/pull/1439))
- Regenerate windows sys bindings ([#1437](https://github.com/rust-lang/cc-rs/pull/1437))
- Fix wasm32-wali-linux-musl target parsing ([#1434](https://github.com/rust-lang/cc-rs/pull/1434))
- Parse `rustc` target names ([#1413](https://github.com/rust-lang/cc-rs/pull/1413))
- Regenerate target info ([#1429](https://github.com/rust-lang/cc-rs/pull/1429))
- Added base support for `wasm32-wali-linux-musl` target ([#1373](https://github.com/rust-lang/cc-rs/pull/1373))

## [1.2.16](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.15...cc-v1.2.16) - 2025-02-28

### Fixed

- force windows compiler to run in `out_dir` to prevent artifacts in cwd (#1415)

### Other

- use `/arch:SSE2` for `x86` target arch (#1425)
- Regenerate windows-sys binding ([#1422](https://github.com/rust-lang/cc-rs/pull/1422))
- Regenerate target info ([#1418](https://github.com/rust-lang/cc-rs/pull/1418))
- Add LIB var when compiling flag_check (#1417)
- Change flag ordering ([#1403](https://github.com/rust-lang/cc-rs/pull/1403))
- Fix archiver detection for musl cross compilation ([#1404](https://github.com/rust-lang/cc-rs/pull/1404))

## [1.2.15](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.14...cc-v1.2.15) - 2025-02-21

### Other

- Regenerate target info ([#1406](https://github.com/rust-lang/cc-rs/pull/1406))
- Always read from all `CFLAGS`-style flags ([#1401](https://github.com/rust-lang/cc-rs/pull/1401))
- Simplify the error output on failed `Command` invocation ([#1397](https://github.com/rust-lang/cc-rs/pull/1397))

## [1.2.14](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.13...cc-v1.2.14) - 2025-02-14

### Other

- Regenerate target info ([#1398](https://github.com/rust-lang/cc-rs/pull/1398))
- Add support for setting `-gdwarf-{version}` based on RUSTFLAGS ([#1395](https://github.com/rust-lang/cc-rs/pull/1395))
- Add support for alternative network stack io-sock on QNX 7.1 aarch64 and x86_64 ([#1312](https://github.com/rust-lang/cc-rs/pull/1312))

## [1.2.13](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.12...cc-v1.2.13) - 2025-02-08

### Other

- Fix cross-compiling for Apple platforms ([#1389](https://github.com/rust-lang/cc-rs/pull/1389))

## [1.2.12](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.11...cc-v1.2.12) - 2025-02-04

### Other

- Split impl Build ([#1382](https://github.com/rust-lang/cc-rs/pull/1382))
- Don't specify both `-target` and `-mtargetos=` on Apple targets ([#1384](https://github.com/rust-lang/cc-rs/pull/1384))

## [1.2.11](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.10...cc-v1.2.11) - 2025-01-31

### Other

- Fix more flag inheritance ([#1380](https://github.com/rust-lang/cc-rs/pull/1380))
- Include wrapper args. in `stdout` family heuristics to restore classifying `clang --driver-mode=cl` as `Msvc { clang_cl: true }` ([#1378](https://github.com/rust-lang/cc-rs/pull/1378))
- Constrain `-Clto` and `-Cembed-bitcode` flag inheritance to be `clang`-only ([#1379](https://github.com/rust-lang/cc-rs/pull/1379))
- Pass deployment target with `-m*-version-min=` ([#1339](https://github.com/rust-lang/cc-rs/pull/1339))
- Regenerate target info ([#1376](https://github.com/rust-lang/cc-rs/pull/1376))

## [1.2.10](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.9...cc-v1.2.10) - 2025-01-17

### Other

- Fix CC_FORCE_DISABLE=0 evaluating to true ([#1371](https://github.com/rust-lang/cc-rs/pull/1371))
- Regenerate target info ([#1369](https://github.com/rust-lang/cc-rs/pull/1369))
- Make hidden lifetimes explicit. ([#1366](https://github.com/rust-lang/cc-rs/pull/1366))

## [1.2.9](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.8...cc-v1.2.9) - 2025-01-12

### Other

- Don't pass inherited PGO flags to GNU compilers (#1363)
- Adjusted zig cc judgment and avoided zigbuild errors([#1360](https://github.com/rust-lang/cc-rs/pull/1360)) ([#1361](https://github.com/rust-lang/cc-rs/pull/1361))
- Fix compilation on macOS using clang and fix compilation using zig-cc ([#1364](https://github.com/rust-lang/cc-rs/pull/1364))

## [1.2.8](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.7...cc-v1.2.8) - 2025-01-11

### Other

- Add `is_like_clang_cl()` getter (#1357)
- Fix clippy error in lib.rs ([#1356](https://github.com/rust-lang/cc-rs/pull/1356))
- Regenerate target info ([#1352](https://github.com/rust-lang/cc-rs/pull/1352))
- Fix compiler family detection issue with clang-cl on macOS ([#1328](https://github.com/rust-lang/cc-rs/pull/1328))
- Update `windows-bindgen` dependency ([#1347](https://github.com/rust-lang/cc-rs/pull/1347))
- Fix clippy warnings ([#1346](https://github.com/rust-lang/cc-rs/pull/1346))

## [1.2.7](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.6...cc-v1.2.7) - 2025-01-03

### Other

- Regenerate target info ([#1342](https://github.com/rust-lang/cc-rs/pull/1342))
- Document new supported architecture names in windows::find
- Make is_flag_supported_inner take an &Tool ([#1337](https://github.com/rust-lang/cc-rs/pull/1337))
- Fix is_flag_supported on msvc ([#1336](https://github.com/rust-lang/cc-rs/pull/1336))
- Allow using Visual Studio target names in `find_tool` ([#1335](https://github.com/rust-lang/cc-rs/pull/1335))

## [1.2.6](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.5...cc-v1.2.6) - 2024-12-27

### Other

- Don't inherit the `/Oy` flag for 64-bit targets ([#1330](https://github.com/rust-lang/cc-rs/pull/1330))

## [1.2.5](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.4...cc-v1.2.5) - 2024-12-19

### Other

- Check linking when testing if compiler flags are supported ([#1322](https://github.com/rust-lang/cc-rs/pull/1322))

## [1.2.4](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.3...cc-v1.2.4) - 2024-12-13

### Other

- Add support for C/C++ compiler for Neutrino QNX: `qcc` ([#1319](https://github.com/rust-lang/cc-rs/pull/1319))
- use -maix64 instead of -m64 ([#1307](https://github.com/rust-lang/cc-rs/pull/1307))

## [1.2.3](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.2...cc-v1.2.3) - 2024-12-06

### Other

- Improve detection of environment when compiling from msbuild or msvc ([#1310](https://github.com/rust-lang/cc-rs/pull/1310))
- Better error message when failing on unknown targets ([#1313](https://github.com/rust-lang/cc-rs/pull/1313))
- Optimize RustcCodegenFlags ([#1305](https://github.com/rust-lang/cc-rs/pull/1305))

## [1.2.2](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.1...cc-v1.2.2) - 2024-11-29

### Other

- Inherit flags from rustc ([#1279](https://github.com/rust-lang/cc-rs/pull/1279))
- Add support for using sccache wrapper with cuda/nvcc ([#1304](https://github.com/rust-lang/cc-rs/pull/1304))
- Fix msvc stdout not shown on error ([#1303](https://github.com/rust-lang/cc-rs/pull/1303))
- Regenerate target info ([#1301](https://github.com/rust-lang/cc-rs/pull/1301))
- Fix compilation of C++ code for armv7-unknown-linux-gnueabihf ([#1298](https://github.com/rust-lang/cc-rs/pull/1298))
- Fetch target info from Cargo even if `Build::target` is manually set ([#1299](https://github.com/rust-lang/cc-rs/pull/1299))
- Fix two files with different extensions having the same object name ([#1295](https://github.com/rust-lang/cc-rs/pull/1295))
- Allow disabling cc's ability to compile via env var CC_FORCE_DISABLE ([#1292](https://github.com/rust-lang/cc-rs/pull/1292))
- Regenerate target info ([#1293](https://github.com/rust-lang/cc-rs/pull/1293))

## [1.2.1](https://github.com/rust-lang/cc-rs/compare/cc-v1.2.0...cc-v1.2.1) - 2024-11-14

### Other

- When invoking `cl -?`, set stdin to null ([#1288](https://github.com/rust-lang/cc-rs/pull/1288))

## [1.2.0](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.37...cc-v1.2.0) - 2024-11-11

### Added

- add i686-pc-windows-gnullvm prefix detection ([#1283](https://github.com/rust-lang/cc-rs/pull/1283))

### Other

- Allow only specifying the architecture ([#1285](https://github.com/rust-lang/cc-rs/pull/1285))
- Fix WASM vs. WASI options ([#1284](https://github.com/rust-lang/cc-rs/pull/1284))

## [1.1.37](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.36...cc-v1.1.37) - 2024-11-08

### Other

- Use relative directory for obj files hash ([#1270](https://github.com/rust-lang/cc-rs/pull/1270))
- Regenerate target info ([#1280](https://github.com/rust-lang/cc-rs/pull/1280))

## [1.1.36](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.35...cc-v1.1.36) - 2024-11-05

### Other

- Fix CUDA build with clang++. ([#1273](https://github.com/rust-lang/cc-rs/pull/1273))

## [1.1.35](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.34...cc-v1.1.35) - 2024-11-04

### Other

- Remove support for FRC ([#1268](https://github.com/rust-lang/cc-rs/pull/1268))
- Do not add -fPIC by default on UEFI targets ([#1263](https://github.com/rust-lang/cc-rs/pull/1263))
- Use -windows-gnu for all UEFI targets ([#1264](https://github.com/rust-lang/cc-rs/pull/1264))

## [1.1.34](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.33...cc-v1.1.34) - 2024-11-02

### Other

- Remove redundant flags ([#1256](https://github.com/rust-lang/cc-rs/pull/1256))

## [1.1.33](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.32...cc-v1.1.33) - 2024-11-02

### Other

- Reduce size of `cc::Build`  and size of generated targets ([#1257](https://github.com/rust-lang/cc-rs/pull/1257))

## [1.1.32](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.31...cc-v1.1.32) - 2024-11-02

### Other

- Use `rustc`'s knowledge of LLVM/Clang target triples ([#1252](https://github.com/rust-lang/cc-rs/pull/1252))
- Use Cargo's target information when possible ([#1225](https://github.com/rust-lang/cc-rs/pull/1225))

## [1.1.31](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.30...cc-v1.1.31) - 2024-10-19

### Other

- Add comment explaining why cc does not rebuild on env PATH change ([#1247](https://github.com/rust-lang/cc-rs/pull/1247))

## [1.1.30](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.29...cc-v1.1.30) - 2024-10-11

### Other

- Don't pass -fPIC by default on wasm ([#1245](https://github.com/rust-lang/cc-rs/pull/1245))

## [1.1.29](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.28...cc-v1.1.29) - 2024-10-11

### Other

- Regenerate target info ([#1243](https://github.com/rust-lang/cc-rs/pull/1243))

## [1.1.28](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.27...cc-v1.1.28) - 2024-10-06

### Other

- Environment variables: For one accepting boolean, treat "0", "false" and empty env as false ([#1238](https://github.com/rust-lang/cc-rs/pull/1238))

## [1.1.27](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.26...cc-v1.1.27) - 2024-10-06

### Other

- Revert "Use debug version of MSVC runtime library on debug ([#1231](https://github.com/rust-lang/cc-rs/pull/1231))" ([#1237](https://github.com/rust-lang/cc-rs/pull/1237))
- Disable `CC_ENABLE_DEBUG_OUTPUT` if it is set to "0" ([#1234](https://github.com/rust-lang/cc-rs/pull/1234))

## [1.1.26](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.25...cc-v1.1.26) - 2024-10-06

### Other

- Use debug version of MSVC runtime library on debug ([#1231](https://github.com/rust-lang/cc-rs/pull/1231))

## [1.1.25](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.24...cc-v1.1.25) - 2024-10-05

### Other

- Remove incorrect "lib" prefixes in CXXSTDLIB doc comments ([#1228](https://github.com/rust-lang/cc-rs/pull/1228))

## [1.1.24](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.23...cc-v1.1.24) - 2024-10-01

### Other

- Fix wasm32-wasip1-threads:  shared-memory disallowed due to not compiled with 'atomics' or 'bulk-memory' features ([#1221](https://github.com/rust-lang/cc-rs/pull/1221))
- Reduce the need for the host target triple ([#1224](https://github.com/rust-lang/cc-rs/pull/1224))
- Add auto cancellation for CI jobs ([#1222](https://github.com/rust-lang/cc-rs/pull/1222))

## [1.1.23](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.22...cc-v1.1.23) - 2024-09-30

### Other

- Update doc for detecting changes/upgrades of compilers ([#1218](https://github.com/rust-lang/cc-rs/pull/1218))

## [1.1.22](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.21...cc-v1.1.22) - 2024-09-27

### Other

- Don't rerun if PATH changes ([#1215](https://github.com/rust-lang/cc-rs/pull/1215))

## [1.1.21](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.20...cc-v1.1.21) - 2024-09-18

### Other

- disable pic for targets that end in `-none` ([#1212](https://github.com/rust-lang/cc-rs/pull/1212))

## [1.1.20](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.19...cc-v1.1.20) - 2024-09-17

### Other

- Add buildcache as known Rust and C/C++ compiler wrapper ([#1209](https://github.com/rust-lang/cc-rs/pull/1209))

## [1.1.19](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.18...cc-v1.1.19) - 2024-09-15

### Other

- Add support arm64e-apple-darwin ([#1207](https://github.com/rust-lang/cc-rs/pull/1207))

## [1.1.18](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.17...cc-v1.1.18) - 2024-09-07

### Other
- Fixed unsoundness in `StderrForwarder::forward_available` ([#1203](https://github.com/rust-lang/cc-rs/pull/1203))

## [1.1.17](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.16...cc-v1.1.17) - 2024-09-06

### Fixed
- fix finding toolchains when invoked by msbuild ([#1201](https://github.com/rust-lang/cc-rs/pull/1201))

## [1.1.16](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.15...cc-v1.1.16) - 2024-09-04

### Other
- Treat VxWorks wr-cc as a Gnu compiler ([#1198](https://github.com/rust-lang/cc-rs/pull/1198))

## [1.1.15](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.14...cc-v1.1.15) - 2024-08-26

### Other
- Add -mfloat-abi=hard as a default argument when using any arm/thumb-none-eabihf target ([#1194](https://github.com/rust-lang/cc-rs/pull/1194))

## [1.1.14](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.13...cc-v1.1.14) - 2024-08-23

### Other
- allow finding tools from path if VisualStudioDir is set

## [1.1.13](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.12...cc-v1.1.13) - 2024-08-16

### Other
- Fix detect family: should detect emscripten as clang, closes [#1185](https://github.com/rust-lang/cc-rs/pull/1185) ([#1186](https://github.com/rust-lang/cc-rs/pull/1186))

## [1.1.12](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.11...cc-v1.1.12) - 2024-08-15

### Other
- improve docs ([#1183](https://github.com/rust-lang/cc-rs/pull/1183))

## [1.1.11](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.10...cc-v1.1.11) - 2024-08-14

### Other
- Add support for parsing shell encoded `*FLAGS` ([#1181](https://github.com/rust-lang/cc-rs/pull/1181))
- Replace vector of tuples with BTreeMap which already is sorted and free of duplicates ([#1177](https://github.com/rust-lang/cc-rs/pull/1177))

## [1.1.10](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.9...cc-v1.1.10) - 2024-08-11

### Other
- Remap Windows targets triples to their LLVM counterparts ([#1176](https://github.com/rust-lang/cc-rs/pull/1176))

## [1.1.9](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.8...cc-v1.1.9) - 2024-08-11

### Other
- Add custom CC wrapper to the wrapper whitelist ([#1175](https://github.com/rust-lang/cc-rs/pull/1175))

## [1.1.8](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.7...cc-v1.1.8) - 2024-08-06

### Other
- Fix broken link in docs.rs ([#1173](https://github.com/rust-lang/cc-rs/pull/1173))

## [1.1.7](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.6...cc-v1.1.7) - 2024-07-29

### Other
- add `.objects` ([#1166](https://github.com/rust-lang/cc-rs/pull/1166))

## [1.1.6](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.5...cc-v1.1.6) - 2024-07-19

### Other
- Clippy fixes ([#1163](https://github.com/rust-lang/cc-rs/pull/1163))

## [1.1.5](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.4...cc-v1.1.5) - 2024-07-15

### Other
- Fix cyclic compilation: Use vendored once_cell ([#1154](https://github.com/rust-lang/cc-rs/pull/1154))

## [1.1.4](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.3...cc-v1.1.4) - 2024-07-14

### Other
- Support compiling on wasm targets (Supersede [#1068](https://github.com/rust-lang/cc-rs/pull/1068)) ([#1160](https://github.com/rust-lang/cc-rs/pull/1160))

## [1.1.3](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.2...cc-v1.1.3) - 2024-07-14

### Other
- Reduce msrv to 1.63 ([#1158](https://github.com/rust-lang/cc-rs/pull/1158))
- Revert "Use raw-dylib for windows-sys ([#1137](https://github.com/rust-lang/cc-rs/pull/1137))" ([#1157](https://github.com/rust-lang/cc-rs/pull/1157))
- Fix typos ([#1152](https://github.com/rust-lang/cc-rs/pull/1152))
- Fix `doc_lazy_continuation` lints ([#1153](https://github.com/rust-lang/cc-rs/pull/1153))

## [1.1.2](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.1...cc-v1.1.2) - 2024-07-12

### Other
- Add empty `jobserver` feature. ([#1150](https://github.com/rust-lang/cc-rs/pull/1150))

## [1.1.1](https://github.com/rust-lang/cc-rs/compare/cc-v1.1.0...cc-v1.1.1) - 2024-07-12

### Other
- Fix is_flag_supported not respecting emit_rerun_if_env_changed ([#1147](https://github.com/rust-lang/cc-rs/pull/1147)) ([#1148](https://github.com/rust-lang/cc-rs/pull/1148))

## [1.1.0](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.106...cc-v1.1.0) - 2024-07-08

### Added
- add cargo_output to eliminate last vestiges of stdout pollution ([#1141](https://github.com/rust-lang/cc-rs/pull/1141))

## [1.0.106](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.105...cc-v1.0.106) - 2024-07-08

### Other
- Drop support for Visual Studio 12 (2013) ([#1046](https://github.com/rust-lang/cc-rs/pull/1046))
- Use raw-dylib for windows-sys ([#1137](https://github.com/rust-lang/cc-rs/pull/1137))
- Bump msrv to 1.67 ([#1143](https://github.com/rust-lang/cc-rs/pull/1143))
- Bump msrv to 1.65 ([#1140](https://github.com/rust-lang/cc-rs/pull/1140))
- Fix clippy warnings ([#1138](https://github.com/rust-lang/cc-rs/pull/1138))

## [1.0.105](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.104...cc-v1.0.105) - 2024-07-07

### Other
- Regenerate windows sys bindings ([#1132](https://github.com/rust-lang/cc-rs/pull/1132))
- Fix generate-windows-sys-bindings ([#1133](https://github.com/rust-lang/cc-rs/pull/1133))
- Fix gen-windows-sys-binding ([#1130](https://github.com/rust-lang/cc-rs/pull/1130))
- Fix gen-windows-sys-binding ([#1127](https://github.com/rust-lang/cc-rs/pull/1127))
- Update windows-bindgen requirement from 0.57 to 0.58 ([#1123](https://github.com/rust-lang/cc-rs/pull/1123))

## [1.0.104](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.103...cc-v1.0.104) - 2024-07-01

### Other
- Fixed link break about compile-time-requirements ([#1118](https://github.com/rust-lang/cc-rs/pull/1118))

## [1.0.103](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.102...cc-v1.0.103) - 2024-06-30

### Other
- Fix compilation for wasm: env WASI_SYSROOT should be optional ([#1114](https://github.com/rust-lang/cc-rs/pull/1114))

## [1.0.102](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.101...cc-v1.0.102) - 2024-06-29

### Other
- Fix invalid wasi targets compatibility ([#1105](https://github.com/rust-lang/cc-rs/pull/1105))
- Speedup regenerate-target-info and regenerate-windows-sys ([#1110](https://github.com/rust-lang/cc-rs/pull/1110))

## [1.0.101](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.100...cc-v1.0.101) - 2024-06-25

### Other
- Use `Build::getenv` instead of `env::var*` in anywhere that makes sense ([#1103](https://github.com/rust-lang/cc-rs/pull/1103))

## [1.0.100](https://github.com/rust-lang/cc-rs/compare/cc-v1.0.99...cc-v1.0.100) - 2024-06-23

### Other
- Update publish.yml to use release-plz ([#1101](https://github.com/rust-lang/cc-rs/pull/1101))
- Accept `OsStr` instead of `str` for flags ([#1100](https://github.com/rust-lang/cc-rs/pull/1100))
- Use `dep:` syntax to avoid implicit features. ([#1099](https://github.com/rust-lang/cc-rs/pull/1099))
- Minor clippy fixes. ([#1098](https://github.com/rust-lang/cc-rs/pull/1098))
- Fix WASI compilation for C++ ([#1083](https://github.com/rust-lang/cc-rs/pull/1083))
- Regenerate windows sys bindings ([#1096](https://github.com/rust-lang/cc-rs/pull/1096))
- Rename regenerate-windows-sys to regenerate-windows-sys.yml ([#1095](https://github.com/rust-lang/cc-rs/pull/1095))
- Create regenerate-windows-sys.yml ([#1094](https://github.com/rust-lang/cc-rs/pull/1094))
- Update windows-bindgen requirement from 0.56 to 0.57 ([#1091](https://github.com/rust-lang/cc-rs/pull/1091))
- Eagerly close tempfile to fix [#1082](https://github.com/rust-lang/cc-rs/pull/1082) ([#1087](https://github.com/rust-lang/cc-rs/pull/1087))
- Output msvc.exe in the output directory ([#1090](https://github.com/rust-lang/cc-rs/pull/1090))
- Fix clippy warnings on Windows ([#1088](https://github.com/rust-lang/cc-rs/pull/1088))
- Don't try to free DLL on drop ([#1089](https://github.com/rust-lang/cc-rs/pull/1089))
- Fix panic safety issue in StderrForwarder ([#1079](https://github.com/rust-lang/cc-rs/pull/1079))
