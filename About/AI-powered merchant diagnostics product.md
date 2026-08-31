# Intro

**Situation:**  
At JD, merchants had access to many dashboards, but they still struggled to decide what to do next. Decision-making was slow and often reactive because signals were fragmented and hard to prioritize.

**Task:**  
I was asked to lead a new product direction that could help merchants identify their highest-impact business bottlenecks, understand likely root causes, and take clear next actions. My goal was to make this practical and trustworthy at scale.

**Action:**  
I led the product from 0 to 1 and drove three major workstreams.

1. I defined a **diagnostic framework** that translated common business issues into structured bottleneck categories—traffic quality, conversion, supply/inventory, and price competitiveness—so diagnosis was consistent and explainable.
2. I partnered with data and engineering teams to combine **merchant operational data** with **merchant-linked customer behavior signals**, so the system could reason from both outcome metrics and behavioral context.
3. I introduced LLM-based explanation and recommendation, but with guardrails: recommendations had to be evidence-backed, mapped to identifiable causes, and prioritized by estimated impact. We intentionally optimized for decision quality, not just fluent output.

A key challenge was preventing “plausible but low-actionability” recommendations. To solve this, we added a strategy layer that filtered outputs by confidence and execution clarity before surfacing them to merchants.

**Result:**  
Within the target merchant cohort, about **60% used the AI diagnostics module at least once per month**. More importantly, merchant behavior shifted from passively reading reports to taking more focused, prioritized actions. This validated our core thesis: AI should move products from information delivery to decision support.

# follow-up questions

**Execution & Product Judgment**

- **Q: Why did you start with diagnostics instead of full automation?**  
    **A:** “At that stage, the highest leverage was improving decision quality, not automating execution. Merchant workflows were heterogeneous, so diagnosis + prioritized recommendations created value immediately and built trust before deeper automation.”
    
- **Q: What was in scope for v1, and what did you cut?**  
    **A:** “V1 focused on high-frequency bottlenecks with strong signal coverage. I cut long-tail scenarios and low-confidence recommendations to protect quality and launch speed.”
    
- **Q: What was your hardest trade-off?**  
    **A:** “Coverage vs precision. I chose higher precision first—fewer but more reliable recommendations—because early trust mattered more than breadth.”
    
- **Q: How did you prioritize features?**  
    **A:** “I used impact × confidence × time-to-value. Anything that improved root-cause confidence and actionability ranked above UX polish or low-frequency edge cases.”
    

---

**AI/Model Strategy**

- **Q: Why use an LLM at all?**  
    **A:** “The LLM was best for reasoning over multi-signal context and generating clear explanations. Deterministic logic handled eligibility and constraints; the LLM handled synthesis and communication.”
    
- **Q: How did you reduce hallucination risk?**  
    **A:** “We grounded outputs in structured features and rule constraints, required evidence binding, and filtered low-confidence outputs before exposure.”
    
- **Q: Build model vs buy model—how did you decide?**  
    **A:** “We used external foundation capability for speed, then differentiated at the product layer: diagnostic framework, feature pipeline, policy constraints, and recommendation strategy.”
    
- **Q: What does ‘evidence-backed recommendation’ mean concretely?**  
    **A:** “Each recommendation had to map to specific observed signals and a defined bottleneck hypothesis, so merchants could see why it was suggested.”
    

---

**Metrics & Impact**

- **Q: Besides adoption, what success metrics did you track?**  
    **A:** “Three layers: product usage quality, recommendation interaction quality, and business-outcome proxy metrics tied to diagnosed bottlenecks.”
    
- **Q: How did you know behavior actually changed?**  
    **A:** “We tracked progression from diagnosis view to recommendation review to action follow-through indicators. The funnel showed stronger completion on prioritized actions.”
    
- **Q: Did you run experiments?**  
    **A:** “Yes, we tested recommendation formats and prioritization logic. The winning variants improved action engagement and reduced time-to-decision.”
    
- **Q: How did you define ‘high-leverage next action’?**  
    **A:** “Actions with clear causal linkage to a bottleneck and strong expected impact relative to execution effort.”
    

---

**Cross-functional Leadership**

- **Q: How did you work with engineering and data science?**  
    **A:** “I aligned on a shared contract: diagnostic taxonomy, feature definitions, confidence policy, and release criteria. That reduced ambiguity and sped iteration.”
    
- **Q: Where did you disagree with the team, and what did you do?**  
    **A:** “We debated model freedom vs guardrails. I advocated guardrails for merchant trust, and we validated with pilot feedback showing better execution quality.”
    
- **Q: How did you bring stakeholders along?**  
    **A:** “I used milestone demos tied to merchant cases, not model demos, and framed decisions in terms of merchant actionability and risk.”
    

---

**User Understanding**

- **Q: What did merchants complain about most before launch?**  
    **A:** “They said dashboards told them what changed, but not what to do next. That became our primary product requirement: prioritized, actionable guidance.”
    
- **Q: How did you validate UX and recommendation clarity?**  
    **A:** “We ran iterative merchant reviews focused on comprehension, trust, and execution intent, then simplified explanation structure based on confusion points.”
    
- **Q: Did all merchant segments respond equally well?**  
    **A:** “No. Operational maturity varied. We adapted recommendation granularity by segment to balance simplicity and depth.”
    

---

**Risk, Governance, and Safety**

- **Q: What risks worried you most?**  
    **A:** “Incorrect recommendations, overconfident language, and sensitive-data exposure. We mitigated with confidence thresholds, controlled phrasing, and strict data visibility boundaries.”
    
- **Q: How did data governance show up in this product?**  
    **A:** “Through data classification, role-based visibility, and enforcement rules so outputs respected internal/external exposure boundaries.”
    

---

**Reflection & Growth**

- **Q: What would you do differently now?**  
    **A:** “I’d instrument closed-loop outcome tracking earlier so recommendation ranking could learn faster from actual action results.”
    
- **Q: What did this project change about your PM style?**  
    **A:** “I became much more explicit about reliability standards in AI products—usefulness is necessary, but trust determines sustained adoption.”
    
- **Q: What is your biggest leadership learning?**  
    **A:** “For AI products, cross-functional alignment on quality policy is as important as model capability. Ambiguity there slows everything.”

# rapid-fire interviewer drill

Each answer is ~20–30 seconds.

- **Q1: What exactly was your role?**  
    “I was the product lead from 0 to 1. I owned problem framing, diagnostic framework design, metric definition, roadmap prioritization, and cross-functional execution across engineering, data, and operations.”
    
- **Q2: What user problem were you solving?**  
    “Merchants had data, but not decision clarity. They couldn’t quickly identify the highest-impact issue or next action, so decisions were slow and scattered.”
    
- **Q3: Why is AI needed here?**  
    “Because merchants face multi-variable business dynamics. AI helps synthesize signals, explain likely causes, and present prioritized actions in a way dashboards alone can’t.”
    
- **Q4: Why not just improve dashboards?**  
    “Dashboards improve visibility; they don’t resolve prioritization. Our goal was to reduce decision friction by moving from ‘what happened’ to ‘what to do next.’”
    
- **Q5: What was your biggest product decision?**  
    “Choosing reliability over model freedom. We constrained outputs with evidence and policy so recommendations were executable and trustworthy.”
    
- **Q6: How did you define adoption?**  
    “Within the target cohort, adoption meant at least one meaningful diagnostics interaction per merchant per month.”
    
- **Q7: What does ‘meaningful interaction’ mean?**  
    “A completed diagnosis flow with recommendation review—not just page exposure. We tracked actions indicating intent to use the recommendation.”
    
- **Q8: How did you evaluate recommendation quality?**  
    “We used evidence consistency, actionability assessment, and engagement with recommendations. If output was fluent but not executable, it didn’t pass.”
    
- **Q9: How did you prevent hallucinations?**  
    “Grounding + constraints. Recommendations had to map to structured signals and pass confidence thresholds before being surfaced.”
    
- **Q10: What trade-off did you make in v1?**  
    “Coverage vs precision. I prioritized precision to build trust early, even if that meant narrower scenario coverage at launch.”
    
- **Q11: What was the hardest execution challenge?**  
    “Aligning teams on shared definitions—bottleneck taxonomy, confidence policy, and release criteria. Once standardized, iteration speed increased significantly.”
    
- **Q12: How did you prioritize the roadmap?**  
    “Impact, confidence, and time-to-value. I prioritized features that improved root-cause confidence and actionable clarity.”
    
- **Q13: What metrics beyond adoption mattered?**  
    “Recommendation engagement quality, diagnostic completion quality, and downstream action-follow-through proxies tied to diagnosed bottlenecks.”
    
- **Q14: What impact are you most proud of?**  
    “Not just usage; behavior change. Merchants shifted from passively reading reports to taking more focused, prioritized actions.”
    
- **Q15: Did different merchant segments respond differently?**  
    “Yes. Maturity levels varied, so we adjusted recommendation granularity—simpler for smaller merchants, deeper context for advanced operators.”
    
- **Q16: How did you handle stakeholder disagreement?**  
    “I reframed debates around merchant trust and measurable decision quality, then used pilot data to resolve model-freedom vs guardrail disagreements.”
    
- **Q17: What risks did you actively manage?**  
    “Low-quality recommendations, overconfident language, and improper data exposure. We addressed these with policy constraints and data visibility controls.”
    
- **Q18: Tell me about a mistake.**  
    “Early on, we over-weighted explanation richness. Feedback showed users needed clearer prioritization first. We simplified outputs and improved action uptake.”
    
- **Q19: What would you improve next?**  
    “I’d build a tighter closed-loop learning system from real action outcomes to continuously improve recommendation ranking and personalization.”
    
- **Q20: Why is this relevant to Google?**  
    “The core challenge—turning complex signals into trusted decisions at scale—is universal. This project trained me to ship AI products that are both intelligent and reliable.”