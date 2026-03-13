# Changelog

## 2026-03-13

### Added — Region Filter System (全部藏品)

**Two-tier classification for Full Holdings section:**

**Row 1 — Region buttons:**
- 全部 | 中央 | 造总 | 北洋 | 吉林 | 奉天 | 江南 | 安徽 | 湖北 | 湖南 | 四川 | 广东 | 云南 | 福建 | 浙江 | 袁像 | 孙像 | 军阀

**Row 2 — Sort buttons:**
- 按时间 | 按估值 | 按珍稀度 | 样币
- Click once for ascending, click again for descending (with arrow indicator)

**COIN_REGION mapping — every coin tagged to its mint origin:**

| Region | Coin IDs | Count |
|--------|----------|-------|
| 中央 | C030, C048, C090 | 3 |
| 造总 | C032, C045, C084 | 3 |
| 北洋 | C031, C078, C085 | 3 |
| 吉林 | C079 | 1 |
| 奉天 | C081, C089 | 2 |
| 江南 | C010, C061-C064, C080 | 6 |
| 湖北 | C018, C033, C034, C082 | 4 |
| 四川 | C086 | 1 |
| 广东 | C011, C044, C047, C083 | 4 |
| 云南 | C087 | 1 |
| 福建 | C097 | 1 |
| 浙江 | C098 | 1 |
| 袁像 | C013, C014, C020, C037, C038, C046, C049, C069-C072 | 11 |
| 孙像 | C012, C017, C019, C039-C043, C054-C059, C067, C068, C073-C077, C091-C094 | 25 |
| 军阀 | C015, C016, C035, C036, C050-C053, C060, C065, C066, C095, C096, C099, C100 | 15 |

### Fixed — Dropdown filter alignment

Dropdown (搜索框右边) now uses COIN_REGION mapping:
- **清·壹两** — coins with 壹两/一两 in name (8 coins across provinces)
- **清·中央龙洋** — COIN_REGION = 中央
- **清·省造龙洋** — all provincial regions combined (造总/北洋/吉林/奉天/江南/安徽/湖北/湖南/四川/广东/云南/福建/浙江)
- **民国·袁像** — COIN_REGION = 袁像
- **民国·孙像** — COIN_REGION = 孙像
- **军阀** — COIN_REGION = 军阀

### Fixed — Year sort using data field

Sort by time now uses each coin's `year` field (e.g., `1897`, `1908`) instead of parsing from Chinese name. Previously, coins without a year pattern in their name (e.g., 江南省造光绪元宝) all defaulted to 1900, making the sort appear broken.

### Fixed — filterDB crash (curLang undefined)

`filterDB()` referenced an undefined variable `curLang`, causing a silent ReferenceError that broke all filter and sort buttons. Fixed to use the correct language variable `CL`.

---

## 2026-03-08

### Added — Live Tracker section

Real-time auction monitoring for Xianyu, Huaxia, Heritage, SBP, and Auction World.

### Improved — Smart parser

Rewrote smart parser for better data extraction from auction results.
