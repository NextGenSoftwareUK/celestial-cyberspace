# Celestial Cyberspace

The OASIS holonic galaxy map and pre-check portal. A cosmic UI for exploring, classifying, and holonizing projects as celestial bodies in the OASIS omniverse.

## Pages

| Path | Description |
|------|-------------|
| `/` or `/galaxy` | Celestial Cyberspace — interactive 3D galaxy map |
| `/check` | Holonic Pre-Check — scan a GitHub repo, Web3 protocol, or local project for celestial classification |
| `/import` | Import Portal |

## Celestial Tiers

Projects are classified based on size and activity metrics:

| Tier | Criteria |
|------|----------|
| 🌑 Moon | < 1k LOC / small token |
| 🌍 Planet | 1k–10k LOC / small cap |
| ⭐ Star | 10k–100k LOC / mid cap |
| 🌟 SuperStar | 100k–500k LOC / large cap |
| 💫 GrandSuperStar | 500k+ LOC / mega cap |

## Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/NextGenSoftwareUK/celestial-cyberspace)

```bash
# One-shot deploy via CLI
npx vercel --prod
```

## Backend

The GitHub and Web3 pre-checks run entirely in-browser via public APIs (GitHub, DefiLlama, CoinGecko). No backend required for these features.

The **Local Clone** scan tab requires the OASIS WebAPI running locally:
```bash
cd "STAR ODK/NextGenSoftware.OASIS.STAR.WebAPI"
dotnet run --urls "http://localhost:50564"
```

To connect a deployed OASIS API to the galaxy map, set `window.__OASIS_API__` before the module loads:
```html
<script>window.__OASIS_API__ = 'https://your-api.railway.app';</script>
```

## Stack

- **Three.js** — 3D galaxy rendering via ES module import map
- **Vanilla JS** — no build step, deploy as static files
- **GitHub API** — repo stats for pre-check
- **DefiLlama API** — DeFi TVL and protocol data
- **CoinGecko API** — token market cap and community data
- **MetaMask** — Web3 ownership verification

## Part of OASIS

[OASIS](https://github.com/NextGenSoftwareUK/Our-World-OASIS-API-HoloNET-HoloUnity-And-HoloUnity-For-Unity) · Open Architecture for Sovereign Interdimensional Systems
