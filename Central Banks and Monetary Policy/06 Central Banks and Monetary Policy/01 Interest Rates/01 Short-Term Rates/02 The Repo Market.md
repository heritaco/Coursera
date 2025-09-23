# Abstract

Short-term secured funding in the **repo market** is structured as a sale today with a contracted repurchase tomorrow of high-quality collateral, chiefly Treasuries. The market grew from the 1980s, exceeded **\$4T outstanding by end-2020**, and admits a broad lender base beyond banks, notably money market mutual funds. Core mechanics: collateralized overnight cash loans, lender protection via **haircuts**, and widespread **general collateral** baskets. Net effect: low-risk, high-liquidity funding that underpins U.S. money markets.&#x20;

# Glossary

* **Repurchase agreement (repo):** Sale of a security for cash now with an agreement to buy it back later at a higher price; economically a secured loan.&#x20;
* **Repo seller / borrower:** Obtains cash and posts the security. Title to collateral passes during the term.&#x20;
* **Repo buyer / lender:** Provides cash and holds the collateral until repurchase. Earns interest via the price differential.&#x20;
* **Collateral:** Commonly government-backed securities (e.g., Treasuries) due to negligible credit risk, stable pricing, and deep liquidity.&#x20;
* **Haircut $h$:** Discount on collateral value so the loan $L=(1-h)P_{\text{collateral}}$ is below market value; reduces lender loss if prices fall.&#x20;
* **Overnight repo:** One-day maturity; canonical tenor.&#x20;
* **General collateral (GC):** Trades executed against an eligible basket of safe government securities without naming a specific issue; lowest haircuts and most common.&#x20;
* **Federal funds market (contrast):** Unsecured, bank-only overnight market; repo participation is broader.&#x20;
* **Money market mutual funds (MMFs):** Major repo lenders who hold short-term repos instead of long-term assets.&#x20;

---

# Improved summary

## Role and scale

A central **cash** market for short-term, secured funding used by many institution types, not just banks. Outstanding volumes surpassed **\$4T by end-2020**; MMFs held about **\$1T** near end-2019. The market is the single largest cash conduit for liquidity in the U.S.&#x20;

## Mechanics

A borrower needing cash sells a Treasury today and commits to repurchase it tomorrow at a slightly higher price. Legal title transfers to the lender during the term, making the loan **secured**. The price difference embeds the **repo rate** on the cash.&#x20;

## Risk control

Main lender risk: the borrower fails to repurchase when collateral prices drop. **Haircuts** mitigate this by lending less than collateral value; determinants are collateral credit quality, price volatility, and market liquidity. Treasuries score well, so haircuts are low.&#x20;

## Collateral choice and GC

Government-backed securities dominate because they are safe, liquid, and stable. **GC repos** standardize eligibility rather than a specific security, enabling scale and low financing costs.&#x20;

## Takeaways

* Repos = **short-term secured lending** with collateral title transfer.&#x20;
* Broad access beyond banks; systemically important liquidity.&#x20;
* **Haircuts** are the key micro-prudential control making most repos near risk-free for lenders.&#x20;

---

# Worked example: end-to-end

**Setup.** GC Treasury repo, 1-day term, collateral midprice $$P_0=\$200$$. Haircut $h=2\%$.
**Loan amount.** $$L=(1-h)P_0=0.98\times 200=\$196$$.&#x20;
**Repurchase price.** Contracted $$P_1=\$200.02$$ tomorrow. Price differential on cash $=200.02-200.00$ is economically interest on the **cash lent** $L$.&#x20;

**Repo rate (simple, ACT/360):**

$$
r_{\text{daily}}=\frac{P_1-P_0}{L}
=\frac{0.02}{196}=0.0001020408
\quad\Rightarrow\quad
r_{\text{annual}}=r_{\text{daily}}\times 360\approx 3.67\%\ \text{p.a.}
$$

Interpretation: the lender earns \~3.67% annualized on the \$196 cash exposure, while holding title to the Treasury during the term. Haircut coverage: if the Treasury falls to \$199 intraday, the borrower still has incentive to repurchase; the lender remains protected so long as $$P_{\text{collateral}}>L=\$196$$.&#x20;

**Why low risk here.** GC Treasury collateral has negligible credit risk, low volatility, and high liquidity, so haircuts are modest and liquidation is feasible if needed. This is why GC repos dominate volumes and carry the lowest financing spreads.&#x20;
