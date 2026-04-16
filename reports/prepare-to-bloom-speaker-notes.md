# AI as a Tool, Not an Oracle -- Speaker Notes

**Event:** Prepare to Bloom AI Workshop
**Date:** April 15, 2026, 9am PT / 12pm ET
**Format:** 40 min presentation + 20 min Q&A
**Audience:** ~9 therapeutic consultants (IECA/TCA members), post-TCA keynote
**Presenter:** Eric Falke, ThriveIEP
**Host:** Shayna Abraham, Prepare to Bloom

---

## Slide 1: Title -- "AI as a Tool, Not an Oracle"

**Open (Shayna introduces Eric, then hand off)**

"Thanks, Shayna. I'm Eric, co-founder and chief product and technology officer at ThriveIEP. We build tools that help clinical and educational professionals work with sensitive documents more safely and more efficiently.

Today I'm going to walk you through how we think about AI -- not as a magic box, but as a tool with real strengths and real limits. And I'll use the Bloom report as a concrete example, because it's the product Shayna and I built together, and it shows exactly where AI helps and where it needs guardrails.

This session is for people who are curious about AI but want to understand it before they trust it. You don't need any technical background."

---

## Slide 2: Poll -- "How are you using AI today?"

**Quick show of hands or chat responses. Don't dwell -- 60 seconds max.**

"Before we dive in, I'd love to get a read on the room. Just a quick show of hands:"

- Not yet / Occasionally / Mostly for writing / Sometimes with documents

"Great. Wherever you are is the right starting point. Everything I'm going to show you today builds from first principles -- we'll start with what AI actually is and work forward from there.

One thing I want to name upfront: AI is already being used in your space. The question isn't whether to engage with it. The question is how to engage with it well."

---

## Slide 3: Task -- "The real task is not 'use AI'"

**Reframe: the work comes first, the tool comes second.**

"Forget AI for a moment. Think about the actual work.

You have a student. You have a stack of documents -- psych evals, discharge summaries, IEPs, treatment notes, maybe some call notes. Typically 5 to 10 documents, sometimes more. Each one written by a different person, at a different time, for a different purpose.

Your job is to read all of that, make sense of it, and produce something concise -- a placement report that helps families, admissions directors, and treatment teams understand what this student needs and why.

That's hard, skilled work. It takes hours. And the stakes are real -- this report shapes where a young person goes next."

**Key number to land:** "The output is about 2 pages. The input might be 50, 80, 100 pages of source material. The value isn't in summarizing -- it's in deciding what matters."

---

## Slide 4: Brainstorm -- "How would you do it by hand?"

**This is interactive. Give the audience 2-3 minutes. Let them generate the problem.**

"Here's what I want to try. Before I show you anything about how we built this, I want you to think about how *you* would approach it.

If someone handed you 6 documents for a new case and said 'write the placement report,' what would you do first?"

**Prompt if needed:**
- "What would you read first? The most recent doc? The psych eval?"
- "How would you organize the information? A mental timeline? Sticky notes?"
- "Where would you worry about getting something wrong?"

**Listen for these themes (they will come up):**
- Privacy ("I can't just upload this anywhere")
- Contradictions ("What if two evaluators disagree on diagnosis?")
- Missing context ("What if there's no parent interview?")
- Overwhelm ("There's too much to hold in my head at once")

**Bridge to the architecture:** "Every single concern you just named -- privacy, contradictions, missing data, too much information -- those are the exact design problems we had to solve. The Bloom report architecture exists because we took those problems seriously."

---

## Slide 5: First Principles -- "AI from first principles"

**This is the Feynman moment. Keep it simple and concrete.**

"Here's the simplest honest description of what AI like Claude actually is:

**It's a brilliant intern with limited desk space and no filing cabinet.**

It can read beautifully. It can write beautifully. It can synthesize patterns across a large amount of text. Those are real, valuable capabilities.

But it has three important limits:"

1. **No durable memory.** "When you start a new conversation, it doesn't remember the last one. It has no filing cabinet. Everything it knows has to be in front of it right now."

2. **Limited desk space.** "There's a limit to how much text it can hold at once -- we call this the context window. If you paste in too many documents, it starts losing the thread. Like reading through a mail slot."

3. **Confident even when wrong.** "This is the big one. AI generates text by predicting what comes next. It doesn't 'know' things the way you know them. It will write something that sounds authoritative and polished -- and it might be wrong. A date shifted by a year. A diagnosis attributed to the wrong evaluator. We call this hallucination, but a simpler name is: fluent doesn't mean true."

**The punchline:** "These aren't bugs that will be fixed in the next version. They're features of how the technology works. So the question becomes: how do you use something powerful that has these specific limits? Answer: you build a system around it."

---

## Slide 6: Context Limits -- "Why 'just put it into Claude' breaks down"

**Connect directly to their experience.**

"How many of you have tried putting a long document into ChatGPT or Claude and gotten something back that felt... vaguely right but not actually useful?"

**Name the two failure modes:**

- **Too much context:** "You paste in everything. The model gives you a polished summary that smooths over the details that actually matter. It blends information across documents. It sounds good but doesn't serve the case."

- **Not enough context:** "You ask it to write a placement report, but it doesn't know your professional standards. It doesn't know BBI pillars. It doesn't know what 'least restrictive environment' means in practice. So it writes something generic."

"This is the paradox: generic AI often fails because there's simultaneously too much and not enough context. Too much raw data, not enough structure and guidance.

That's what we set out to solve."

---

## Slide 7: Case Study -- "The Bloom case study"

**This is where the Shayna partnership story comes in.**

"Shayna and I started working together because she had a real problem. She was writing these placement reports by hand -- reading stacks of documents, synthesizing them, writing concise reports that follow IECA and TCA best practices, BBI principles, level of care criteria.

The question wasn't 'Can AI write?' The question was: 'Can we build a system that supports good clinical judgment?'

That meant sitting down together and answering questions that are fundamentally clinical, not technical:"

1. **Messy source docs:** "Different authors, different dates, different levels of reliability. A discharge summary from 2023 might contradict an IEP from 2025. Who do you trust?"

2. **Short final output:** "The report needs to be about 2 pages -- concise enough that an admissions director actually reads it. Not a data dump."

3. **Practice-specific lens:** "The report has to answer specific placement questions: What must the milieu handle daily? Why is higher care indicated? What are the family's needs? Those questions come from clinical expertise, not AI training data."

---

## Slide 8: Report Goals -- "What the report has to do"

**Briefly walk through the four qualities.**

"Every Bloom report has to be four things:

- **Concise** -- about 1,200 words. Not a 20-page summary. A decision tool.
- **Grounded** -- every clinical claim traces back to a source document. If the report says 'eight incidents in three weeks,' you can see exactly which document that came from.
- **Useful** -- each section answers a specific placement question. 'Needs and Challenges' answers 'What must staff handle daily?' Not just a diagnosis list.
- **Family-centered** -- the student and family stay visible throughout. This isn't a clinical abstract. It's a document that families read."

**The quote to land:** "A good summary is not just accurate. It's decision-useful. That distinction shaped every design choice."

---

## Slide 9: Pipeline -- "The pipeline matters"

**Walk through the 5 steps. Use the Emily Fung run as concrete illustration.**

"Here's what happens when documents are uploaded for a student. I'll use a real case -- anonymized -- where we processed 4 documents through the pipeline:

**Step 1: Redact and minimize** (deterministic -- no AI)
The redaXtor strips personally identifiable information before documents enter the broader system. Names, dates of birth, facility names, addresses. This is pattern matching and trained detection models -- no AI guessing.

**Step 2: Extract** (AI -- Sonnet model)
Each document is read separately. The AI pulls out structured claims: diagnoses, medications, placement events, risk indicators, strengths. Each claim gets tagged with exactly which document it came from.

In our reference case, this produced 300 individual claims across 4 documents. Total time: about 6 minutes, running all documents in parallel.

Why separately? Because if the AI reads all documents at once, it starts blending. A discharge summary mentions a prior placement -- the AI 'fills in' details from another document. By processing each one alone, the evidence stays clean.

**Step 3: Reconcile** (deterministic -- no AI)
Now we have 300 claims. We build the timeline. When dates conflict, we follow clinical source hierarchy rules:

| Conflict | Trust | Why |
|----------|-------|-----|
| Placement names and sequence | Parent/family report | Lived experience |
| Admission/discharge dates | Facility's own records | Source knows own dates |
| Student ages | Computed from DOB | Never trust stated ages |
| Diagnostic conclusions | Each evaluator's report | Note convergence/divergence |

These are Shayna's clinical rules, encoded in code. Not AI opinion. This step took 2 milliseconds.

**Step 4: Synthesize** (AI -- most powerful model, Opus)
Only after all data is validated and organized does the powerful model see it. It gets clean, pre-organized data and produces the 9-section report. This is the one step where we use the most capable AI model -- and it runs exactly once.

Time: about 2 minutes. The model sees pre-validated data, so it's focused on writing well, not on figuring out what's true.

**Step 5: Check** (mostly deterministic)
After the AI writes, code checks it: Are all 9 sections present? Do all 86 grounded claims trace back to real source documents? Are there zero ungrounded claims? Is the formatting correct?

In our reference case: 29 out of 30 quality checks passed. The one miss? Word count was 1,541 instead of the target 1,400 max. That's a tuning issue, not a clinical error."

**The punchline:** "We don't ask one model to freestyle the whole case. We break it into smaller tasks, use AI only where it's genuinely needed, and check the output."

---

## Slide 10: AI vs Code -- "Where AI helps. Where code helps."

**Reinforce the principle with the split.**

"Here's the simple version:

**Generative AI is good at:**
- Synthesizing across documents
- Drafting readable prose at an appropriate reading level
- Turning structured evidence into narrative

**Deterministic code is good at:**
- Routing the right context to the right step
- Timeline reconciliation and date math
- Enforcing format rules (all 9 sections present, no formatting errors)
- Quality checks and gates

The phrase I'd leave you with: **Generative AI needs a harness.** The harness is not anti-AI. It's what makes AI useful. A language engine inside a controlled system."

---

## Slide 11: Hallucinations -- "Fluent is not the same as true"

**Don't be scary. Be practical.**

"Hallucination is not a mystery. It's a predictable failure mode. AI generates text by predicting what should come next based on patterns. Sometimes the prediction is wrong -- and because AI is always fluent, wrong outputs sound just as confident as right ones.

In clinical documents, this can mean:
- A date shifted by a year
- A diagnosis attributed to the wrong evaluator
- A placement described that didn't actually happen
- Details 'borrowed' from one document and attributed to another

The answer is not to panic or avoid AI entirely. The answer is better workflow design:

- **Ground:** Use real source material, not vague prompting
- **Narrow:** Give the model smaller, cleaner tasks
- **Check:** Verify important claims before trusting the output

In our reference case, the pipeline checked 300 extracted claims for cross-document contamination. Zero flags. That's what grounding and isolation give you."

---

## Slide 12: Context Management -- "Give the right folder at the right time"

**This is the 'so what' slide -- why the file system matters.**

"Remember the filing cabinet problem? AI has no durable memory. So we built one.

**A: Guidelines.** IECA principles, TCA standards, BBI pillars, level of care criteria -- these live in files that get loaded into the system when the AI needs them. The AI doesn't have to 'know' your standards from training data. We give it the authoritative source at the right moment.

**B: Report structure.** The 9-section format, the guiding questions each section must answer -- these are held outside the AI and applied as constraints. You can customize the format by changing the file, not retraining a model.

**C: Case facts.** The AI sees only the evidence relevant to the step it's performing. Not every file at once. Stage 2 sees one document. Stage 4 sees the reconciled, structured profile. No stage sees everything.

This is why the file system matters: it lets us apply professional guidelines, customize report format, and reduce the confusion that causes errors. It's the filing cabinet the AI doesn't have on its own.

**For your own work:** Even if you're using Claude directly, this principle applies. Save your professional guidelines as a text document. Build a 'system prompt' that describes what you need. Give the AI the right context, not all the context."

---

## Slide 13: Privacy -- "Protect privacy by design"

**Lead with their concern. The TCA keynote generated the most questions here.**

"I know the number one question after the TCA conference was about HIPAA and FERPA compliance. Let me address that directly.

When you paste a document into ChatGPT or Claude directly, that text goes to a server. Even with privacy policies, you are sending client information to a third party. That's a real risk.

Our approach has three layers:

- **Minimize:** Don't expose more information than the task requires. The AI doesn't need the student's real name to write a good report.
- **Redact:** Use a purpose-built tool -- we call it the redaXtor -- to strip personally identifiable information before AI processing. Names, DOBs, SSNs, facility names, addresses, phone numbers.
- **Control exposure:** Be intentional about which systems see what data and when.

HIPAA and FERPA compliance isn't only about server infrastructure. It's also about habits, workflows, and minimization. The best security practice is: don't send data that doesn't need to be sent."

**On contract disclosure:** "Some of you are wondering: do I need to tell families I'm using AI? The answer depends on your state and professional guidelines. But the architecture we've built makes this conversation easier: the AI never sees identifying information. Your clinical judgment drives every decision point. AI is a drafting tool, not a decision-maker."

---

## Slide 14: Redactor -- "The redaXtor is a bridge to safer AI use"

**Make it concrete.**

"The redaXtor is a separate tool we built for document redaction. It's not AI generating new text -- it's detection and removal.

It uses two approaches:
- **Deterministic pattern matching** for structured PII: SSNs, phone numbers, dates, email addresses. These follow known formats.
- **Trained entity recognition models** for unstructured PII: names, facility names, cities. These require context to identify.

Why it matters for this audience:
- It reduces the manual burden of redaction. You're not going through 80 pages with a marker.
- It makes privacy protection practical at scale. If you're processing 6 documents for a case, you need automated help.
- It's the bridge that makes AI workflows possible for sensitive documents. Without redaction, every AI workflow is a privacy risk.

For many professionals, privacy is the barrier to AI adoption. The redaXtor lowers that barrier."

---

## Slide 15: Best Practices -- "Use AI well"

**Close with practical, take-home value.**

"Let me leave you with five things you can do right now, regardless of what tools you use:

1. **Be specific about the task.** Don't say 'summarize this.' Say 'summarize this psych eval, focusing on findings relevant to residential placement. Note safety concerns and failed lower-level interventions.'

2. **Give relevant context, not all context.** If you're using Claude directly, include your professional standards in the prompt. Tell it what framework you're working within.

3. **Ask for a draft, not a final truth.** Frame AI output as a starting point that you will review, not a finished product.

4. **Check important claims.** Verify dates, ages, facility names, and diagnostic conclusions against the source documents. Those are the things AI gets wrong most often.

5. **Keep humans in the loop.** The value of AI in clinical work is that it handles the synthesis labor. The value of you is that you bring judgment, context, and ethical responsibility that no model has."

**Discussion close (transition to Q&A):**

"I'd love to hear from you:
- Where do you lose the most time in your current workflow?
- Where do you need more consistency?
- What would you want AI to help with first?"

**Closing line:** "Use AI with structure. Use AI with judgment. Use AI with care. Thank you."

---

## Appendix: Key Facts for Q&A

### Pipeline numbers (Emily Fung reference case, April 12, 2026)
- 4 documents ingested
- 300 claims extracted, 0 cross-contamination
- 86 grounded claims in final report, 0 ungrounded
- 27 inline citations
- 82 timeline events across all 4 documents
- 29/30 quality checks passed
- Total processing time: ~8.7 minutes
- Only the synthesis step uses the most powerful (and expensive) model

### Source hierarchy (for conflict resolution questions)
| Conflict | Trust | Why |
|----------|-------|-----|
| Placement names/sequence | Parent/family report | Lived experience |
| Admission/discharge dates | Facility's own records | Source knows own dates |
| Student ages | Computed from DOB | Never trust stated age |
| Diagnostic conclusions | Each evaluator's report | Note convergence/divergence |

### HIPAA/FERPA talking points
- AI never sees real names (redaXtor strips PII first)
- Data minimization: only send what the task requires
- Clinical judgment remains with the human at every decision point
- Pipeline halts for human input when factual conflicts can't be resolved automatically
- Contract disclosure depends on state/professional guidelines; the architecture supports transparency

### Report structure (9 sections, each answering a guiding question)
1. Background -- How did this student arrive at this moment?
2. Clinical Profile -- What does admissions need to know about diagnosis?
3. Personality and Strengths -- What can a program build engagement around?
4. Needs and Challenges -- What must staff handle daily/weekly?
5. Academic Functioning -- What does the academic program need to provide?
6. Family System Impact -- What must the program offer the family?
7. Treatment History -- What's been tried, and why is higher care indicated?
8. Recommendations -- Environment features, BBI screening, placement goals
9. Executive Summary -- 3-4 sentence decision brief

### What is ThriveIEP (if asked)
- EdTech company building AI tools for clinical and educational professionals
- Products: Accommodation Engine (IEP report generation), Bloom Report (placement profiles), C2A (assessment for neurodivergent learners), PI Redactor (document redaction)
- Team: Eric (CPTO), Elizabeth (CEO), Soham (developer)
