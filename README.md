# Midtown Athletic Gym QR Guide (unofficial demo)

**QR machine-instruction app skinned for a Midtown Athletic club demo.** Members scan a QR on a machine → bilingual (EN/FR) how-to guide. Staff manage machines, download QRs, print floor sheets, and review ROI insights.

> **Unofficial demo mockup for pitching only.** Not affiliated with Midtown Athletic or any parent company. Does **not** use official logo image assets — text wordmark only. Brand colors (`#C4A35A` / `#1B1B1B`) are approximate pitch tokens.

Seeded demo gym: **Midtown Sanctuaire Montréal**. `/` is the **demo-ready member product UI** — not a marketing landing page.

Sibling (generic GymQR Guide): [gym-machine-qr-guide](https://github.com/alexbalut/gym-machine-qr-guide)

## Disclaimer

This repository is an **unofficial product demo**. Midtown Athletic® and related marks belong to their respective owners. Do not represent this app as an official Midtown Athletic product. No official logos are bundled.

## Quick start

```bash
cd midtown-sanctuaire-gym-qr-guide
cp .env.example .env
npm install
npx prisma db push
npm run seed
npm run dev
```

Or one-shot setup:

```bash
npm install && npm run setup && npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — member gym home for **Midtown Sanctuaire Montréal** (Machines / Workout / Progress / Scan).

## Demo credentials

| Field    | Value                    |
|----------|--------------------------|
| Email    | `admin@midtown-sanctuaire.demo`        |
| Password | `demo1234`             |
| Gym      | Midtown Sanctuaire Montréal                |
| Slug     | `midtown-sanctuaire`           |

Seed creates **10 bilingual machines**, sample view counts, and a few open/resolved issues.

## Branding notes

- Surfaces use secondary `#1B1B1B` with primary accent **`#C4A35A`**
- Text wordmark **Midtown Athletic** — no trademarked logo files
- Tagline: “Premium athletic club”

## Key routes

| Route | Description |
|-------|-------------|
| `/` | Gym member home |
| `/scan` | Camera QR scan |
| `/q/[token]` | Machine guide |
| `/m/midtown-sanctuaire/[machineSlug]` | Friendly slug URL |
| `/admin/login` | Staff login |
| `/admin/insights` | Owner ROI dashboard |

## Caveats

- Auth is simple credential + JWT cookie — fine for demo; harden for production.
- SQLite at `prisma/dev.db` — don’t commit it.
- Member workout/progress is browser localStorage only (`midtown-sanctuaire-workout:v1:<slug>`).
- Unofficial branding — do not ship as an official Midtown Athletic app.

## Photo credits

Demo photos under `public/machines/` are from Unsplash — see [CREDITS.md](./CREDITS.md). Not official Midtown Athletic assets.

## License / affiliation

This repository is an **unofficial product demo mockup** for pitch purposes. Midtown Athletic® and related marks belong to their respective owners. Do not represent this app as an official Midtown Athletic product.

## Repo

https://github.com/alexbalut/midtown-sanctuaire-gym-qr-guide
