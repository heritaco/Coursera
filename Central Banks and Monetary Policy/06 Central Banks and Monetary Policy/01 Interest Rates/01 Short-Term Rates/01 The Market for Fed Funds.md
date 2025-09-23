# Federal funds market — summary + enhancements

## TL;DR

* Banks hold **required** and **excess** reserves at the Fed to meet withdrawals and surprises. Excess = liquidity buffer. &#x20;
* When a bank is short, it **borrows reserves overnight** from another bank in the **federal funds market**; these loans are **unsecured**. The rate is the **federal funds rate (FFR)**.&#x20;
* The FFR **reallocates cash across banks** and **anchors other short rates**, so it spills into loan and mortgage pricing first. &#x20;
* The Fed **controls the FFR** by adjusting the **supply of reserves** via **open market operations**.&#x20;

## Core setup

* Banks “borrow short, lend long,” so they keep reserves at the Fed to handle withdrawals and payments. **Required** reserves are legal minima; **excess** reserves cover uncertainty. &#x20;
* COVID example: firms drew ≈ **\$600B** on credit lines suddenly ⇒ banks needed cash ⇒ excess reserves proved vital.&#x20;

## Why reserves surged after 2008

* **Low rates** cut the opportunity cost of holding reserves, and the Fed **started paying interest on reserves**; crises raised banks’ desired buffers. Result: reserves jumped from ≈ **\$40B (2007)** to **\~\$3T (2014)** and **\~\$3.7T (Mar-2021)**.&#x20;

## Mechanics of the fed funds market

* Overnight, **unsecured** interbank loans of reserves; price = **FFR**.&#x20;
* **Function 1 — plumbing:** moves cash from reserve-rich to reserve-poor banks to meet loan demand.&#x20;
* **Function 2 — pricing:** if FFR rises, banks demand higher rates on new loans; spillover strongest to **short-maturity** assets, which are closest substitutes for overnight cash.&#x20;

## Policy lever

* The Fed **steers FFR** by changing reserve supply (**OMO**), using it to hit macro goals later in the course.&#x20;
* Module framing: repo, LIBOR/SOFR, Treasuries, term structure, MMMFs, and securitization are the other links in the chain you’ll study next.  &#x20;

## Quick mental model

* **Choice for a bank:** hold reserves (safe, low return) **vs.** make loans (higher return, less liquidity). The gap is the **opportunity cost** of excess reserves.&#x20;
* **Policy pass-through:** ↑FFR ⇒ ↑money-market rates ⇒ ↑bank funding costs ⇒ ↑loan/mortgage rates (first at short maturities).&#x20;

## Common pitfalls (fixed)

* “FFR only matters for banks.” Correction: it **anchors** many short-dated prices economy-wide.&#x20;
* “Reserves were always huge.” No. They were tiny pre-2008; the post-crisis regime changed the scale.&#x20;

**One check:** if the FFR jumps, which loan rates should move first in your view, and why?


**Speed ranking (fast → slow)**

1. **Overnight/short-term wholesale:** SOFR, fed funds, ON RRP, T-bills, overnight repo, 1–3m CDs/CP.
2. **Administered/posted:** bank **prime** rate; **floating-rate** loans tied to SOFR/prime (credit cards, some HELOCs).
3. **New issue fixed-rate credit:** new mortgages/auto/corp bonds (via MBS and long Treasuries).
4. **Existing fixed-rate loans:** basically unchanged; price effect shows up if you **refi** or sell.

**Why:** funding costs and close substitutes move first; longer maturities add duration, prepayment, and term-premium dynamics; retail pricing has menu frictions and competition.

Quick check: after a Fed hike **today**, which adjusts by tomorrow morning—**SOFR**, **prime**, or an **existing 30-year fixed mortgage rate**?

Right away: **expected future short rates dominate.**

Why:
- New 30-yr mortgage quotes track **MBS/10-yr Treasury**, not the 30-yr point; average mortgage life ≈ 5–10y due to prepayments.  
- Pricing: \(y(\tau)=\frac{1}{\tau}\sum_{k=1}^{\tau}\mathbb E[i_{t+k}]+\text{term premium}\). FOMC moves + guidance shift \(\mathbb E[i_{t+k}]\) **immediately**.  
- **Term premium** moves with risk appetite, supply/QE, and convexity hedging. It matters, but it drifts or jumps episodically; the **first-day move** is usually expectations.

Quick mental model:
- Day 0 surprise dovish signal → 10y ↓ mostly via lower path of short rates; MBS spread may compress a bit later.
- QE/taper news → term premium leg does more of the work.

Check: If the Fed signals faster cuts next year but makes **no** balance-sheet change, what should happen to **new** fixed-rate mortgage quotes tomorrow?


Short answer: **new fixed-rate mortgage quotes would likely fall tomorrow** if the Fed signals faster cuts next year **and** the balance sheet is unchanged. That signal lowers the *expected path of future short rates*, which pulls down 10-year Treasury and MBS yields; the term-premium piece shouldn’t move much without a balance-sheet action.

# What “balance sheet” means here

Any balance sheet: **Assets = Liabilities + Equity**.

**Central bank balance sheet**

* **Assets:** Treasuries, MBS, repo loans, emergency facilities.
* **Liabilities:** currency in circulation, **bank reserves**, **ON RRP** balances.
* **QE (LSAPs):** buys more assets → assets ↑, reserves ↑. Usually compresses the **term premium**.
* **QT:** lets assets run off/sells → assets ↓, reserves ↓. Usually lifts the **term premium**.
* Saying “no balance-sheet change” ⇒ you’re *not* using QE/QT to push the term premium; only expectations of future short rates move.

# “Dovish” (and its opposite)

* **Dovish:** prefers easier policy. More tolerant of inflation in the short run, prioritizes growth and employment, signals **lower/earlier cuts**.
* **Hawkish:** prefers tighter policy. Prioritizes disinflation, signals **higher/longer rates**.

# Putting it together

* **Dovish signal (no QE/QT):** expectations channel does the work → long yields down → **new** 30-yr mortgage quotes down.
* **Dovish + QE:** expectations ↓ *and* term premium ↓ → bigger drop in long yields → mortgage quotes fall more.
* **Hawkish signal:** the mirror image.

Quick check (one line): If the Fed is dovish *but* announces **faster QT**, what happens to long yields *net*—down, up, or ambiguous?

Ambiguous. The dovish signal pushes long yields down via expectations, but faster QT pushes the term premium up. The net effect depends on which force is stronger.

**Term premium** = the extra yield on a long-term bond above the average path of expected short rates. It is compensation for risks you take by locking money in for years.

**Core decomposition**

$$
y_t(\tau)=\underbrace{\frac{1}{\tau}\sum_{k=1}^{\tau}\mathbb{E}_t[i_{t+k}]}_{\text{expected future short rates}}+\underbrace{\mathrm{TP}_t(\tau)}_{\text{term premium}}
$$

**Numerical feel**

* If the 10y yield is 3.8% and the market’s average expected short rate over 10y is 3.2%, then $\mathrm{TP}\approx 0.6\%$.
* Post-QE episodes sometimes saw **negative** TP (investors accept less yield because duration is scarce and safe assets are in demand).

**What moves it**

* **QE/QT:** QE removes duration → TP ↓. QT adds duration → TP ↑.
* **Risk appetite/uncertainty:** higher macro and inflation uncertainty → TP ↑.
* **Supply/demand:** heavy Treasury issuance or fewer duration buyers → TP ↑.
* **Liquidity/market frictions:** worse liquidity → TP ↑.
* **MBS convexity hedging:** can push TP around when rates jump.

**Why you care**

* Long mortgage and Treasury rates move with both pieces. Guidance changes expectations; balance-sheet and supply changes move TP.

Quick check (one line): if uncertainty about future inflation rises sharply but policy guidance is unchanged, what happens to the term premium?


Short version: **QE lowers the term premium; QT raises it.** Why? **Supply of long-duration risk.**

* **Term premium (TP)** = extra yield investors demand to hold **long** bonds because they’re more sensitive to rate moves (**duration risk**).
* **QE (Fed buys long bonds):** fewer long bonds left for the public → less duration risk to hold → investors require **less** extra yield → **TP ↓** → long yields ↓ (if expectations unchanged).
* **QT (Fed lets bonds roll off/sells):** more long bonds for the public → more duration risk to absorb → investors require **more** extra yield → **TP ↑** → long yields ↑ (if expectations unchanged).

Think **chairs game**:

* QE = Fed removes chairs (long bonds) from the room. More people chasing fewer chairs → chair **prices up** → bond **yields down** → **TP down**.
* QT = Fed puts chairs back. More chairs to sit on → prices **down** → yields **up** → **TP up**.

Tiny numbers:

* Before: expected short-rate path = **3.0%**, TP = **1.0%** ⇒ 10y ≈ **4.0%**.
* After **QE**: TP → **0.6%** ⇒ 10y ≈ **3.6%**.
* After **QT**: TP → **1.4%** ⇒ 10y ≈ **4.4%**.
  (Expectations stayed at 3.0% in all three.)

One check: with **QT** and unchanged expectations, does the **10-year yield** go **up** or **down**?

Yes. At any moment the supply is **finite**. Two useful views:

**1) Total outstanding vs free float**

* **Total outstanding:** all bonds issued and not yet matured.
* **Free float:** total outstanding **minus** holdings parked with “buy-and-hold” owners (central bank QE portfolio, foreign CBs, index funds, insurers, banks’ HQLA).
* QE **cuts free float**, so the private sector holds fewer long bonds. That is what “fewer long bonds left for the public” means.

**2) Duration-weighted supply (what moves term premium)**

* Not all bonds add the same “long-rate risk.” Use **10-year equivalents**:

  $$
  \text{10y-eq}_i \;=\; \frac{D_i}{D_{10}}\times \text{Notional}_i
  $$

  Buying \$100B of 30-years removes **more** 10y-eq duration than \$100B of 2-years. QE that targets the long end shrinks **duration supply** the most ⇒ term premium falls.

**Can the supply grow?**

* **Treasury** can issue more at auctions, but not instantly on demand. It follows a calendar and debt-management plans.
* **The Fed does not issue Treasuries.** It buys or sells in the secondary market, changing **who** holds duration, not the government’s total debt that day.

**Implications**

* QE: free float ↓, duration supply ↓ ⇒ term premium ↓.
* QT or heavy new issuance: free float ↑, duration supply ↑ ⇒ term premium ↑.

Quick check: does QE change **who holds** long-duration risk, or does it reduce the **government’s** total debt?
