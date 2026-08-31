Transaction Analysis (Single Product Diagnostic Agent)
════════════════════════════════════════════════════════════════


[Step 1] Volume & Trend
──────────────────────────────
Purpose: First assess the product's GMV absolute value and short-term trend

  ① This week's GMV absolute value
  ② 7-day / 30-day trend direction → Growth / Stable / Decline
  ③ WoW / YoY figures → Prepare data for market benchmark comparison in Step 4


[Step 2] Four-Dimension Decomposition of GMV
──────────────────────────────
Core Formula: GMV = Visitors × Conversion Rate × Price per Unit × Units per Buyer

Four dimensions mapped one-to-one:
  Traffic     → Check visitor count
  Conversion  → Check conversion rate
  Price       → Check price per unit
  Units/Buyer → No direct metric, inferred from units and buyer count:
                 Units↓ + Buyers↓   → Attribute to Traffic (fewer people = fewer units naturally)
                 Units↓ + Buyers stable → Units/Buyer dimension (same people buying fewer units)
                 Units↑ + Buyers↑   → Attribute to Traffic (more people = more units naturally)
                 Units↑ + Buyers stable → Units/Buyer dimension (same people buying more units)


[Step 3] Marginal Contribution Analysis
──────────────────────────────
Rule: A factor's marginal contribution = absolute value × rate of change, not just the rate alone

Example (decline scenario):
  Visitors 1000→800 (-20%)
  Conversion rate 2%→2.5% (+25%)
  → Although conversion rate grew more, visitor decline has greater drag on GMV

Example (growth scenario):
  Visitors 800→1000 (+25%)
  Conversion rate 2%→2.2% (+10%)
  → Visitor growth is the primary driver of GMV increase

Output: Which of the four dimensions has the largest marginal contribution (positive or negative)


[Step 4] Market Benchmark Comparison (Conditionally Activated)
──────────────────────────────
Core Principle: The market benchmark is an "elimination tool", not a "scoring tool" — first determine the product's trend pattern, then decide whether to activate benchmark comparison

Layer 1: Determine the product's trend pattern
  ▸ Pulse pattern (recent spike → pullback)
      Explanation: Likely a natural pullback after a promotion/campaign
      Action: Lower weight of market comparison, compare against historical pullback amplitude
              - Pullback ≤ historical similar pulses → Normal rhythm
              - Pullback > historical similar pulses → May have compounding issues, proceed to Layer 2

  ▸ Sustained decline (no prior spike, gradual decline)
      Explanation: Not driven by own rhythm, needs external reference
      Action: Activate market benchmark comparison, proceed to Layer 2

  ▸ Sustained growth (no pulse, steady rise)
      Explanation: Could be operational improvement or industry tailwind
      Action: Activate market comparison to determine if outperforming (own capability) or riding the market (industry tailwind)

  ▸ Stable (no significant change)
      Explanation: No problem or opportunity signal, can skip subsequent steps

Layer 2: Market benchmark comparison (only when needed)
  ① Get the product's core metrics WoW/YoY change values
  ② Get the industry benchmark's same-period WoW/YoY range (e.g., "industry WoW -8%~-3%")
  ③ Determine the product vs. market relative position (5 tiers):

    Tier                        Phenomenon                    Example                                Attribution
    Critical Alert·Divergent    Market up/flat, product down   Product -25% vs Market +5% (30pp gap)   Pure self-issue
    Warning·Major Underperform  Product decline >> market      Product -25% vs Market -8% (17pp gap)   Self-issue dominant
    Watch·Slight Underperform   Product decline > market       Product -25% vs Market -20% (5pp gap)   Partial self-issue
    Normal·Tracking Market      Decline matches market         Product -25% vs Market -25%             Market-driven
    Strong·Outperforming        Decline < market or counter    Product -10% vs Market -25% (resilient) Strong operations

  ④ Apply this comparison to each core metric:
    GMV / Visitors / Conversion Rate / AOV / Buyers / Units Sold / Price per Unit


[Step 5] Comprehensive Assessment
──────────────────────────────
Rule: Combine trend pattern (Step 4 Layer 1) + marginal contribution (Step 3) + market comparison (Step 4 Layer 2, if activated)

  Decline scenarios:
    Pulse + normal pullback         → Own rhythm, no intervention needed
    Pulse + pullback exceeds norm   → Post-campaign issues compounded with other problems, locate factors
    Sustained decline + underperforming market → High-priority problem (real issue, need to stop loss)
    Sustained decline + tracking market        → Market-driven (seasonal/industry trend)
    Sustained decline + small contribution     → Potential risk (needs attention)

  Growth scenarios:
    Pulse-type rise                → Likely short-term campaign-driven, monitor for sustainability
    Sustained growth + outperforming market → Own operational advantage, identify driver and amplify
    Sustained growth + tracking market      → Industry tailwind, monitor if sustainable after tailwind fades
    Sustained growth + concentrated driver  → Growth depends on single dimension, both risky and scalable

Output:
  ① Primary driver dimension    Traffic / Conversion / Price / Units-per-Buyer / Composite
  ② Change direction            Decline / Growth / Stable
  ③ Severity level              Critical Alert / Warning / Watch / Normal / Strong
  ④ Attribution                 Own operational issue / Own operational strength / Market factor / Mixed
  ⑤ Action direction            Stop loss / Amplify / Maintain / Observe
  ⑥ Secondary dimension         (if any)


[Step 6] Exclude Interference Factors
──────────────────────────────
Before final conclusions, exclude the following interference:

  ① Store-specific events (just ended a major promotion, clearance, stockout, system failure)
  ② Product-specific situations (listing age, seasonal factors)
  ③ Competitor major actions (link to "Competitor Analysis")


[Atom Boundary]
══════════════════════════════════════════════════════════════════
This atom only performs "entry-level" diagnosis: four-dimension decomposition + market comparison + primary driver identification + action direction guidance
Deep drill-down handled by corresponding atoms, often requiring multi-dimensional linkage (not single drill-down):

  Root Dimension    Primary Drill      Linked Drill                          Counter-intuitive Chain
  ─────────────     ─────────────      ─────────────────────────────────     ──────────────────
  Traffic           Traffic Structure   Search / Keywords / Ads / Geography   Reviews / Inventory / Compliance
  Conversion        Conversion Funnel  Keywords / Reviews / Price             Inventory / Promotions / Competitors
  Price             Price Analysis     SKU Matrix                             —
  Units/Buyer       SKU Matrix         Price                                  —

Conclusion: This atom identifies "which dimension is changing (up or down) + whether the change is reasonable (trend pattern + market elimination) + whether to stop loss or amplify + which atoms to drill into."
