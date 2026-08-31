Search Analysis (Single Product Diagnostic Agent)
════════════════════════════════════════════════════════════════
Prerequisite: Traffic Structure Analysis has identified the search channel as a problem or opportunity channel, requiring drill-down into search performance
Data definition: Daily granularity, supports period-over-period comparison


[Step 1] Search Overview
──────────────────────────────
Purpose: Assess overall search channel performance to establish baseline

  Core Formula: Search GMV = Impressions (unique users) × Search CTR × Search CVR × AOV

  ① Volume metrics (current vs. prior period)
      Impressions (total) / Impressions (unique users)
      Clicks (total) / Clicks (unique users)
      Buyers / Orders / Units sold / GMV

  ② Efficiency metrics (current vs. prior period)
      Search CTR (click-through rate)
      Search CVR (conversion rate)
      AOV

  ③ Competitiveness metrics
      Category ranking (current vs. prior period)
      Final price (current vs. prior period)


[Step 2] Funnel Decomposition
──────────────────────────────
Purpose: Locate bottleneck using "Impression → Click → Purchase" funnel

  Three funnel layers:
    Impression layer → Check impression (unique users) change
    Click layer      → Check search CTR change
    Purchase layer   → Check search CVR change

  Marginal contribution analysis (same as Transaction Analysis logic):
    Each layer's contribution share to search GMV change
    → How much from impressions, how much from CTR, how much from CVR, how much from AOV

  Identify primary driver layer:
    Impressions↓ dominant   → Impression problem (search weight / ranking decline)
    Search CTR↓ dominant    → Click problem (main image / title / price lacking appeal in search results)
    Search CVR↓ dominant    → Conversion problem (detail page / reviews / price competitiveness insufficient)
    AOV↓ dominant           → Price problem (promotion / discount depth change)

    Impressions↑ dominant   → Impression opportunity (ranking improvement / search weight strengthened)
    Search CTR↑ dominant    → Click advantage (main image / title / price appeal strengthened)
    Search CVR↑ dominant    → Conversion advantage (detail page / reviews / price competitiveness improved)
    AOV↑ dominant           → Price increase (AOV rise driving GMV growth)


[Step 3] Layer-by-Layer Deep Diagnosis
──────────────────────────────
Purpose: Further analyze causes for both problem and advantage layers, determine if stop-loss or amplification is possible

  ▸ Impression layer
    Decline scenario:
      Is category ranking declining → Ranking drop directly impacts impressions
      Final price change → Price competitiveness affects platform search weight
      Impressions per user = Total impressions ÷ Unique impression users
        Rising → Repeated exposure but audience pool not expanding
        Falling → Exposure opportunities decreasing
    Growth scenario:
      Is category ranking improving → Ranking rise brings more impressions
      Has final price decreased → Price competitiveness boost driving weight
      Impressions per user change → Determine if audience pool expanded or per-user exposure increased

  ▸ Click layer
    Decline scenario:
      Search CTR declining period-over-period
      Has final price changed → Price is the most intuitive decision factor on search results page
      Has category ranking changed → Lower ranking naturally yields lower CTR
      Possible causes: main image appeal, title relevance, price display, competitor interception
    Growth scenario:
      Search CTR rising period-over-period
      Has final price decreased → Price advantage driving CTR improvement
      Has category ranking improved → Higher ranking provides position advantage
      Identify driver: main image optimization? price adjustment? competitor exit? → Is it sustainable

  ▸ Purchase layer
    Decline scenario:
      Search CVR declining period-over-period
      Has final price changed → Price directly impacts purchase decision
      Clicks per user = Total clicks ÷ Unique click users
        Rising → Users viewing repeatedly but not buying (hesitating / comparing)
        Falling → Users either leaving after one view or buying immediately
      Possible causes: detail page persuasiveness, review reputation, price competitiveness, stock status
    Growth scenario:
      Search CVR rising period-over-period
      Has final price changed → Price reduction driving conversion
      Clicks per user change → Decrease means faster decision-making (trust improved / price persuasive)
      Identify driver: price adjustment? review improvement? detail page optimization? → Can it be replicated to other channels


[Step 4] Trend Pattern Assessment
──────────────────────────────
Purpose: Determine whether change is own rhythm or a trend requiring attention

  Pulse pattern (recent spike → pullback)   → Likely natural pullback after promotion/campaign ends
  Sustained decline (no prior spike)         → Requires further analysis, may indicate competitiveness decline
  Sustained growth (steady rise)             → Identify driver, assess if sustainable amplification possible
  Stable                                     → No significant signal

  Category ranking + final price linkage assessment:
    Ranking↓ + Price↑       → Price competitiveness decline causing weight drop
    Ranking↓ + Price stable → May be competitor strengthening or platform rule change
    Ranking↑ + Impressions flat → Ranking improved but search pool shrinking (industry search volume declining)


[Step 5] Comprehensive Assessment & Operational Recommendations
──────────────────────────────
Purpose: Based on funnel analysis results, provide search-level operational recommendations

  ① Impression issues
      Ranking declining → Optimize search weight (improve CVR, review scores, price competitiveness)
      Price increase causing weight drop → Evaluate pricing strategy
      Industry search volume declining → Not a self-issue, focus on other traffic channels

  ② Click issues
      CTR↓ + Price↑       → Price competitiveness insufficient, evaluate if repricing needed
      CTR↓ + Price stable → Main image / title needs optimization, or competitor images more appealing
      CTR↓ + Ranking↓     → Lower ranking causing position disadvantage

  ③ Conversion issues
      CVR↓ + Price↑       → Price resistance increased
      CVR↓ + Price stable → Detail page / reviews / competitor factors
      CVR↓ + Users clicking repeatedly → Users hesitating/comparing, need stronger persuasion

  ④ Opportunity amplification
      CTR↑ / CVR↑ → Identify driver (price adjustment? main image optimization?)
      Ranking↑    → Seize momentum, invest more to push for higher ranking
      Layer efficiency far above historical → Assess sustainability


[Atom Boundary]
══════════════════════════════════════════════════════════════════
This atom does:
  Search overall performance → Impression / Click / Purchase funnel decomposition → Layer-by-layer deep diagnosis → Trend assessment → Operational recommendations

This atom does not:
  Specific keyword-level analysis → Handled by "Keyword Analysis" atom
  Detail page conversion breakpoints → Handled by "Conversion Funnel" atom
  Competitor search strategies → Handled by "Competitor Analysis" atom

Relationship with other atoms:
  Traffic Structure Analysis (identifies search channel problem/opportunity) → This atom (search funnel diagnosis) → Keyword Analysis / Conversion Funnel / Competitor Analysis atoms
