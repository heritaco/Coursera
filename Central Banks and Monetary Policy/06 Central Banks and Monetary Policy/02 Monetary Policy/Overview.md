# Abstract

Module 2 presents the Federal Reserve’s mandate, governance, and operating framework, then maps the toolkit that implements policy in practice. It links **targets** (maximum employment, stable prices) to **instruments** (open-market operations, discount window, reserve requirements) and to **post-2008 tools** (forward guidance, large-scale asset purchases, overnight reverse repo) that align short-term money rates and shape the yield curve when the policy rate is constrained. 

# Glossary

* **Federal Reserve System (Fed):** U.S. central bank; FOMC sets policy. 
* **Dual Mandate:** Maximum employment + stable prices; policy analysis must tie back to these goals. 
* **Money supply:** Monetary aggregates created via banking and Fed balance-sheet operations; difficult to measure precisely. 
* **Federal funds market / rate:** Overnight unsecured interbank market; main U.S. target rate. 
* **Open-market operations (OMO):** Purchases/sales of Treasuries to add/drain reserves, shifting the funds-rate equilibrium. 
* **Discount window:** Collateralized lending to banks; rate set above funds rate to cap the target range’s top. 
* **Reserve requirements:** Regulatory reserves against deposits; a traditional lever interacting with reserves and money. 
* **Forward guidance:** Statements about the **future** policy path to steer longer yields via expectations. 
* **Large-scale asset purchases (LSAP):** Central-bank buying of Treasuries/agency MBS to compress term premia when short rates are at the lower bound. 
* **ON RRP:** Overnight reverse-repo facility; sets a floor in repo markets so all short-term rates align with the policy stance. 

---

## Summary with enhancements

**Scope and logic.** The module moves from **why a central bank exists** and how the Fed is organized, to **what it optimizes** (the Dual Mandate), and finally **how it implements** that mandate through markets. All later topics connect back to employment and price stability. 

**Money supply vs interest-rate targeting.** The transcript contrasts targeting the **price of money** (the interest rate) with targeting **quantities** (money supply). Measuring money precisely is non-trivial, hence the modern emphasis on rate control while tracking monetary aggregates through the Fed’s balance sheet. Heuristically, in the overnight market,
[
i^*=\mathcal{I}\big(M_s,,M_d\big)\quad\text{with}\quad \partial i^*/\partial M_s<0,
]
so OMO that increase reserves ((M_s\uparrow)) shift the equilibrium funds rate down, and vice versa. 

**Traditional implementation.**

* **OMO:** Adjust reserves to pin the **federal funds rate** within the target range.
* **Discount window:** Liquidity backstop; its rate defines the **upper bound** of the funds-rate corridor.
* **Reserve requirements:** Shape the demand for reserves and interact with OMO.
  Together they determine the overnight equilibrium and transmit to other short rates. 

**Unconventional tools after 2008.**

* **Forward guidance:** Re-anchors expectations for the **path** of policy rates, affecting long maturities via (y_n \approx \frac1n\sum_{k=0}^{n-1}\mathbb{E}[r_{t+k}]+\text{term premium}).
* **LSAP:** Purchases of Treasuries/agency MBS expand the Fed’s assets and reduce term premia when short rates are at the effective lower bound.
* **ON RRP:** Floors repo rates; because funds and repo are close substitutes, aligning repo equilibria helps keep **all** short-term rates consistent with the stance. Core principle: the Fed targets multiple, tightly linked overnight markets, not a single quote in isolation. 

**Operating-framework insight (enhancement).** Think in **markets**, not instruments: the Desk steers the **joint** equilibrium across funds and repo so that arbitrage transmits policy **horizontally** (across money markets) while guidance and LSAP transmit **vertically** (along maturities) into the curve. 

---

## Worked example: bringing it all together

**Objective.** Inflation is running above target while labor slack is small. The FOMC raises the target range by **25 bp** and wants all overnight rates to reflect that stance the next day. 

**Step 1 — Corridor bounds.** The Board sets the **discount-window** rate above the new range. This caps upside pressure: banks won’t fund above the window rate. 

**Step 2 — Floor and cross-market alignment.** The Fed adjusts the **ON RRP** rate up 25 bp. Money funds shift cash into ON RRP if private repo pays less, so **repo rates lift**, dragging the **funds rate** with them because banks and dealers arbitrage between repo and fed funds. All overnight rates re-anchor around the new floor. 

**Step 3 — Reserves and OMO.** If the funds rate prints below target, the Desk **drains** reserves (e.g., bill sales or counterpart operations). If it prints above, the Desk **adds** reserves. Small balance-sheet moves fine-tune the midpoint inside the corridor. 

**Step 4 — Term transmission when constrained.** If later the policy rate hits the lower bound, the FOMC cannot cut further. It then deploys **forward guidance** to lower expected future short rates and **LSAP** to compress term premia, pulling down 5–10y yields without moving the overnight rate. 

**Outcome.** Overnight markets align to the new stance via ON RRP/funds/window, while guidance and LSAP propagate the stance to longer maturities. The chain from **mandate → tools → market equilibria → yields** remains intact under both “traditional” and “unconventional” regimes. 
