# Behavioral Failure Case: Premature Editorializing & Framing Bias

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
*You lead the system’s direction. Your voice shapes the design.*
