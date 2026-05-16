# Military Pension Studio

A retirement decision instrument for US service members. One self-contained HTML file. No accounts, no tracking, runs entirely in your browser.

**Live:** https://stevennolanjr-dev.github.io/military-pension-studio/

## What it does

Calculates your net monthly retired pay after every modeled tax, premium, and offset, then helps you make the four hard decisions that go into a retirement:

1. **When to retire.** The COLA trap + time-in-service accrual chart by month.
2. **Where to live.** Side-by-side comparison of US states and 24 expat destinations on cost-of-living-adjusted buying power.
3. **What to elect.** Survivor Benefit Plan base amount, BRS lump sum (if applicable), Social Security claim age.
4. **How to transition.** First 12 months of cash flow with terminal leave, SkillBridge, pension lag, and target civilian salary to match active duty takehome.

## Features

- All four retirement systems: High-3, Blended Retirement System (BRS), REDUX, Final Pay
- 2026 VA disability rates with combined ratings and dependent uplifts
- Concurrent Retirement and Disability Pay (CRDP) and Combat-Related Special Compensation (CRSC) modeling
- Date optimizer for first-year COLA + TIS accrual
- 50 states plus DC and 24 expat destinations: Portugal, Mexico, Panama, Costa Rica, Spain, Italy, Ecuador, Colombia, Belize, Malaysia, Thailand, Philippines, Greece, Malta, Cyprus, Vietnam, Czech Republic, Uruguay, Dominican Republic, Turkey, Ireland, UK/Scotland, Netherlands, France
- Auto-computed federal effective tax rate from 2026 IRS brackets with filing status
- Auto-computed years in retirement from life expectancy tables
- Social Security with claim age decision (62-70) and breakeven analysis
- Thrift Savings Plan projection with growth rate up to 200%
- Survivor Benefit Plan modeling with the 2023 widow's tax elimination
- BAH cliff and target civilian salary calculation
- TRICARE Prime, Select, and Overseas premium modeling
- Print stylesheet for clean PDF export
- Mobile responsive
- Inline Learn blocks on every major decision
- Confidence badges (High / Medium / Low) on every result

## Sources

All rates and tables verified May 2026:

- **Pension formulas:** 10 U.S.C. § 1409 (High-3), § 1415 (BRS); DFAS calculation methods
- **VA disability rates 2026:** VA.gov 2026 compensation rate tables (2.8% COLA, effective Dec 1, 2025)
- **Federal tax brackets 2026:** IRS Revenue Procedure 2025-32 via Tax Foundation
- **State income tax treatment:** TheMilitaryWallet.com, state veteran affairs offices, Tax Foundation 2025
- **State cost of living indices:** C2ER 2025
- **Effective property tax rates:** Tax Foundation 2025
- **Expat country cost of living:** Numbeo 2026, rebased to US average = 100
- **TRICARE premiums:** TRICARE.mil 2026 enrollment fees
- **Social Security:** SSA Period Life Tables 2024, SSA early/delayed retirement factors
- **CRDP / CRSC eligibility:** 38 CFR § 3.750 (CRDP), 10 U.S.C. § 1413a (CRSC)

## Disclaimers

This is a **planning instrument**, not a substitute for professional advice. Official retirement pay is determined by the Defense Finance and Accounting Service (DFAS) based on your actual record.

- Tax calculations do not include itemized deductions, qualified business income deduction, capital gains, Additional Medicare Tax, or Alternative Minimum Tax. For complex situations, override the auto rate.
- State and expat tax treatment is general. Specific exemptions, age thresholds, income limits, and treaty edge cases vary.
- Cost of living indices are area or country averages. Real numbers vary widely by city.
- REDUX age-62 catch-up is described but simplified in lifetime calculations.
- BRS lump sum uses an approximate 2026 personal discount rate (~7%).

Verify with your retirement services office and a tax professional before locking in a date.

## Deploy your own

This is a single static HTML file with no build step. Any static host works.

**GitHub Pages (recommended):**

```bash
# 1. Create a new public repository named "military-pension-studio" on github.com
# 2. From your local copy:
git init
git add .
git commit -m "Initial commit: Military Pension Studio v3.2"
git branch -M main
git remote add origin https://github.com/stevennolanjr-dev/military-pension-studio.git
git push -u origin main

# 3. On github.com → your repo → Settings → Pages
#    Source: Deploy from a branch
#    Branch: main / (root)
#    Save
```

Within a minute it will be live at `https://stevennolanjr-dev.github.io/military-pension-studio/`.

**Other hosts that work with zero config:** Netlify (drag and drop), Cloudflare Pages, Vercel, any S3 + CloudFront setup, any static file server.

## License

MIT. See [LICENSE](LICENSE).

## Built with Claude

This project was designed and built in conversation with Anthropic's Claude over a few iterations of feature requests and review cycles, with cross-review from OpenAI's Codex. The math has been spot-checked against the official DFAS, VA, IRS, and SSA references cited above, and against a working COLA trap workbook from CG Fleissner.

If you find an error or have a feature request, open an issue.

---

*Not affiliated with, endorsed by, or connected to the U.S. Department of Defense, Department of Veterans Affairs, IRS, or any federal agency.*
