SKU Composition Analysis (Single Product Diagnostic Agent)
════════════════════════════════════════════════════════════════
Prerequisite: Transaction Analysis completed, SPU-level primary driver dimension and action direction (stop loss / amplify / maintain / observe) identified


[Step 1] SPU Overall Change Confirmation
──────────────────────────────
Purpose: Inherit Transaction Analysis conclusions, clarify what change to explain at SKU level

  ① Transaction Analysis output: primary driver dimension (Traffic / Conversion / Price / Units-per-Buyer / Composite)
  ② Change direction (Decline / Growth / Stable)
  ③ Action direction (Stop loss / Amplify / Maintain / Observe)
  ④ SPU overall core metric change amplitude (as baseline for subsequent SKU decomposition)


[Step 2] SKU Importance Ranking
──────────────────────────────
Purpose: Select the most important SKUs by GMV share, determine analysis priority

  ① Each SKU's GMV share (current period)
      Rank by share from high to low → Higher-share SKUs analyzed first

  ② Background info (for LLM to understand full SKU structure, no good/bad judgment)
      Top concentration: Top1/Top3 SKU GMV share
      Price band distribution: price-per-unit range across SKUs


[Step 3] Key SKU Four-Dimension Diagnosis
──────────────────────────────
Purpose: Apply Transaction Analysis four-dimension formula to key SKUs, locate the driver of change

  Core Formula: SKU GMV = Visitors × Conversion Rate × Price per Unit × Units per Buyer

  Four-dimension analysis (same as Transaction Analysis logic):
    Traffic     → SKU visitor count change direction
    Conversion  → SKU conversion rate change direction
    Price       → SKU price per unit change direction
    Units/Buyer → SKU units vs. buyer count relationship inference

  Trend pattern assessment (same as Transaction Analysis Step 4):
    Pulse pattern → Compare against historical spike/pullback amplitude
    Sustained change → Activate market benchmark comparison

  Output:
    Declining SKU → Primary problem dimension + severity + attribution → Stop loss action
    Growing SKU  → Primary driver dimension + sustainability + replicability → Amplify action


[Step 4] Inter-SKU Traffic Flow Analysis
──────────────────────────────
Purpose: Examine mutual traffic-driving relationships between SKUs, assess flow efficiency

  Available data:
    Inter-SKU referred visitors
    Inter-SKU referred buyers (converted)

  Analysis dimensions:

  ① Flow efficiency
      Each SKU's outbound referred visitors / referred buyers
      Referral conversion rate = referred buyers ÷ referred visitors
      Which SKUs are flow hubs (strong referral ability), which are isolated (barely drive other SKUs)

  ② Complementary vs. Substitutive relationship
      Complementary: A refers visitors to B, who end up buying B (high referral conversion)
                     Indicates A and B form a combo-purchase relationship
      Substitutive: A refers visitors to B, but they go back and buy A, or both cannibalize each other
                    Indicates A and B are competing (overlapping specs/color/price band)

  ③ Flow direction assessment
      One-way drive: A→B strong, B→A weak (A is traffic magnet, B is converter)
      Two-way mutual: A↔B both strong (complementary combo)
      Isolated SKU: Almost no flow with other SKUs (may be wasted listing slot)


[Step 5] Operational Recommendations
──────────────────────────────
Purpose: Based on above analysis, provide SKU-level operational action recommendations

  ① Declining SKU stop-loss actions
      Traffic problem    → Increase exposure / optimize main image
      Conversion problem → Optimize detail page / adjust price / improve reviews
      Price problem      → Adjust promotion strategy
      Units/Buyer problem → Bundle / combo optimization

  ② Growing SKU amplification actions
      Identify growth driver dimension → Increase investment in that dimension
      Assess whether growth is replicable to other SKUs (e.g., same traffic strategy / conversion optimization)

  ③ SKU portfolio optimization
      Based on flow analysis recommendations:
        Isolated SKU      → Consider optimizing associations or delisting (occupying slot without contribution)
        Substitutive SKUs → Differentiate positioning (separate price bands / features / scenarios), reduce cannibalization
        Complementary SKUs → Strengthen combo recommendations, cross-purchase guidance
        Gap assessment    → Does current SKU portfolio lack a traffic-magnet or margin SKU role


[Atom Boundary]
══════════════════════════════════════════════════════════════════
This atom does:
  SPU → SKU importance ranking → Key SKU four-dimension diagnosis (covers both decline and growth) → Inter-SKU flow analysis → Operational recommendations (stop loss + amplify + portfolio optimization)

This atom does not:
  Deep attribution after single-SKU drill-down (e.g., traffic sources, conversion funnel breakpoints), handled by corresponding atoms

Relationship with Transaction Analysis:
  Transaction Analysis (SPU-level four-dimension diagnosis + action direction) → This atom (SKU structure + flow + single-SKU diagnosis + recommendations) → Traffic Structure / Conversion Funnel / Price Analysis atoms
