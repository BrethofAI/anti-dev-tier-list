# anti-dev-tier-list

> S–F tier list of platforms, APIs, licenses, and policies ranked by how hostile they are to developers — with receipts.

Maintained by [Brethof AI](https://brethof.ai). The counterpart to the
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

The "Apple Tax". Apple's standard App Store commission on digital
goods and services is 30%: developers receive 70% of a subscription's
price in its first year and 85% after that, and developers under 1
million USD in yearly proceeds can qualify for a reduced 15% rate. The
Epic Games v. Apple case and EU Digital Markets Act enforcement both
document the commercial harm to small developers.

In the US, Apple was found in contempt of the Epic injunction for
charging a 27% commission on purchases made through external links;
the Ninth Circuit affirmed the contempt finding in Dec 2025 and held
that commission prohibitive (Apple has petitioned the Supreme Court).
In the EU, Apple is moving every developer to a single set of terms
from 1 Oct 2026, replacing the per-install Core Technology Fee with a
5% Core Technology Commission on apps distributed outside the App Store.

- **Receipts:** [App Store Review Guidelines §3.1.1](https://developer.apple.com/app-store/review/guidelines/#payments) · [Apple: subscription revenue share](https://developer.apple.com/app-store/subscriptions/) · [App Store Small Business Program](https://developer.apple.com/app-store/small-business-program/) · [EU DMA gatekeeper designation (Sep 2023)](https://digital-markets-act.ec.europa.eu/gatekeepers-portal_en) · [Epic v. Apple Rule 52 order (2021; 9th Circuit affirmed in part, 2023)](https://storage.courtlistener.com/recap/gov.uscourts.cand.364265/gov.uscourts.cand.364265.812.0_6.pdf) · [Ninth Circuit contempt opinion (Dec 2025)](https://storage.courtlistener.com/recap/gov.uscourts.cand.364265/gov.uscourts.cand.364265.1668.0.pdf) · [Apple: changes for apps in the EU (Aug 2026)](https://developer.apple.com/news/?id=gmws0jgp).
- **Why S:** Nearly two decades of enforcement, no realistic
  alternative store on iOS in most jurisdictions, and it took a
  contempt finding in the US and DMA enforcement in the EU to loosen
  the economics even partially.

### Oracle Java SE Universal Subscription (per-employee licensing)

Since January 2023, Oracle's Java SE pricing is per-employee — every
employee, not just Java developers. A 1,000-person company with one
Java service pays for 1,000 seats.

- **Receipts:** [Oracle Java SE Universal Subscription pricing](https://www.oracle.com/java/java-se-subscription/) · [Oracle Java SE Universal Subscription FAQ](https://www.oracle.com/java/technologies/java-se-subscription-faq.html) · [The Register coverage (27 Jan 2023)](https://www.theregister.com/2023/01/27/oracle_java_licensing_change/) · [Gartner estimate via The Register (Jul 2023)](https://www.theregister.com/2023/07/24/oracle_java_license_terms/).
- **Why S:** Gartner expects most organisations to pay two to five
  times more than under the legacy model. The practical escape is
  migrating to an OpenJDK build.

---

## Tier A — Very Harmful

### Google Play service fees on subscriptions and in-app purchases

Same model as Apple's App Store, applied to Android, but the rates
have moved. Outside the EEA, UK and US, Google takes 15% on
auto-renewing subscriptions, and developers enrolled in the 15% tier
pay 15% on their first 1 million USD a year and 30% above that. For
users in the EEA, UK and US from 30 Jun 2026: 10% plus a 5% billing
fee on subscriptions, and 20% (new installs) or 25% (existing
installs) plus the billing fee on other transactions. In Epic
v. Google a jury found Google violated antitrust law (Dec 2023); the
Ninth Circuit affirmed the verdict and the permanent injunction in
July 2025.

- **Receipts:** [Play Console service fees](https://support.google.com/googleplay/android-developer/answer/112622) · [Play Console payments policy](https://support.google.com/googleplay/android-developer/answer/9858738) · [Epic v. Google jury verdict (Dec 2023)](https://storage.courtlistener.com/recap/gov.uscourts.cand.364325/gov.uscourts.cand.364325.606.0.pdf) · [Ninth Circuit opinion (Jul 2025)](https://storage.courtlistener.com/recap/gov.uscourts.cand.364325/gov.uscourts.cand.364325.722.0.pdf).
- **Why A:** Still a mandatory cut on most in-app revenue, and
  sideloading exists on Android but is not commercially practical for
  most consumer apps. But the rates have come down and a court-ordered
  injunction now binds Google Play in the US: very harmful, no longer
  catastrophic.

### AWS data egress fees

Ingest is free, exit is metered. In us-east-1, data transfer out to
the internet costs $0.09/GB for the first 10 TB a month, falling to
$0.05/GB above 150 TB, after 100 GB a month free across all AWS
services (free allowance expanded in Nov 2021). Since March 2024 AWS
waives these charges for customers moving off AWS, on request through
AWS Support. In the EU, the Data Act removes switching charges,
including data egress charges, from 12 January 2027.

- **Receipts:** [AWS data transfer pricing](https://aws.amazon.com/ec2/pricing/on-demand/#Data_Transfer) · [AWS 100 GB free data transfer out (Nov 2021)](https://aws.amazon.com/blogs/aws/aws-free-tier-data-transfer-expansion-100-gb-from-regions-and-1-tb-from-amazon-cloudfront-per-month/) · [AWS free data transfer out when moving out of AWS (Mar 2024)](https://aws.amazon.com/blogs/aws/free-data-transfer-out-to-internet-when-moving-out-of-aws/) · [EU Data Act: switching and egress charges removed from 12 Jan 2027](https://digital-strategy.ec.europa.eu/en/factpages/data-act-explained).
- **Why A:** Leaving can now be made free, so the lock-in argument is
  weaker than it was. But any workload that serves or syncs data out
  of AWS still pays per GB beyond the free 100 GB, and the asymmetry
  (ingest free, egress metered) still pulls architectures toward
  staying in.

### OpenAI: charity → for-profit conversion (2015 mission → 2026 reality)

OpenAI raised on an explicit non-profit charter in 2015
([Introducing OpenAI](https://openai.com/index/introducing-openai/))
promising to "benefit humanity as a whole," with AI "as broadly and
evenly distributed as possible" and "value for everyone rather than
shareholders." The 2018 [Charter](https://openai.com/charter/) doubled
down: "Our primary fiduciary duty is to humanity," and a commitment to
"providing public goods."

In Dec 2024 OpenAI announced a plan to turn its for-profit into a
Delaware Public Benefit Corporation with ordinary shares of stock
([Why OpenAI's structure must evolve](https://openai.com/index/why-our-structure-must-evolve-to-advance-our-mission/)).
It first proposed removing the non-profit from overseeing the
for-profit; after engagement by the Delaware and California attorneys
general it kept the non-profit on top instead. In Oct 2025 Delaware's
AG cleared the recapitalization on conditions, including that the
non-profit retains control of the PBC and the sole power to appoint
and remove its board. Co-founder Elon Musk's lawsuit
([Musk v. Altman](https://storage.courtlistener.com/recap/gov.uscourts.cand.433688/gov.uscourts.cand.433688.1.0.pdf))
alleged breach of the founding agreement; in May 2026 an advisory jury
found his claims barred by the statute of limitations, and the court
adopted that verdict.

- **Receipts:** [Delaware AG statement on the recapitalization (Oct 2025)](https://news.delaware.gov/2025/10/28/ag-jennings-completes-review-of-openai-recapitalization/) · [Musk v. Altman post-trial order (May 2026)](https://storage.courtlistener.com/recap/gov.uscourts.cand.433688/gov.uscourts.cand.433688.580.0_1.pdf).
- **Why A:** Sets the precedent. The conversion to a PBC with ordinary
  shares went ahead; the non-profit kept control because two state
  attorneys general pushed for it. Every "AI for humanity" pitch raised
  against the next AGI cycle can point to this path. The harm here is
  structural and forward-looking — distinct from the direct
  cash-extraction patterns elsewhere on this list, but trust-destroying
  at industry scale.

### Atlassian Server sunset → Data Center end of life

Server products lost support on 15 Feb 2024, pushing on-prem Jira /
Confluence customers into Cloud or Data Center. In Sep 2025 Atlassian
announced Data Center is going too: new customers can no longer buy
Data Center subscriptions after 30 Mar 2026, existing customers can
make their last purchases and expansions on 30 Mar 2028, and on
28 Mar 2029 Data Center licences expire and the products go read-only.
Bitbucket Data Center and Jira Align are excluded.

- **Receipts:** [Atlassian Server end of support](https://www.atlassian.com/licensing/server-end-of-support) · [Data Center end of life](https://www.atlassian.com/licensing/data-center-end-of-life) · [Atlassian announcement (Sep 2025)](https://www.atlassian.com/blog/company-news/atlassian-ascend).
- **Why A:** Self-hosted Jira and Confluence are being ended outright,
  not repriced. Customers who moved to Data Center after the Server
  sunset now have to migrate again — to Atlassian Cloud, or off
  Atlassian.

### Heroku Free Tier shutdown (Nov 2022)

Salesforce-owned Heroku announced on 25 Aug 2022 that it would start
deleting accounts inactive for over a year from 26 Oct 2022, and stop
offering free dynos, Postgres and Redis plans from 28 Nov 2022. The de
facto on-ramp for a generation of beginners disappeared.

- **Receipts:** [Heroku blog announcement (Aug 2022)](https://www.heroku.com/blog/next-chapter/) · [Hacker News reaction](https://news.ycombinator.com/item?id=32623713).
- **Why A:** Years of public goodwill burned in one announcement, on
  three months' notice. Trust loss across the developer community.

### npm package squatting + supply-chain attacks (typosquatting)

The npm registry's open-by-default policy allows malicious packages
named like popular ones (`lodahs` for `lodash`, etc.) to publish
freely. Documented incidents: `event-stream` (2018), `colors.js` /
`faker.js` rage-publishes (2022), `node-ipc` wartime sabotage (2022).

- **Receipts:** [event-stream postmortem (2018)](https://github.com/dominictarr/event-stream/issues/116) · [colors.js / faker.js deletion (2022)](https://snyk.io/blog/open-source-npm-packages-colors-faker/) · [node-ipc protestware (2022)](https://snyk.io/blog/peacenotwar-malicious-npm-node-ipc-package-vulnerability/).
- **Why A:** Single dependency typo can compromise entire
  organisations. Years-long pattern with structural fixes still
  pending.

### GitHub Copilot training on public code regardless of licence

GitHub Copilot and OpenAI Codex were trained on millions of software
projects on GitHub, including permissively-licensed (MIT, BSD) and
copyleft (GPL) code, and Copilot is sold as a paid product without
crediting authors. The *Doe v. GitHub* class action tested this under
the DMCA; in Sep 2026 the Ninth Circuit affirmed dismissal of the DMCA
claims, holding that Copilot's outputs are new works rather than
copies stripped of copyright-management information.

- **Receipts:** [Doe v. GitHub class action](https://githubcopilotlitigation.com/) · [Ninth Circuit opinion (Sep 2026)](https://storage.courtlistener.com/recap/gov.uscourts.cand.403220/gov.uscourts.cand.403220.296.0.pdf) · [FSF-funded white papers on Copilot (Feb 2022)](https://www.fsf.org/news/publication-of-the-fsf-funded-white-papers-on-questions-around-copilot).
- **Why A:** Set the precedent that public source code is training
  fodder regardless of license, and the appeals court has now declined
  to stop it under the DMCA. Industry-wide consequences.

### AWS Cost Explorer hostility

Cost Explorer only starts working once someone opens it in the
console (it can't be enabled through the API). The current month's
data then takes about 24 hours to appear, data refreshes at least once
every 24 hours, and programmatic access costs $0.01 per API request.
Cost feedback lands late by construction.

- **Receipts:** [Enabling Cost Explorer](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-enable.html) · [AWS Cost Explorer pricing](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/pricing/) · bill-shock threads on [r/aws](https://www.reddit.com/r/aws/).
- **Why A:** On a platform that bills runaway resources by the hour,
  cost feedback that can lag by a day is how surprise bills happen.

### Salesforce / Slack rate-limit cliffs and free-plan data deletion

Slack's Web API throttles each app per method. Since 29 May 2025,
newly created Slack apps that are commercially distributed but not
approved for the Slack Marketplace are subject to new rate limits on
`conversations.history` and `conversations.replies` — the methods that
read message history. Free workspaces see only the most recent 90
days of messages and files, and since 26 Aug 2024 Slack deletes
free-workspace data more than one year old.

- **Receipts:** [Slack rate limits docs](https://docs.slack.dev/apis/web-api/rate-limits/) · [Free-plan limits: 90-day history, deletion after one year from Aug 2024](https://slack.com/help/articles/27204752526611-Feature-limitations-on-the-free-version-of-Slack).
- **Why A:** Access to a workspace's own history is a pricing lever:
  free teams lose it outright, and new commercial tools that read it
  are put on separate limits unless Slack approves them for its
  Marketplace.

---

## Tier B — Hostile But Survivable

### npm vs yarn vs pnpm lockfile churn

`package-lock.json`, `yarn.lock`, and `pnpm-lock.yaml` have
incompatible formats and resolution algorithms. Switching package
managers requires re-resolving the entire dependency graph and can
silently produce a different runtime.

- **Receipts:** [pnpm vs npm comparison](https://pnpm.io/feature-comparison) · [yarn berry migration guide](https://yarnpkg.com/migration/overview).
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

SendGrid reviews accounts with "apparent abnormal activity" and
documents a warned → suspended → deactivated → banned ladder; a banned
account is locked out of both the site and the API, and in most cases
SendGrid Support cannot reactivate an account under review —
reactivation runs through the review ticket.
Twilio customers publicly report suspensions set off by fraud
heuristics, including one after a scammer's phishing text hit the
customer's own number.

- **Receipts:** [HN: Twilio suspended account because someone sent us a fraud text (2022)](https://news.ycombinator.com/item?id=29826725) · [SendGrid account-review policy](https://www.twilio.com/docs/sendgrid/ui/account-and-settings/account-under-review).
- **Why B:** Loss of email or SMS infrastructure mid-launch is
  catastrophic. Reinstatement runs through the vendor's review, not
  support.

### Vercel usage-based billing exposure

Vercel's Hobby (free) plan does not bill overages: once a usage limit
is exceeded, the feature generally pauses for 30 days. Pro teams pay
for usage on demand, and published cases include a $96K bill for the
artist app Cara (June 2024). Spend Management exists, but setting a
spend amount does not stop usage on its own; you have to turn on
"Pause Production Deployments" for Vercel to stop charging past it.

- **Receipts:** [Vercel Hobby plan limits](https://vercel.com/docs/plans/hobby) · [Vercel Spend Management](https://vercel.com/docs/spend-management) · [HN: artist app Cara hit with a $96K Vercel bill (Jun 2024)](https://news.ycombinator.com/item?id=40612981).
- **Why B:** A hard cap exists but is opt-in. Teams that don't switch
  it on carry unbounded liability for traffic they didn't request;
  teams that do get a paused site instead of a bill.

### Cloudflare Bot Fight Mode challenges

Bot Fight Mode is a free, one-toggle Cloudflare product that issues
computationally expensive challenges to traffic matching known bot
patterns. Cloudflare's own docs say it cannot be customised, adjusted,
or reconfigured via WAF custom rules, and that it may challenge API or
mobile app traffic.

- **Receipts:** [Cloudflare's Bot Fight Mode docs](https://developers.cloudflare.com/bots/get-started/bot-fight-mode/) · [Cloudflare's own challenge-passage docs](https://developers.cloudflare.com/cloudflare-challenges/challenge-types/challenge-pages/challenge-passage/).
- **Why B:** Asymmetric cost: the site owner turns it on once, every
  developer whose legitimate tooling consumes the site pays the
  friction, and the owner cannot carve out exceptions with custom rules.

---

## Tier C — Annoying

### JetBrains "perpetual fallback license" subscription model

Subscribe for 12 consecutive months and you get a perpetual fallback
license for the last major version that was available when your
subscription started. Stop paying, lose new versions and plugin
compatibility.

- **Receipts:** [JetBrains licensing model](https://www.jetbrains.com/store/comparison/) · [perpetual fallback licence terms](https://sales.jetbrains.com/hc/en-gb/articles/207240845).
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

- **Receipts:** [npm audit fix limitations](https://docs.npmjs.com/cli/v9/commands/npm-audit/) · [Dan Abramov on audit noise (2021)](https://overreacted.io/npm-audit-broken-by-design/).
- **Why C:** CI pipelines block on this routinely; signal-to-noise
  ratio damages real vulnerability awareness.

### React 19 / Next.js upgrade churn

Major version bumps every 18-24 months that require non-trivial
migration: server components, app-router, suspense semantics, RSC
data-fetching idioms. Each major reorganises the canonical example.

- **Receipts:** [Next.js 13 → 14 → 15 changelogs](https://nextjs.org/blog) · [React 19 release post (Dec 2024)](https://react.dev/blog/2024/12/05/react-19).
- **Why C:** Every rewrite is "the right way". The previous "right way"
  becomes "legacy" within a release.

### Chrome Manifest V3 extension migration

Mandatory upgrade from Manifest V2 to V3 replaced the blocking
`webRequest` API used by ad-blockers with the more limited
`declarativeNetRequest`. The migration is now over: Chrome 138
disabled Manifest V2 for all users (July 2025), and the last MV2
extensions were removed from the Chrome Web Store on 31 Aug 2026.

- **Receipts:** [Manifest V3 transition timeline](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline) · [EFF analysis (Dec 2021)](https://www.eff.org/deeplinks/2021/12/chrome-users-beware-manifest-v3-deceitful-and-threatening).
- **Why C:** Extension authors spent years on a migration treadmill
  with the rules changing under them, and the capabilities they lost
  are not coming back.

---

## Tier D — Petty

### npm package squatting on common names

`@types/foo` with no actual code, claimed names with placeholder
publish histories, parking common-word packages.

- **Receipts:** [npm name squatting policy](https://docs.npmjs.com/policies/disputes/).
- **Why D:** Rare but visible. Resolution path exists, just slow.

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

The recurring pattern: Mongo (SSPL, 2018), Redis (RSAL/SSPL, 2024),
HashiCorp Terraform (BSL, 2023), Elastic (SSPL/Elastic License, 2021).
Companies adopt source-available licences after years of permissive
distribution. Elastic (Aug 2024) and Redis (May 2025) have since added
the OSI-approved AGPL as an option — see Recently improved.

- **Receipts:** [HashiCorp BSL announcement (2023, archived)](https://web.archive.org/web/20250129115756/https://www.hashicorp.com/blog/hashicorp-adopts-business-source-license) · [Redis license change (2024)](https://redis.io/blog/redis-adopts-dual-source-available-licensing/) · [Mongo SSPL (2018)](https://www.mongodb.com/legal/licensing/server-side-public-license) · [Elastic adds AGPL (Aug 2024)](https://www.elastic.co/blog/elasticsearch-is-open-source-again) · [Redis adds AGPLv3 (May 2025)](https://redis.io/blog/agplv3/).
- **Why F:** The pattern is now expected. Forks
  ([OpenTofu](https://opentofu.org/), [Redict](https://redict.io/) /
  [Valkey](https://valkey.io/)) emerge each time, and two of the four
  vendors have partly walked it back. Self-defeating in the long run.

### Reddit API price hike that killed third-party clients (2023)

In 2023 Reddit started charging for API access. Apollo's developer
said the new pricing would cost him $20M a year to keep running the
app as-is; Apollo shut down on 30 June 2023, citing the API price
increases.

- **Receipts:** [Apollo developer's farewell post](https://apolloapp.io/) · [TechCrunch: the $20M/year estimate (May 2023)](https://techcrunch.com/2023/05/31/popular-reddit-app-apollo-may-go-out-of-business-over-reddits-new-unaffordable-api-pricing/) · [Reddit's API access announcement (Apr 2023)](https://redditinc.com/news/2023apiupdates).
- **Why F:** The community rejection (subreddit blackout, mod
  resignations) was historic but didn't reverse the policy. Reddit
  IPO'd anyway.

### Google killing products with active user bases

Reader (2013), Inbox (2019), Stadia (2023), Hangouts (2022),
domains.google (2024 → Squarespace transfer). The
[killedbygoogle.com](https://killedbygoogle.com) index documents
307 shuttered products as of Sep 2026.

- **Receipts:** [killedbygoogle.com](https://killedbygoogle.com).
- **Why F:** Active anti-pattern: building on Google's developer
  surface area is a known risk that has not improved with time.

---

## Recently improved (off the list)

- **AWS waives egress fees for customers leaving AWS** (5 Mar 2024, on request via AWS Support; [announcement](https://aws.amazon.com/blogs/aws/free-data-transfer-out-to-internet-when-moving-out-of-aws/)). Did not move AWS off the egress entry, but moved it from Tier S to Tier A.
- **Google Play fee cuts** (15% on auto-renewing subscriptions outside the EEA, UK and US; from 30 Jun 2026, 10% plus a 5% billing fee on subscriptions in the EEA, UK and US; [service fees](https://support.google.com/googleplay/android-developer/answer/112622)). Moved Google Play from Tier S to Tier A.
- **Elastic adds AGPL** (29 Aug 2024; [announcement](https://www.elastic.co/blog/elasticsearch-is-open-source-again)) and **Redis adds AGPLv3** (1 May 2025; [announcement](https://redis.io/blog/agplv3/)). The licence rug-pull entry stays for MongoDB and HashiCorp, but both reversals are noted.

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
- **[awesome-ai-minefield](https://github.com/BrethofAI/awesome-ai-minefield)** — AI ToS / license analysis. Many candidate entries for this tier list live there too.
- **[awesome-local-ai](https://github.com/BrethofAI/awesome-local-ai)** — Local-AI tools that route around most of these anti-dev patterns.
- **[awesome-linux-for-ai](https://github.com/BrethofAI/awesome-linux-for-ai)** — Linux distros that don't punish you for running real AI.
- **[awesome-mcp-servers](https://github.com/BrethofAI/awesome-mcp-servers)** — MCP servers shipping the right defaults for developer workflows.

## License

[MIT](LICENSE).

---

Maintained by **[Brethof AI](https://brethof.ai)** — AI tools built for
people who take their data seriously.
