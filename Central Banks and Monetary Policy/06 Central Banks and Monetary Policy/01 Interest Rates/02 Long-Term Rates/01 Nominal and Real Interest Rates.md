# Abstract

Nominal rates price cash in current dollars. Real rates price intertemporal purchasing power. The Fisher relation links both through inflation. Treasury Inflation-Protected Securities (TIPS) operationalize real returns by indexing principal to the price level; their prices and yields reveal market inflation expectations.

# Glossary

* **Inflation $(\pi)$:** Rate of general price increase.
* **Nominal interest rate $(i)$:** Return measured in dollars, not adjusted for inflation.
* **Real interest rate $(r)$:** Return measured in purchasing power.
* **Fisher equation:** Exact: $(1+i)=(1+r)(1+\pi)$. Approx.: $i\approx r+\pi$.
* **TIPS:** U.S. Treasuries with CPI-indexed principal; deliver a real return by construction.
* **Breakeven inflation:** Difference between nominal Treasury yield and TIPS yield for the same maturity; a market-based gauge of expected inflation.

---

# Summary with enhancements

1. **Nominal vs real.** A bank paying 10% adds \$10 to a \$100 deposit after one year. That \$10 is nominal. Real return adjusts for the change in what \$1 buys; if prices rise 5%, purchasing-power gain is lower.
2. **Fisher relation.** Inflation connects the two: exactly $(1+i)=(1+r)(1+\pi)$, so approximately $r\approx i-\pi$ when rates are moderate. This approximation explains why 10% nominal and 5% inflation imply near-5% real.
3. **TIPS mechanics.** Principal scales with CPI. Because coupons are computed on the indexed principal, TIPS neutralize inflation’s erosion and target a real return.
4. **Expectations from prices.** When inflation protection is valuable, TIPS prices rise and TIPS yields fall relative to nominals; low expected inflation does the opposite. Comparing TIPS and nominal yields recovers market-implied inflation, acknowledging markets can be wrong.

---

# Worked example: all together

**Step 1 — Nominal vs real today.** You hold \$100. Bank pays $i=10\%$. CPI inflation $\pi=5\%$. Exact Fisher:

$$
r=\frac{1+i}{1+\pi}-1=\frac{1.10}{1.05}-1\approx 4.7619\%.
$$

In “goods” terms: if gasoline is \$4→\$4.20, \$100 buys 25 gallons now; next year \$110 buys $110/4.20\approx26.19$ gallons, a real gain of $1.19$ gallons $\approx 4.76\%$.

**Step 2 — A TIPS year.** Buy TIPS with 5% stated rate and \$100 principal. CPI rises 2%. The principal indexes to \$102; nominal return in the transcript’s simplified illustration is $5\%+2\%=7\%$. Real return equals the stated 5% because the 2% indexation offsets the 2% inflation.

**Step 3 — Market expectations.** Five-year nominal Treasury yield = 4.0%. Five-year TIPS yield = 1.6%. Breakeven $\approx 4.0\%-1.6\%=2.4\%$. Interpretation: the market is pricing about 2.4% average inflation over five years, subject to risk premia and forecast error.

**Takeaway.** Use Fisher to translate between money returns and purchasing-power returns; use TIPS structure to earn real returns and the TIPS–nominal spread to read inflation expectations.

---
Note that the TIPS yield can be negative if the stated coupon is low and/or the inflation adjustment is high. A negative real yield means the investor accepts a guaranteed loss in purchasing power, typically in exchange for safety or liquidity.

Example: If a 5-year TIPS has a 0.5% coupon and the market expects 3% annual deflation, the principal would fall over time.
Deflation has happened in the past (e.g., 2009), but is rare in the U.S. context. Other countries have experienced prolonged deflation (e.g., Japan), which can lead to negative real yields on inflation-indexed bonds.

The TIPS yield is based on the expected value of inflation, but actual inflation can differ. If actual inflation exceeds expected inflation, TIPS investors benefit from higher principal adjustments. Conversely, if actual inflation is lower than expected, TIPS investors receive lower principal adjustments, which can lead to lower overall returns compared to nominal Treasuries.

# Interpretation for today

U.S. 10 Year TIPS
US10YTIP:Exchange

+
LIVESTREAM
Shark Tank
RT Quote | Exchange | USD
Yield | 7:30 PM EDT
1.777%
UNCH
Interpretation: 1.777% is the **real yield to maturity**. If you hold this 10-year TIPS to maturity, your purchasing power grows ≈1.777% per year after CPI inflation, before taxes and fees.

Key points

* **Coupon 1.875% vs yield 1.777% → price > 100.** Since the real coupon rate exceeds the real yield, the bond trades at a small premium. Your quoted clean price 100.875 is consistent with that relation.
* **What the coupon means on TIPS.** The 1.875% is a **real coupon rate** applied to **inflation-adjusted principal**. With index ratio $I_t$ and semiannual pay,

  $$
  \text{Coupon}_t=\frac{0.01875}{2}\times 100\times I_t.
  $$
* **Invoice price you actually pay.** TIPS settle on the **inflation-adjusted** amount:

  $$
  \text{Invoice}=(\text{clean price}+ \text{accrued coupon})\times I_{\text{settle}}\quad\text{per \$100 par}.
  $$
* **Link to expected nominal return.** If expected average inflation is $\pi$,

  $$
  1+i_{\text{nom}}\approx (1+0.01777)(1+\pi)\ \Rightarrow\ i_{\text{nom}}\approx 0.01777+\pi+0.01777\,\pi.
  $$

  Example: if $\pi=2.3\%$, then $i_{\text{nom}}\approx 4.12\%$ per year.
* **Breakeven inflation.** If the 10-year nominal Treasury yield is $y^{\text{nom}}_{10}$, then

  $$
  \text{breakeven}\approx y^{\text{nom}}_{10}-1.777\%.
  $$

  Holding to maturity, the TIPS outperforms nominal Treasuries if realized CPI exceeds that breakeven; underperforms if it falls short.
