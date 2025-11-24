# Abstract

U.S. Treasury securities are the canonical proxy for the risk-free rate because they carry negligible credit risk, trade in the world’s deepest and most liquid bond market, and are demanded globally as dollar reserves and cash-like assets. Their yields anchor pricing across finance, yet mark-to-market losses can arise from unexpected inflation and rate moves; long-maturity nominal yields embed real rates, expected inflation, and a term premium. 

# Glossary

* **Treasury bills (T-Bills):** 4–52 week maturities; about 20% of outstanding. Discount instruments.
* **Treasury notes:** 2–10 year maturities; bulk of outstanding.
* **Treasury bonds (“long bond”):** 20–30 year maturities.
* **Risk-free rate (proxy):** Treasury yield, used as benchmark in contracts worldwide.
* **Liquidity:** Ability to trade quickly at low cost; Treasuries are the most liquid securities market.
* **Inflation risk:** Real value of fixed nominal payoffs falls when inflation surprises high.
* **Interest-rate risk (duration):** Price falls when market yields rise before maturity.
* **Term premium:** Compensation for longer-horizon risks, including rate changes.
* **TIPS:** CPI-indexed Treasuries delivering real returns; used to infer expected inflation. 
* **Repo collateral:** Treasuries commonly pledged in overnight secured funding.

---

## Summary and enhancements

**Scale and participants.** The Treasury market is the largest debt market globally, with >\$24T outstanding as of 2020; ownership spans banks, mutual funds, insurers, pensions, the Federal Reserve, foreign investors, and cash parked in Treasury-only money market funds (> \$2T by end-2020). 

**Why Treasuries anchor “risk-free.”** Negligible default risk, exceptional liquidity, and dollar primacy make Treasuries the preferred benchmark and reserve asset; they function as cash-like instruments and high-quality repo collateral.  

**Risk is not zero before maturity.** If held to maturity, payments are certain; selling early exposes you to:

* **Inflation risk:** Higher-than-expected inflation reduces real value and market price. 
* **Rate risk:** When new-issue yields rise, prices of outstanding fixed-coupon notes fall; the effect grows with maturity (duration).

**Risk-free yield decomposition.** A nominal Treasury yield at longer maturities can be parsed as:

$$
y^{\text{nom}} \approx r^{\text{real}} + \mathbb{E}[\pi] + \text{term premium}.
$$

Real rate prices intertemporal consumption, $\mathbb{E}[\pi]$ is expected inflation, and the term premium compensates for horizon risks.

**Interaction with TIPS and breakevens.** Comparing nominal Treasuries with same-maturity TIPS yields a market-implied inflation “breakeven,” acknowledging risk premia and forecast error.

**Funding link (repo).** Treasuries’ safety and liquidity underpin the overnight repo market where they are pledged as collateral, reinforcing their role in short-term money pricing.

---

## Worked example: everything together

**Setup.** You bought a 2-year Treasury note at par with a 2% coupon. After one year you must sell. Over that year: inflation realized higher than expected, and the new 1-year T-bill rate is now 3%. 

**Price impact from rates.** Your note has one year left and pays \$2 coupon plus \$100 principal in one year. If the market discount rate for a close substitute is 3%, the fair price is

$$
P=\frac{102}{1.03}=99.029\ (<100),
$$

a capital loss vs par because yields rose.

**Real-return impact from inflation.** If you originally expected 2% inflation but it realized at 5%, a 2% nominal T-bill would have delivered $-3\%$ real ex post; the same inflation surprise also pressures Treasury market prices today.

**Decomposition view.** Today’s 1-year nominal yield reflects $r^{\text{real}}$, updated $\mathbb{E}[\pi]$, and any term premium (small at 1y), while longer maturities embed larger term premia and thus more price sensitivity.

**Why Treasuries still benchmark “risk-free.”** Default risk remains negligible, liquidity is unmatched, they serve as dollar reserves and repo collateral; hence their yields remain the baseline for discounting and performance measurement, despite interim mark-to-market volatility. 
