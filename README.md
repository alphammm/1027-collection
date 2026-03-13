# 1024 Collection | 中国机制币珍藏

A museum-grade digital catalog of Chinese milled silver coins spanning the late Qing Dynasty to the Republic era (1889-1936).

## Live Site

**https://1024-collection.vercel.app**

## Overview

1024 Collection is a comprehensive numismatic database featuring 80+ Chinese milled silver coins, covering:

- **Qing Dynasty central coinage** — Da Qing Silver Coins, Hu Bu Taels
- **Provincial dragon dollars** — Kwangtung, Kiangnan, Fengtian, Pei Yang, Kirin, Hupeh, Szechuan, Yunnan, Fukien, Chekiang
- **Yuan Shikai portraits** — Year 3-10 dollars, Flying Dragon, signed patterns
- **Sun Yat-sen portraits** — Junk dollars, Dragon & Phoenix, Memento dollars
- **Warlord era** — Zhang Zuolin, Li Yuanhong, Xu Shichang, Cao Kun, Duan Qirui, Tang Jiyao

## Features

### Full Holdings (全部藏品)

**Two-tier filtering system:**

| Layer | Function | Options |
|-------|----------|---------|
| Row 1 — Region | Filter by mint origin | 全部, 中央, 造总, 北洋, 吉林, 奉天, 江南, 安徽, 湖北, 湖南, 四川, 广东, 云南, 福建, 浙江, 袁像, 孙像, 军阀 |
| Row 2 — Sort | Sort within selection | 按时间, 按估值, 按珍稀度, 样币 |

- Sort buttons toggle ascending/descending on repeated click (arrow indicator)
- Dropdown filter aligns with region mapping (省造龙洋 = all provincial mints, 壹两 = tael denominations)
- Region and sort filters can be combined

### Other Sections

- **至臻之藏** — The Finest: top-tier rarities
- **巅峰评级** — Top Grades: highest graded specimens
- **顶级名誉品** — Masterpieces: the most celebrated coins
- **各省龙洋** — Provincial Dragons: by province
- **拍卖溯源** — Auction Provenance: full auction history
- **收藏圣杯** — The Grails: wish list
- **藏家档案** — Collector Profiles
- **数据库** — Numismatic Database: 11 auction house data sources
- **交易记录** — Trade History (P&L tracking)
- **实时追踪** — Live Tracker: real-time auction monitoring

## Data Sources

Auction records compiled from Heritage Auctions, Stack's Bowers, Beijing ChengXuan, China Guardian, PCGS Population Reports, ShouXi.com, and more.

## Tech Stack

Single-page static site. HTML + inline CSS + inline JS. No build step. Deployed on Vercel.

## Repository Structure

```
index.html          — Main application (root, served by Vercel)
data.js             — Coin database (88 entries)
auctions.js         — Auction tracking data
img/                — PCGS certificate images
VERSION01-03/       — Historical versions
```

## Deployment

```bash
# Deploy to Vercel
npx vercel build --prod && npx vercel deploy --prebuilt --prod
```
