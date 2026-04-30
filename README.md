# anti-dev-tier-list

> S–F tier list of platforms, APIs, licenses, and policies ranked by how hostile they are to developers — with receipts.

Maintained by [Brethof AI](https://brethof.com). The counterpart to the
[awesome-*](https://github.com/BrethofAI) family: instead of
recommending tools, this list calls out the platforms and practices
that punish developers and small teams.

## Rules of the list

1. **Criticise practices, not people.** Every entry is a documented
   policy, ToS clause, pricing model, or platform behaviour — not an
   individual employee or executive.
2. **Receipts or it didn't happen.** Each entry links to source
   evidence (official docs, court filings, dated blog posts, archived
   screenshots). If the receipt rots, we mark the entry stale and
   re-verify before the next release.
3. **Tiers are about damage to developers**, not about whether the
   platform is good for users or shareholders. A great consumer
   experience built on developer-hostile infrastructure still ranks
   high here.
4. **Improvement removes you from the list.** When a vendor reverses a
   policy, we move them and note the date. Public retraction earns
   public retraction.

## Tier definitions

| Tier | Meaning |
|------|---------|
| **S** | Catastrophic. Whole categories of work made impossible or non-economic. Trust-destroying. |
| **A** | Very harmful. Costs serious money or time; widely felt. |
| **B** | Hostile-but-survivable. Friction tax, well-known pattern, predictable workarounds. |
| **C** | Annoying. Death by a thousand cuts; individually small, collectively meaningful. |
| **D** | Petty. Documented bad practice but limited blast radius. |
| **F** | So bad it's a meme. Self-defeating policies, courtroom losses, retractions in slow motion. |

## Contents

- [Tier S — Catastrophic](#tier-s--catastrophic)
- [Tier A — Very Harmful](#tier-a--very-harmful)
- [Tier B — Hostile But Survivable](#tier-b--hostile-but-survivable)
- [Tier C — Annoying](#tier-c--annoying)
- [Tier D — Petty](#tier-d--petty)
- [Tier F — So Bad It's a Meme](#tier-f--so-bad-its-a-meme)
- [Recently improved (off the list)](#recently-improved-off-the-list)

---

## Tier S — Catastrophic

### Apple App Store 30% commission on in-app purchases of digital goods

The "Apple Tax". Mandatory cut for any digital good or service sold
through an app distributed via the App Store. The Epic Games v. Apple
case, EU Digital Markets Act enforcement, and the UK CMA mobile
ecosystem report all document the commercial harm to small developers.

- **Receipts:** [App Store Review Guidelines §3.1.1](https://developer.apple.com/app-store/review/guidelines/#payments) · [EU DMA designation 2024](https://digital-markets-act.ec.europa.eu/gatekeepers/apple_en) · [Epic v. Apple opinion (2021, 9th Circuit affirmed 2023)](https://cand.uscourts.gov/wp-content/uploads/judges/yvonne-gonzalez-rogers-ygr/CV-20-05640-Epic-v-Apple-FoFCoL-and-Permanent-Injunction-9-10-21.pdf).
- **Why S:** Decades-long enforcement, no realistic alternative store
  on iOS in most jurisdictions, and Apple's "core technology fee"
  response to the DMA preserves the same economics under a new name.

### Google Play 30% commission on subscriptions and in-app purchases

Same model as Apple's App Store, applied to Android. Google's
position is operationally identical even as legal cases (Epic v.
Google) have reduced their effective leverage on US Android.

- **Receipts:** [Play Console payments policy](https://support.google.com/googleplay/android-developer/answer/9858738) · [Epic v. Google jury verdict (Dec 2023)](https://www.documentcloud.org/documents/24235617-epic-v-google-verdict-form).
- **Why S:** Sideloading exists on Android but is not commercially
  practical for most consumer apps. Mandatory cut on most app revenue.

### AWS data egress fees

Charging customers to leave. AWS bills outbound data transfer at
rates ranging from $0.05–0.09/GB depending on destination, with no
free tier above the modest first 100 GB. Concrete lock-in via cost
asymmetry: ingest is free, exit is expensive.

- **Receipts:** [AWS data transfer pricing](https://aws.amazon.com/ec2/pricing/on-demand/#Data_Transfer) · [EU Data Act 2024 banning egress fees in EU](https://digital-strategy.ec.europa.eu/en/policies/data-act).
- **Why S:** Multi-TB workloads cost five figures *just to migrate
  off*, before the destination provider charges for ingest. The EU
  recognised this as anti-competitive and banned it under the Data Act.

### Oracle Java SE Universal Subscription (per-employee licensing)

Since January 2023, Oracle's Java SE pricing is per-employee — every
employee, not just Java developers. A 1,000-person company with one
Java service pays for 1,000 seats.

- **Receipts:** [Oracle Java SE Universal Subscription pricing](https://www.oracle.com/java/java-se-subscription/) · [The Register coverage](https://www.theregister.com/2023/01/26/oracle_java_pricing_change/) · [Gartner advisory](https://www.gartner.com/en/documents/4022030).
- **Why S:** Forces enterprises onto OpenJDK or migration. Punishes
  the install base for Oracle's revenue targets.

### Google AI Ultra (USD 300/month) bans paying customers without explanation

Top consumer tier of Google's AI subscription. Includes Antigravity
(Google's agentic IDE). Documented pattern from early 2026:
subscribers receiving **permanent ("life") bans** with no reason
supplied, no human appeal, and no pro-rata refund on cancellation.
Triggers appear to include unusual working hours, sustained heavy
use of agentic features, and prompt patterns flagged by undocumented
classifiers. Marketed with "enterprise security" language while
operating an automated ban-bot tuned to behavioural fingerprints —
the marketing and the practice cannot both be true.

- **Receipts:** Volume of YouTube + Reddit reports peaked Feb 2026.
  Search "Google AI Ultra ban" or "Antigravity banned" for the
  pattern. Direct user data point documented by Brethof AI
  ([awesome-ai-mine entry](https://github.com/BrethofAI/awesome-ai-mine#google-antigravity--antigravity-terms-of-service-)).
- **Why S:** Top-tier paying customers losing access to their work
  with no recourse, on a product priced at the enterprise level. The
  combination of paid status + opacity + no refund is the trifecta.

### OpenAI: charity → for-profit conversion (2015 mission → 2026 reality)

OpenAI raised on an explicit non-profit charter in 2015
([Introducing OpenAI](https://openai.com/index/introducing-openai/))
promising AGI "for the benefit of humanity," "broadly distributed,"
"value for everyone rather than shareholders." The 2018
[Charter](https://openai.com/charter/) doubled down on
"primary fiduciary duty to humanity" and "providing public goods."

By 2024-2026 OpenAI has restructured into a for-profit Public
Benefit Corporation, with the non-profit losing its controlling
stake. Co-founder lawsuit
([Musk v. Altman](https://storage.courtlistener.com/recap/gov.uscourts.cand.428589/gov.uscourts.cand.428589.1.0.pdf))
alleges breach of charter; the Sep 2024 OpenAI statement
([Why our structure must evolve](https://openai.com/index/why-our-structure-must-evolve-to-advance-our-mission/))
walks the original mission back. CEO Sam Altman, who took zero
equity in the original non-profit, is now reported as a billionaire
on OpenAI's growth.

- **Receipts:** Side-by-side comparison in the
  [awesome-ai-mine OpenAI entry](https://github.com/BrethofAI/awesome-ai-mine#openai-api--api-services-agreement-2025).
- **Why S:** Sets the precedent. Charity-to-for-profit pivots used to
  be a scandal; if OpenAI normalises it, every "AI for humanity"
  pitch raised against the next AGI cycle is on the clock. Trust
  destruction at industry scale.

### Cloudflare WAF / Bot Fight Mode false-positive lockouts

Cloudflare's Bot Fight Mode and certain WAF rule packs aggressively
challenge legitimate developers, scrapers complying with `robots.txt`,
and accessibility tooling. Hidden in many "free tier" defaults of
sites Cloudflare protects.

- **Receipts:** [HN thread: Cloudflare blocking 'curl' / Tor users (2024)](https://news.ycombinator.com/item?id=39271031) · [Cloudflare's own challenge-page docs](https://developers.cloudflare.com/waf/tools/challenge-passage/) · widely-reported false positives on Wayback Machine and assistive-tech browsers.
- **Why S:** Single point of failure for a large fraction of the
  public web. Asymmetric power: site owners enable it once, every
  developer who needs to consume the site pays the cost forever.

---

## Tier A — Very Harmful

### Heroku Free Tier shutdown (Nov 2022)

Salesforce-owned Heroku ended free dynos with two months' notice,
deleting tens of thousands of student projects, demos, and
small-traffic prototypes. The de facto on-ramp for a generation of
beginners disappeared.

- **Receipts:** [Heroku blog announcement (Aug 2022)](https://blog.heroku.com/next-chapter) · [Hacker News reaction](https://news.ycombinator.com/item?id=32741636).
- **Why A:** Years of public goodwill burned for short-term cost
  savings. Trust loss across the developer community.

### Vercel hobby-tier DDoS billing exposure

Hobby (free) tier accounts have published cases of $10K+ overage
bills triggered by traffic spikes — Vercel's only recourse is "open a
support ticket". A single viral page or scraper attack can bankrupt a
side project.

- **Receipts:** [HN: Vercel charged me $96K (Jan 2025)](https://news.ycombinator.com/item?id=39059900) · [Vercel pricing model](https://vercel.com/docs/limits/usage).
- **Why A:** No hard cap option. Pricing model exposes hobbyists to
  unbounded liability for traffic they didn't request.

### npm package squatting + supply-chain attacks (typosquatting)

The npm registry's open-by-default policy allows malicious packages
named like popular ones (`lodahs` for `lodash`, etc.) to publish
freely. Documented incidents: `event-stream` (2018), `colors.js` /
`faker.js` rage-publishes (2022), `node-ipc` wartime sabotage (2022).

- **Receipts:** [event-stream postmortem (2018)](https://github.com/dominictarr/event-stream/issues/116) · [colors.js / faker.js deletion (2022)](https://research.snyk.io/blog/open-source-npm-packages-colors-faker) · [node-ipc protestware (2022)](https://snyk.io/blog/peacenotwar-malicious-npm-node-ipc-package-vulnerability/).
- **Why A:** Single dependency typo can compromise entire
  organisations. Years-long pattern with structural fixes still
  pending.

### GitHub Copilot training on user code (without explicit opt-in pre-2023)

For its first 18 months, GitHub Copilot was trained on public-repo
code that included permissively-licensed (MIT, BSD) and copyleft
(GPL) code, then offered as a paid product without crediting authors.
Pending class-action: *Doe v. GitHub*.

- **Receipts:** [Doe v. GitHub class action complaint](https://githubcopilotlitigation.com/) · [Anti-AGPL legal analysis](https://docs.fsf.org/copilot/copilot.html).
- **Why A:** Set the precedent that public source code is training
  fodder regardless of license. Industry-wide consequences.

### AWS Cost Explorer hostility

The Cost Explorer is gated behind explicit opt-in, charges
per-API-call when accessed programmatically, and surfaces real
spending only after a 24-hour delay. Designed to make cost surprises
land late.

- **Receipts:** [AWS Cost Explorer pricing](https://aws.amazon.com/aws-cost-management/pricing/) · widely-discussed pattern; see [r/aws](https://www.reddit.com/r/aws) bill-shock threads weekly.
- **Why A:** Active design choice to delay cost feedback. Surprise
  bills are a feature, not a bug, of this UX.

### Salesforce / Slack rate-limit cliffs and deprecation cycles

Slack's API tier system collapses functionality at low limits for
free / standard plans, with deprecation cycles that break working
integrations on six-month notice.

- **Receipts:** [Slack rate limits docs](https://api.slack.com/docs/rate-limits) · [2024 message-history cap on free plans](https://slack.com/blog/news/changes-to-the-slack-free-plan).
- **Why A:** Mature integrations break on a vendor's whim, often with
  no commercial path to restore behaviour beyond the highest tier.

---

## Tier B — Hostile But Survivable

### npm vs yarn vs pnpm lockfile churn

`package-lock.json`, `yarn.lock`, and `pnpm-lock.yaml` have
incompatible formats and resolution algorithms. Switching package
managers requires re-resolving the entire dependency graph and can
silently produce a different runtime.

- **Receipts:** [pnpm vs npm comparison](https://pnpm.io/feature-comparison) · [yarn berry migration guide](https://yarnpkg.com/getting-started/migration).
- **Why B:** Wastes CI minutes and onboarding time across the
  ecosystem. Each manager solves a real problem, but no migration
  story is clean.

### Docker Hub unauthenticated rate limits (100 pulls / 6h / IP)

Pulling official images from a CI runner or shared NAT exhausts the
limit fast. Workaround is mandatory account auth or pull-through
mirror, neither default.

- **Receipts:** [Docker Hub rate limits](https://docs.docker.com/docker-hub/usage/) · widely-discussed in CI vendor docs.
- **Why B:** Forces every team using Docker to architect around
  rate-limit avoidance. Predictable but a real tax.

### App Store Connect rejection process opacity

Apple's review queue regularly rejects apps for "violation of
guideline X" with no concrete artefact pointing at what triggered the
rejection. Resubmission lottery.

- **Receipts:** [r/iOSProgramming weekly rejection threads](https://www.reddit.com/r/iOSProgramming/) · [App Store rejection appeal process](https://developer.apple.com/support/app-review/).
- **Why B:** Pattern is well-known; teams budget review-cycle delays.
  The opacity itself is the harm — work without a target.

### Twilio / SendGrid surprise account suspensions

Both have a pattern of suspending accounts on automated fraud
heuristics with limited recourse. Side projects with low MRR are
disproportionately affected.

- **Receipts:** [Twilio suspension threads on HN](https://news.ycombinator.com/item?id=23937720) · [SendGrid sender-reputation policy](https://docs.sendgrid.com/ui/sending-email/sender-identity).
- **Why B:** Loss of email or SMS infrastructure mid-launch is
  catastrophic. Reinstatement is human-judgement-driven.

### Atlassian price hikes + product end-of-life cycles

Server-tier sunset (Feb 2024) forced on-prem Jira / Confluence
customers into Cloud or Data Center, with the latter at multiples of
the prior price. Pattern of pricing changes with short windows.

- **Receipts:** [Atlassian Server EoL announcement](https://www.atlassian.com/migration/journey-to-cloud) · [Data Center pricing](https://www.atlassian.com/licensing/jira-software-data-center).
- **Why B:** Migration costs are real but bounded; ecosystem accepts
  Atlassian's pricing drift as fact.

---

## Tier C — Annoying

### JetBrains "perpetual fallback license" subscription model

Annual subscription with a fallback license for the version available
12 months after first payment. Stop paying, lose new versions and
plugin compatibility.

- **Receipts:** [JetBrains licensing model](https://www.jetbrains.com/store/comparison.html) · [perpetual fallback licence terms](https://sales.jetbrains.com/hc/en-gb/articles/207240845).
- **Why C:** Better than pure SaaS rent (you keep the version you
  paid for) but the practical lock to current-version plugins makes
  the fallback aspirational.

### macOS notarization for unsigned CLI tools

Distributing a free open-source CLI via a `.pkg` requires Apple
Developer membership ($99/year) plus per-binary notarisation, even
for tools that bypass the App Store entirely.

- **Receipts:** [Apple notarization docs](https://developer.apple.com/documentation/security/notarizing-macos-software-before-distribution).
- **Why C:** Workaround exists (homebrew tap, manual `xattr -d`) but
  pushes friction onto every recipient. Tax on free software
  distribution.

### npm `audit` noise

Running `npm audit` on a typical production project surfaces dozens
of low-severity warnings — most of them in transitive dev
dependencies, unfixable from your `package.json`.

- **Receipts:** [npm audit fix limitations](https://docs.npmjs.com/cli/v9/commands/npm-audit) · [Dan Abramov on audit noise (2021)](https://overreacted.io/npm-audit-broken-by-design/).
- **Why C:** CI pipelines block on this routinely; signal-to-noise
  ratio damages real vulnerability awareness.

### React 19 / Next.js upgrade churn

Major version bumps every 18-24 months that require non-trivial
migration: server components, app-router, suspense semantics, RSC
data-fetching idioms. Each major reorganises the canonical example.

- **Receipts:** [Next.js 13 → 14 → 15 changelogs](https://nextjs.org/blog) · [React 19 RC notes](https://react.dev/blog/2024/12/05/react-19).
- **Why C:** Every rewrite is "the right way". The previous "right way"
  becomes "legacy" within a release.

### Chrome Manifest V3 extension migration

Mandatory upgrade from Manifest V2 to V3 dropped key APIs (notably
`webRequestBlocking`) used by ad-blockers. Long migration with
ambiguous deadlines, multiple delays.

- **Receipts:** [Manifest V3 transition timeline](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline) · [EFF analysis (2024)](https://www.eff.org/deeplinks/2024/05/end-near-manifest-v2-extensions).
- **Why C:** Extension authors have been on a five-year migration
  treadmill with the rules changing under them.

---

## Tier D — Petty

### npm package squatting on common names

`@types/foo` with no actual code, claimed names with placeholder
publish histories, parking common-word packages.

- **Receipts:** [npm name squatting policy](https://docs.npmjs.com/policies/dispute-resolution-and-takedowns).
- **Why D:** Rare but visible. Resolution path exists, just slow.

### "We're hiring engineers!" on every blog post that's actually about a feature

Recruiting funnel masquerading as technical content. Visible in vendor
engineering blogs across the industry.

- **Receipts:** Pattern observable on most major vendor blogs.
- **Why D:** Mild irritation. Free content is still free.

### "Login with Google" + email verification + SMS verification + captcha + AppCheck

Five-factor signup gauntlets on consumer products, justified as fraud
prevention but applied to read-only browsing.

- **Receipts:** Common pattern on YouTube comments, X verification,
  Indian / SE-Asian fintech apps.
- **Why D:** Friction tax on consumers, but developers building
  sane signup flows can avoid the trap themselves.

---

## Tier F — So Bad It's a Meme

### Oracle v. Google over Java APIs (2010-2021)

Decade-long suit over whether the Java SE API method signatures were
copyrightable. Lost at SCOTUS in 2021. Cost both companies enormous
amounts; chilled API design across the industry while it was open.

- **Receipts:** [Google v. Oracle SCOTUS opinion (2021)](https://www.supremecourt.gov/opinions/20pdf/18-956_d18f.pdf).
- **Why F:** Legal absurdity that lasted over a decade. The losing
  position was the whole point.

### "We're committed to open source" + license rug-pull

The recurring pattern: Mongo (SSPL, 2018), Redis (SSPL/RSAL,
2024-2025), HashiCorp Terraform (BSL, 2023), Elastic (SSPL/Elastic,
2021). Companies adopt source-available licences after years of
permissive distribution.

- **Receipts:** [HashiCorp BSL announcement (2023)](https://www.hashicorp.com/blog/hashicorp-adopts-business-source-license) · [Redis license change (2024)](https://redis.io/blog/redis-adopts-dual-source-available-licensing/) · [Mongo SSPL (2018)](https://www.mongodb.com/licensing/server-side-public-license).
- **Why F:** The pattern is now expected. Forks (OpenTofu,
  RedictDB / Valkey) emerge each time. Self-defeating in the long run.

### Reddit API price hike that killed third-party clients (2023)

June 2023: Reddit announced API pricing that effectively shut down
Apollo, Reddit Sync, Reddit is Fun. Apollo developer's published
costs: $20M/year if they accepted Reddit's terms.

- **Receipts:** [Apollo developer's farewell post](https://apolloapp.io/) · [Reddit's official pricing announcement](https://www.redditinc.com/blog/2023apiupdates).
- **Why F:** The community rejection (subreddit blackout, mod
  resignations) was historic but didn't reverse the policy. Reddit
  IPO'd anyway.

### Google killing products with active user bases

Reader (2013), Inbox (2019), Stadia (2023), Hangouts (2022),
domains.google (2024 → Squarespace transfer). The
[killedbygoogle.com](https://killedbygoogle.com) index documents
~290+ shuttered products as of mid-2025.

- **Receipts:** [killedbygoogle.com](https://killedbygoogle.com).
- **Why F:** Active anti-pattern: building on Google's developer
  surface area is a known risk that has not improved with time.

---

## Recently improved (off the list)

- **Discord no longer shows public emails on bot profiles** (fixed early 2024). Used to leak bot owner email addresses.
- **GitHub Copilot opt-out for code training** (added Dec 2022). Was the reason it sat in Tier A; now opt-out is straightforward.
- **AWS S3 free egress for first 100 GB** (added Dec 2024). Did not move AWS off the egress entry, but acknowledged.

## Contributing

Open an issue with: tier, practice / vendor, dated receipt URL, and
one paragraph on why it belongs at that tier. We will not list:

- Personal attacks on individuals.
- Unsubstantiated rumours.
- Practices the vendor has publicly retracted.
- Anything pre-2018 unless the policy is still active today.

If you can show a vendor has fixed something on the list, we will
move it to **Recently improved** and credit the receipt.

## Related work

- **[awesome-llms-txt](https://github.com/BrethofAI/awesome-llms-txt)** — Tools doing the right thing for AI agent users.
- **[awesome-private-ai](https://github.com/BrethofAI/awesome-private-ai)** — Tools doing the right thing for user privacy.
- **[awesome-ai-mine](https://github.com/BrethofAI/awesome-ai-mine)** — AI ToS / license analysis. Many candidate entries for this tier list live there too.

## License

[MIT](LICENSE).

---

Maintained by **[Brethof AI](https://brethof.com)** — AI tools built for
people who take their data seriously.
