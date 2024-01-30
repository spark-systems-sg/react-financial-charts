# React Financial Charts: Spark Fork

This repository is a fork of [react-financial-charts](https://github.com/react-financial/react-financial-charts/) with minor UI customizations.
Customizations at this point are limited to the `series` and `axes` packages.

### Use the forked library
1. Add the spark npm repository to your `.npmrc` \
   `npm config set @spark:registry https://artifactoryus.sparksystems.sg:8443`
2. Install the packages with the `@spark` scope \
   `npm install @spark/react-finacial-charts-series @spark/react-financial-charts-axes`
3. Import from the components as required
   ```
   import { CandlestickSeries } from '@spark/react-financial-charts-series';
   import { XAxis } from '@spark/react-financial-charts-axes';
   ```
   
### Create a release
1. Create a `-RC` or `-PA` branch
2. Commit changes with messages following the [conventional commits](https://www.conventionalcommits.org) style of commit messages \
   → The commit messages will be used for the changelog
3. Approve the release job in Circle CI
   - This will create a release commit and with tag
   - The tag will trigger a `publish` job, publishing the package to the spark repository


---
**_ORIGINAL README BELOW_**

---

# React Financial Charts

> **Note:** this repo is a fork of [react-stockcharts](https://github.com/rrag/react-stockcharts), renamed, converted to typescript and bug fixes applied due to the original project being unmaintained.

> **Note:** v1 is a fully breaking change with large parts, if not all, rewritten. Do not expect the same API! although the same features should exist.

![ci](https://github.com/react-financial/react-financial-charts/workflows/ci/badge.svg)
[![codecov](https://codecov.io/gh/reactivemarkets/react-financial-charts/branch/master/graph/badge.svg)](https://codecov.io/gh/reactivemarkets/react-financial-charts)
 [![GitHub license](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/react-financial/react-financial-charts/blob/master/LICENSE) [![npm version](https://img.shields.io/npm/v/react-financial-charts.svg?style=flat)](https://www.npmjs.com/package/react-financial-charts)

Charts dedicated to finance.

The aim with this project is create financial charts that work out of the box.

## Features

- integrates multiple chart types
- technical indicators and overlays
- drawing objects

### Chart types

- Scatter
- Area
- Line
- Candlestick
- OHLC
- HeikenAshi
- Renko
- Kagi
- Point & Figure

### Indicators

- EMA, SMA, WMA, TMA
- Bollinger band
- SAR
- MACD
- RSI
- ATR
- Stochastic (fast, slow, full)
- ForceIndex
- ElderRay
- Elder Impulse

### Interactive Indicators

- Trendline
- Fibonacci Retracements
- Gann Fan
- Channel
- Linear regression channel

---

## Installation

```sh
npm install react-financial-charts
```

## Documentation

[Stories](https://react-financial.github.io/react-financial-charts/)

## Contributing

Refer to [CONTRIBUTING.md](./CONTRIBUTING.md)

This project is a mono-repo that uses [Lerna](https://lerna.js.org/) to manage dependencies between packages.

To get started run:

```bash
git clone https://github.com/react-financial/react-financial-charts.git
cd react-financial-charts
npm ci
npm run build
```

To start up a development server run:

```bash
npm start
```

## Roadmap

- [x] Convert to typescript
- [x] Bump dependencies to latest
- [x] Remove React 16 warnings
- [x] Add CI
- [x] Fix passive scrolling issues
- [x] Implement PRs from react-stockcharts
- [x] Add all typings
- [x] Move examples to storybook
- [x] Add all series' to storybook
- [x] Split project into multiple packages
- [x] Fix issues with empty datasets
- [x] Correct all class props
- [x] Migrate to new React Context API
- [x] Remove all UNSAFE methods
- [ ] Add documentation to storybook
- [ ] Add full test suite

## LICENSE

[![FOSSA Status](https://app.fossa.com/api/projects/custom%2B13613%2Fgit%40github.com%3Areactivemarkets%2Freact-financial-charts.git.svg?type=large)](https://app.fossa.com/projects/custom%2B13613%2Fgit%40github.com%3Areactivemarkets%2Freact-financial-charts.git?ref=badge_large)
