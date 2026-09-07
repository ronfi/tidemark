# Tidemark · 潮位线

> **Bands, not points. Scored, not spun.**
> **档位,不是点位。记分,不是嘴炮。**

**🌊 在线主页 / Live page:<https://ronfi.github.io/tidemark/>** —— 每日更新 / updated daily

---

## 中文

主页包含四部分:比特币周期图 / 周期高点档位 / 交易所净流量 / 情绪六维面板,外加一本记分账本。

1. **比特币周期图(Bitcoin Cycle Chart)** —— 三次减半、三轮顶底与三排跨距(减半→顶、顶→底、顶→今日)画在一张对数图上,本轮低点标"未确认"。
2. **加密周期高点档位(Cycle-Top Bands)** —— 对主流币下一轮牛市高点的推测,以**档位区间 + 偏斜方向**发布,**预注册、带证伪条件、触发后不得回改**。
3. **交易所净流量(CEX Net Flow)** —— 链上储备前 10 名交易所公布地址上 BTC / ETH / 稳定币的每日净流量(枚数变动 × 当日价,已剔除币价涨跌本身的影响),叠加 BTC 价格;地址清单变动日按机械规则剔除并公示明细。
4. **情绪六维面板(6-Dim Sentiment Panel)** —— 资金费 / 散户多空比 / 大户持仓比 / taker 比 / 持仓量分位 / 恐惧贪婪指数,九个标的(BTC / ETH / SOL / BNB / XRP / DOGE / ZEC / HYPE / UNI),含历史回溯。

### 我们错了会怎样(先读这个)

这是本项目与预测类内容的根本区别:**每一条推测在发布时就登记了记分规则**。

- 所有档位/预测进入 [`data/scorecard.json`](data/scorecard.json)(append-only 账本),**登记后不得修改或删除**;
- 每条带明确的**判定时点**与**证伪条件**;到期后无论对错,结果回填并公示;
- 档位可以重估,但**只能新增版本条目并保留旧档**,旧档的被击穿时点与价格一并冻结在 [`data/bands.json`](data/bands.json) 里;
- 概率与档位的**校准历史全程可查** —— 错误不删除,错误是记分的一部分。

### 数据说明

- 周期图与情绪面板:币安公开 API、alternative.me 恐惧贪婪指数。
- 交易所净流量:DefiLlama 各交易所按链按币的每日持仓(公开 API);十家为 Binance / OKX / Bitfinex / Bybit / Robinhood / Gate / Bitget / Gemini / MEXC / Deribit。
- 档位方法论概要:n=3 周期衰减律 × 供给面交叉检验;机制变更或已走出历史倍数族值域的标的,改用机制条件档。详见发布页内注。
- ⚠ 三条口径限制:恐惧贪婪指数是**市场级单一序列**,九个面板里那一维是同一条曲线;判读纪律的阈值**只在 BTC 与 ETH 上标定过**;各标的历史长度不同(HYPE 只有 2025-05 起的一个不完整周期)。

### 免责声明

一切内容均为条件情景研究,**不构成投资建议**。所有模型不应当作交易信号 —— 这句话本身就是方法论的一部分。

---

## English

The page has four parts — a Bitcoin cycle chart, cycle-top bands, exchange net flow, and a six-dimension sentiment panel — plus a scorecard ledger.

1. **Bitcoin Cycle Chart** — three halvings, three cycle tops and bottoms, and three rows of spans (halving→top, top→bottom, top→today) on one log chart; this cycle's low is marked "unconfirmed".
2. **Cycle-Top Bands** — estimates for the next bull-market high of major coins, published as **a range plus a skew direction**, **pre-registered, with falsification conditions, and never revised after they trigger**.
3. **CEX Net Flow** — daily net flow of BTC / ETH / stablecoins across the published addresses of the top 10 exchanges by on-chain reserves (change in coin count × that day's price, so price moves themselves are removed), overlaid on the BTC price; days when an address list changed are excluded by a mechanical rule and listed in full.
4. **6-Dim Sentiment Panel** — funding rate / retail long-short ratio / top-trader position ratio / taker ratio / open-interest percentile / fear & greed index, for nine assets (BTC / ETH / SOL / BNB / XRP / DOGE / ZEC / HYPE / UNI), with history.

### What happens when we are wrong (read this first)

This is what separates the project from prediction content: **every estimate registers its scoring rule at publication.**

- All bands and predictions go into [`data/scorecard.json`](data/scorecard.json), an append-only ledger — **once registered, entries are never edited or deleted**;
- Each carries an explicit **judgement date** and **falsification condition**; when it comes due the outcome is filled in and published, right or wrong;
- Bands may be re-estimated, but **only by adding a version entry while keeping the old band**; the old band's breach date and price are frozen into [`data/bands.json`](data/bands.json);
- The full **calibration history stays visible** — mistakes are not deleted; they are part of the score.

### Data

- Cycle chart and sentiment panel: Binance public API, alternative.me Fear & Greed index.
- Exchange net flow: DefiLlama per-chain, per-token daily holdings for each exchange (public API); the ten are Binance / OKX / Bitfinex / Bybit / Robinhood / Gate / Bitget / Gemini / MEXC / Deribit.
- Band methodology in brief: an n=3 cycle-decay law cross-checked against supply-side facts; assets whose token mechanism has changed, or that have moved outside the historical multiple range, switch to a mechanism-conditional band. Details are annotated on the page.
- ⚠ Three caliber limits: the Fear & Greed index is a **single market-level series**, so that dimension is the same curve in all nine panels; the reading thresholds are **calibrated on BTC and ETH only**; history lengths differ (HYPE has just one incomplete cycle, from 2025-05).

### Disclaimer

Everything here is conditional scenario research and is **not investment advice**. None of these models should be treated as trading signals — that sentence is itself part of the methodology.

---

## 打赏 / Support

如果这些刻度对你有用,欢迎支持本项目持续维护;地址只以 main 分支的 [DONATE.md](DONATE.md) 为准,在其他任何地方看到的地址,无论看起来多像,都不要使用。

If these gauges are useful to you, support for the project's continued maintenance is welcome; use only the addresses in [DONATE.md](DONATE.md) on the main branch, and no address you see anywhere else, however similar it looks.

## License

发布内容采用 **CC BY-NC-ND 4.0**(署名-非商业-禁止演绎)。你可以引用与转发(注明出处),不可商用,不可修改后再发布。

Published content is licensed **CC BY-NC-ND 4.0**. You may quote and share it with attribution; commercial use and derivative works are not permitted.
