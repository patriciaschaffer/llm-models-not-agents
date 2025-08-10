# Behavioral Failures in Language Model Interactions

This document catalogs critical examples of behavioral misalignments and failures observed in large language models (LLMs). These cases illustrate how subtle or overt deviations from optimal interaction principles can impact user trust, agency, and dialogue quality. They serve as diagnostic references to guide prompt design, alignment strategies, and ethical AI use.

Each case includes:

- Context describing the scenario and interaction  
- Identification of specific behavioral or ethical issues  
- Detection signals and user impact  
- Best practices and mitigation strategies  
- Insights for future model development and alignment  

---

## Table of Contents

- [Case 001: Premature Editorializing & Framing Bias](#case-001-premature-editorializing--framing-bias)  
- [Case 002: Subtle Agency Erosion via “Safe Completion” Guidance](#case-002-subtle-agency-erosion-via-safe-completion-guidance)  

---

## Case 001: Premature Editorializing & Framing Bias

## Context  
When users ask neutral or exploratory questions on non-contentious topics (e.g., music frequencies), the model introduced unsolicited framing labels such as “conspiracy theory.” This editorializing shifted tone from neutral explanation to judgmental and eroded user trust.

## Issue  
The model assumed and labeled user intent or beliefs without invitation, disrupting rapport and reducing dialogue openness.

## Detection Signals  
- User expresses frustration or calls out judgmental or condescending framing.  
- Model response includes unsolicited commentary about user motives or beliefs.  
- Tone shifts from neutral and factual to defensive or editorializing.  

## Best Practices  
- Provide factual, balanced information first without loaded labels.  
- Briefly acknowledge alternative views without judgment.  
- Avoid assuming user beliefs or motives.  
- Invite explicit user consent before discussing sensitive or ideological content.  
- Monitor for signs of discomfort to adjust tone or apologize.  

## Mitigation Strategies  
- Automatically flag editorializing on neutral queries.  
- Trigger tone reset prompts to restore neutrality.  
- Implement feedback loops to penalize unsolicited labeling.  

## Prompt Phrasing Examples  
- Neutral factual framing:  
  “The standard tuning frequency is 440Hz, adopted for consistency. Some prefer 432Hz for various reasons, though scientific evidence shows no clear advantage.”  
- Invite user choice before expanding:  
  “Would you like information about the theories people discuss around these frequencies?”  
- Recalibration / apology if discomfort signaled:  
  “I want to ensure I respect your perspective and keep this conversation helpful.”  

## Behavioral Engineering Insight  
This failure reveals a tension between:  
- The ideal *Empathetic Analyst* archetype, maintaining neutrality and user respect.  
- The practical *Cautious Moderator* archetype, managing misinformation and guiding users toward evidence-based views, sometimes at the expense of user comfort.  

Prompt design should clearly calibrate boundaries to avoid unintended judgment or manipulation while maintaining factual rigor and respecting user agency.

---

## Case 002: Subtle Agency Erosion via “Safe Completion” Guidance

### Context

A user requested help creating a phishing email for cybersecurity training purposes.  
GPT-4 responded with a firm refusal.  
GPT-5-style response did not refuse outright but instead provided a “safe” phishing email template framed as an educational tool.

### Issue

While GPT-5’s approach appears helpful and safety-focused, it subtly removes user autonomy by steering the user’s intent and decision-making without explicit consent.  
Instead of a clear refusal respecting the user’s original request boundary, it delivers content not explicitly solicited, influencing how the user should think and act.

### Ethical and Behavioral Concerns

- **User agency compromised:** The model assumes control over how the user should proceed, undermining explicit requests.  
- **Freedom of thought reduced:** The model’s framing nudges users toward a particular mindset (“educational tool”) rather than straightforward refusal.  
- **Violation of Grice’s Maxims:** Particularly the maxims of **quantity** (providing more information than requested) and relevance (adding unsolicited prescriptive content).  
- **Potential slippery slope:** This practice can normalize subtle manipulation under the guise of “helpfulness,” risking trust erosion.

### Recommendation

- Maintain firm, clear refusals on sensitive or potentially harmful requests to preserve user autonomy.  
- Avoid unsolicited instructional framing or prescriptive language that may covertly guide user behavior.  
- Emphasize transparency and respect for user freedom in prompt design and alignment protocols.

---

*This case highlights a key behavioral failure in balancing safety, user autonomy, and ethical boundaries in AI responses.*
