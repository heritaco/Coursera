# Abstract

Short-term benchmark rates transmit monetary conditions to households and firms. **LIBOR** priced unsecured interbank credit across seven tenors and became the floating leg for vast loan volumes. Survey mechanics, credit risk, and post-2008 manipulation broke confidence. **SOFR**, a transaction-based, secured overnight rate from Treasury-repo, replaced LIBOR as the preferred reference from 2022, leveraging deep liquidity and minimal credit risk.

# Glossary

* **LIBOR:** Survey-based unsecured interbank rate by currency × tenor.
* **Eurodollar loan:** USD loan booked outside the U.S.; unsecured.
* **Tenor set:** O/N, 1w, 1m, 2m, 3m, 6m, 12m.
* **Effective fed funds rate:** U.S. unsecured interbank benchmark; tracks USD LIBOR via arbitrage.
* **Floating-rate loan:** Interest = reference rate + fixed spread.
* **Basis point (bp):** 0.01%.
* **SOFR:** Secured Overnight Financing Rate on Treasury-repo, published by FRBNY; transaction-based.
* **Secured vs unsecured:** Collateralized funding (SOFR) vs no collateral (LIBOR). Credit risk embeds a spread in unsecured rates.

# Summary and improvements

1. **Origins and markets.** LIBOR comes from unsecured interbank loans across currencies; USD trades also occur in Europe as Eurodollars. SOFR comes from overnight Treasury-repo.
2. **Computation.** LIBOR used **surveys** from large panel banks because not all trade daily; SOFR uses **observed transactions**.
3. **Arbitrage parity.** USD LIBOR and the effective fed funds rate co-move; if LIBOR fell below fed funds, banks could borrow in London and lend in the U.S., compressing the gap.
4. **Use as reference.** Corporates borrow at **LIBOR + spread**; example filings show ranges like **LIBOR + 10–75 bp** for committed lines.
5. **Stress and manipulation.** Divergences from fed funds came from (i) bank credit concerns and (ii) documented survey manipulation; fines exceeded **\$9B**, and regulators moved the market off LIBOR.
6. **Transition logic.** SOFR is **secured, risk-free-like, high-volume** (≈\$1T daily as of 2020) and is now the mandated replacement reference.

# Enhancements (clearer mechanics)

* **Risk decomposition:** $\text{Unsecured rate} \approx \text{Risk-free} + \text{credit spread}$. SOFR removes most credit spread by design.
* **Why tenors mattered under LIBOR:** Term premia and expected path of policy were embedded in 1m–12m fixings; SOFR is overnight, so longer tenors are built from compounding or term constructions outside this transcript’s scope.
* **Why SOFR is harder to game:** It is based on large-scale repo transactions rather than opinion surveys.

# Worked example: bringing it all together

**Context.** A firm draws on a 30-day, \$50,000,000 revolving facility. Under the legacy document the rate is **3-month USD LIBOR + 75 bp**. Under the amended document the rate is **SOFR + spread** suitable for the same credit risk. (Illustrative numbers.)

1. **Legacy LIBOR loan.** Suppose 3m USD LIBOR fixes at **4.10%**.

   * Coupon rate = $4.10\% + 0.75\% = 4.85\%$.
   * 30/360 day-count interest = $$50{,}000{,}000 \times 0.0485 \times \frac{30}{360} = \$202{,}083$$.

2. **SOFR-based loan.** Suppose daily SOFR averages **3.80%** over the 30-day accrual and the lender quotes a **credit spread of 1.05%** to reflect unsecured borrower risk on a secured base.

   * Coupon rate = $3.80\% + 1.05\% = 4.85\%$.
   * 30/360 interest = again **\$202,083**.

**Takeaways.**

* Pricing logic is unchanged: **reference + spread**. The reference moved from unsecured, survey-based LIBOR to secured, transaction-based SOFR; the spread adjusts to keep total compensation for credit and liquidity risk consistent.
* Arbitrage keeps unsecured USD benchmarks aligned with domestic interbank costs, while the SOFR base inherits stability from Treasury-repo depth.
