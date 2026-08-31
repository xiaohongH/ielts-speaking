Traffic Structure Analysis (Single Product Diagnostic Agent)
════════════════════════════════════════════════════════════════
Prerequisite: Transaction Analysis has identified the primary issue dimension as "Traffic", requiring drill-down into traffic source structure
Data definition: Last-touch attribution, includes Level 1/2/3 channels, each with source details, audience profiles, and trend data


[Step 1] Traffic Overview
──────────────────────────────
Purpose: Assess overall traffic volume, quality, and efficiency to establish a global baseline

  ① Volume
      Total visitors (current vs. prior period)
      Total page views (current vs. prior period)
      7-day / 30-day trend direction → Growth / Stable / Decline

  ② Quality (engagement depth)
      Page views per visitor (current vs. prior period)
      Average time on product page (current vs. prior period)

  ③ Efficiency
      UV value (current vs. prior period)
      Visitor-to-purchase conversion rate (current vs. prior period)
      View-to-purchase conversion rate (current vs. prior period)
      AOV (current vs. prior period)

  ④ Diagnostic clues (overall level)
      High quality (many views / long dwell) + high conversion → Overall healthy operations
      High quality (many views / long dwell) + low conversion → Users interested but transaction barriers exist (price? stockout?)
      Low quality (few views / short dwell) + high conversion → Purpose-driven purchases (repurchase / precise traffic dominant)
      Low quality (few views / short dwell) + low conversion → Overall poor traffic quality, low audience-product fit
      Visitor CVR↓ + View CVR stable   → New visitors are imprecise, but those who browse still convert
      Visitor CVR↓ + View CVR also↓    → Overall conversion deteriorating, not just an audience issue
      Visitor CVR stable + View CVR↓   → Per-view persuasion declining (detail page quality? increased price comparison?)


[Step 2] Channel Volume & Quality Comparison
──────────────────────────────
Purpose: Compare each channel's volume, quality, and efficiency (current vs. prior period) to identify changes

  ① Volume metrics
      Referred product page visitors (current vs. prior period)
      Visitor share % (current vs. prior period)
      Referred product page views (current vs. prior period)

  ② Quality metrics (engagement depth)
      Page views per visitor (current vs. prior period)
      Average time on product page (current vs. prior period)

  ③ Efficiency metrics
      UV value (current vs. prior period)
      Visitor-to-purchase conversion rate (current vs. prior period)
      View-to-purchase conversion rate (current vs. prior period)
      AOV (current vs. prior period)

  ④ Comparative assessment
      Large volume + efficiency declining       → High-priority problem channel (high impact, getting worse)
      Large volume + efficiency stable/rising   → Core channel (maintain)
      Small volume + high efficiency            → Opportunity channel (high UV value, worth scaling)
      Small volume + efficiency trending up     → Potential channel (improving, monitor for acceleration)
      Small volume + low efficiency             → Low-efficiency channel (evaluate whether worth investing)

  ⑤ Diagnostic clues
      High quality (many views / long dwell) + high conversion → Premium channel, users both engaged and converting, worth scaling
      High quality (many views / long dwell) + low conversion → Users interested but transaction barriers (price? stockout?)
      Low quality (few views / short dwell) + high conversion → Purpose-driven / repurchase behavior (clear intent, buy on arrival)
      Low quality (few views / short dwell) + low conversion → Audience mismatch, channel attracting wrong users
      Visitor CVR↓ + View CVR stable   → New arrivals are imprecise (leave without browsing), browsers still convert
      Visitor CVR↓ + View CVR also↓    → Overall conversion deteriorating, not just an audience issue
      Visitor CVR stable + View CVR↓   → Per-view persuasion declining (detail page quality? increased comparison shopping?)


[Step 3] Channel Contribution Decomposition
──────────────────────────────
Purpose: Decompose traffic by channel, locate specific sources for problem and opportunity channels

  ① Level 1 channel decomposition
      Each L1 channel's visitor share (current vs. prior period)
      Each L1 channel's visitor change volume
      → Rank by change volume, locate primary drag channels and primary growth channels

  ② Drill down to Level 2/3 channels
      For problem channels: Within the largest-drag L1 channel, decompose L2/L3 → locate which sub-channel is declining
      For opportunity channels: Within high-UV-value L1 channels, decompose L2/L3 → locate which sub-channel is worth scaling

  ③ Source details
      Problem channel source details → Locate the finest-grain traffic change point
      Opportunity channel source details → See where growth comes from, whether replicable


[Step 4] Trend Pattern Assessment
──────────────────────────────
Purpose: Assess trend patterns for both problem and opportunity channels

  Problem channels:
    Pulse pattern (recent spike → pullback)    → Likely natural pullback after own action ends
    Sustained decline (no prior spike)         → Requires further analysis
    Stable                                     → No problem signal

  Opportunity channels:
    Sustained rise      → Trend confirmed, can increase investment
    Pulse-type rise     → May be one-off factor, monitor sustainability
    Stable              → UV value is high but volume not growing, needs active push


[Step 5] Traffic Structure Health Assessment
──────────────────────────────
Purpose: Beyond rise/fall, assess whether traffic structure has risks or opportunities (background info for LLM judgment)

  ① Channel dependency
      Whether over-reliant on a single channel (e.g., one L1 channel >70% share)

  ② Channel trend divergence
      Whether all channels trend in the same direction
      If multiple channels declining simultaneously → Likely a product competitiveness issue (not channel-specific)
      If only individual channels declining → Channel-specific issue
      If multiple channels rising simultaneously → Product competitiveness strengthening signal

  ③ Growth headroom assessment
      Opportunity channel current volume vs. similar products' volume in that channel (if market data available)
      → Assess how much scaling headroom exists


[Step 6] Operational Recommendations
──────────────────────────────
Purpose: Based on above analysis, provide traffic-level operational action recommendations

  ① Problem channel handling
      Channel traffic↓ + pulse pullback normal    → Own rhythm, no intervention needed
      Channel traffic↓ + pulse pullback excessive  → May have compounding issues, requires further investigation
      Channel traffic↓ + sustained decline         → Investigate cause (weight drop / competitor stealing / content quality)

  ② Opportunity channel amplification
      High UV value + small volume → Increase channel investment, scale up
      Quality trending up          → Monitor if sustainable, consider acceleration

  ③ Structure optimization direction
      High-conversion channel with low traffic → Increase investment in that channel
      Low-efficiency channel with high share   → Optimize channel strategy or reduce investment

  ③ Audience strategy
      Core audience declining → Targeted recall
      Audience mismatch (referred visitors don't convert) → Adjust channel targeting / content


[Atom Boundary]
══════════════════════════════════════════════════════════════════
This atom does:
  Overall traffic trend → Channel decomposition → Trend pattern assessment → Structure health evaluation → Operational recommendations

This atom does not:
  Search channel keyword-level analysis → Handled by "Keyword Analysis" atom
  Conversion funnel breakpoint identification → Handled by "Conversion Funnel" atom

Relationship with other atoms:
  Transaction Analysis (identifies Traffic-type issue) → This atom (channel-level identification) → Keyword Analysis / Ad Analysis / Geography Analysis atoms

Note:
  Audience profile analysis (channel-level audience characteristics, audience-product fit, audience structure changes) currently lacks data support, to be added after future requirements
