# SDE3 & Software Developer Engineer Lead Assessment - Interviewer Guide

## Interview Structure (90 minutes)

**Warm-up (5 min)** → **Architectural Walkthrough (25 min)** → **System Design Depth (25 min)** → **Leadership & Scalability (20 min)** → **Their Questions (10 min)** → **Wrap-up (5 min)**

---

## Part 1: Architectural Walkthrough (25 minutes)

Have the candidate walk you through the system. This is where you assess **systems thinking** and **design maturity**.

### Key Areas to Explore

**1. Architectural Vision & Design Decisions**
- *Ask:* "Walk me through your system architecture. What problem is each component solving?"
- *What to listen for:*
  - Do they articulate a clear vision, not just enumerate technologies?
  - Can they explain the rationale behind service boundaries?
  - Do they discuss trade-offs (consistency vs. availability, complexity vs. flexibility)?
  - Is the architecture documented? (ADRs, diagrams)
- *Red flags:*
  - Architecture seems arbitrary ("just standard microservices")
  - Can't explain why services are separated the way they are
  - Over-engineered for the problem size, or under-engineered

**2. Failure Mode Analysis**
- *Ask:* "Walk me through a request end-to-end. What are all the ways this can fail?"
- *What to listen for:*
  - Do they identify critical failure points?
  - Have they designed for resilience (circuit breakers, retries, timeouts)?
  - Do they understand cascading failures?
  - Is there graceful degradation?
  - How do they handle partial failures?
- *Red flags:*
  - "It won't fail" or dismissive attitude about failures
  - No circuit breakers, retries, or timeout strategies
  - No discussion of how services recover after failures
  - Single points of failure in the design

**3. Observability & Operations**
- *Ask:* "How would you know this system is having problems in production? Walk me through your monitoring strategy."
- *What to listen for:*
  - Structured logging with correlation IDs
  - Key metrics they're tracking (latency, error rates, throughput)
  - How they debug across service boundaries
  - Alert strategy—what wakes them up at 3 AM?
  - Cost awareness—are they thinking about operational burden?
- *Red flags:*
  - Logging is an afterthought ("we log errors")
  - No correlation IDs or tracing across services
  - No clear metrics or alerting strategy
  - "Just look at logs when something breaks"

**4. Data Consistency & Integrity**
- *Ask:* "If an order is placed but payment processing fails halfway through, what happens?"
- *What to listen for:*
  - Understanding of eventual consistency
  - Saga patterns or compensating transactions
  - How they handle idempotency
  - What data consistency guarantees they're making
- *Red flags:*
  - Assumes ACID across service boundaries (impossible)
  - No discussion of what happens if transactions fail mid-flow
  - Inconsistent data states are acceptable without recovery strategy

**5. Scalability & Performance**
- *Ask:* "Your system needs to handle 10x traffic. What breaks first? What do you optimize?"
- *What to listen for:*
  - Understand of bottlenecks (database, cache, network)
  - Caching strategy (what, where, invalidation)
  - Database optimization (indexing, query patterns)
  - Async patterns to handle load
  - Cost/performance trade-offs
- *Red flags:*
  - "Just add more servers" without understanding bottlenecks
  - No caching strategy
  - Database queries aren't optimized
  - No discussion of scaling limits or costs

---

## Part 2: System Design Depth (25 minutes)

Probe deeper into architectural maturity:

### Question Set A: Evolution & Versioning

1. **"Your API's requirements change significantly. How do you roll this out without breaking clients?"**
   - *Evaluating:* Do they think about backwards compatibility? Versioning strategy? Rolling deployments?
   - *Good answer:* Clear versioning approach (URL, header, or graceful deprecation), migration path for clients
   - *Bad answer:* "Break everything and tell clients to update" or no strategy

2. **"A new team wants to use your API. What's the friction they encounter?"**
   - *Evaluating:* Can they see their system from a user's perspective? Have they thought about API ergonomics?
   - *Good answer:* Clear documentation, sample code, SDKs, versioning clarity
   - *Bad answer:* "They read the docs" or dismissive

3. **"If you add a new feature that requires schema changes, how do you deploy without downtime?"**
   - *Evaluating:* Database migration strategy? Blue-green deployments? Backwards compatibility?
   - *Good answer:* Detailed plan for zero-downtime deployments
   - *Bad answer:* "Shut down the service, update, restart" or vague

### Question Set B: Risk & Security

4. **"What's the biggest security risk in your system? How do you mitigate it?"**
   - *Evaluating:* Do they do threat modeling? Understand their attack surface?
   - *Good answer:* Specific risk identified + concrete mitigations (rate limiting, encryption, validation)
   - *Bad answer:* "It's secure because JWT" or no clear threat model

5. **"How do you prevent a compromised service from taking down the whole system?"**
   - *Evaluating:* Defense in depth? Circuit breakers? Isolation? Rate limiting?
   - *Good answer:* Multiple layers of protection, service isolation, monitoring
   - *Bad answer:* "We trust our code" or no strategy

6. **"A team member accidentally commits a secret to the repo. What's your recovery process?"**
   - *Evaluating:* Do they have incident response? Prevention? Recovery strategies?
   - *Good answer:* Automatic secret scanning, rotation process, audit logs
   - *Bad answer:* "Just delete it" or no clear process

### Question Set C: Technical Leadership

7. **"How would you mentor a team building on top of this system?"**
   - *Evaluating:* Can they help others succeed? Do they document patterns?
   - *Good answer:* Clear examples, patterns, documentation, code review process
   - *Bad answer:* "They figure it out" or relying only on verbal knowledge

8. **"What technical debt did you intentionally incur? Why? How would you pay it down?"**
   - *Evaluating:* Can they distinguish necessary shortcuts from real problems?
   - *Good answer:* Specific, time-bound debts with clear payoff strategy
   - *Bad answer:* "No debt" (unrealistic) or ignoring debt completely

9. **"If you could rewrite this system, what would change?"**
   - *Evaluating:* Reflection and growth? Do they understand limitations of their design?
   - *Good answer:* Specific improvements based on lessons learned, with reasoning
   - *Bad answer:* "It's perfect" or vague regrets

---

## Part 3: Leadership & Scaling (20 minutes)

For SDEL candidates specifically, probe deeper here:

### Leadership Questions

10. **"Tell me about a time you had to influence a technical decision without authority."**
    - *Evaluating:* Influence without coercion? Can they persuade others?
    - *Good answer:* Specific example with data-driven reasoning
    - *Bad answer:* "I just convinced them" or no examples

11. **"How do you handle disagreement on technical approach with other strong engineers?"**
    - *Evaluating:* Do they listen? Can they find consensus? Are they stubborn or collaborative?
    - *Good answer:* Collaborative process, respect for other views, focus on outcomes
    - *Bad answer:* "I'm usually right" or dismissive of others

12. **"Describe a time you were wrong about something technical. What did you learn?"**
    - *Evaluating:* Humility? Growth mindset? Ability to admit mistakes?
    - *Good answer:* Clear example, what they learned, how they changed
    - *Bad answer:* "I'm rarely wrong" or vague lessons

13. **"How do you grow the technical capability of your team?"**
    - *Evaluating:* Do they develop others? Create learning opportunities?
    - *Good answer:* Specific practices (code review, pairing, talks, stretch projects)
    - *Bad answer:* "They learn on their own" or no strategy

---

## Part 4: Evaluation Rubric

Rate each category: **1 = Weak, 2 = Acceptable, 3 = Strong, 4 = Exceptional**

| Category | 1 (Weak) | 2 (Acceptable) | 3 (Strong) | 4 (Exceptional) |
|----------|----------|---|---|---|
| **Architectural Vision** | No clear vision, arbitrary tech choices | Basic sound architecture | Well-reasoned architecture with clear trade-offs | Visionary design anticipating future needs |
| **Systems Thinking** | Doesn't consider failure, bottlenecks | Basic awareness of system-wide concerns | Comprehensive failure analysis and mitigation | Elegant solutions to complex system problems |
| **Scalability** | No consideration of scale | Basic understanding, some bottlenecks | Clear scale strategy, identified bottlenecks | Optimized for 10x growth, cost-aware |
| **Observability** | Little to no logging/monitoring | Basic logging, limited debugging ability | Good structured logging, useful metrics | Production-grade observability, great UX |
| **Operations & Security** | No operational thinking | Basic security, ad-hoc operations | Security-first thinking, ops-aware design | Zero-trust, incident-response ready |
| **Data Integrity** | No consistency strategy | Works for happy path, inconsistency issues | Well-thought consistency model | Sophisticated handling of distributed transactions |
| **Documentation** | Minimal or unclear docs | Adequate documentation | Clear ADRs, diagrams, decision rationale | Exceptional documentation enabling team growth |
| **Technical Communication** | Hard to follow, loses audience | Clear but misses nuance | Excellent at explaining complex ideas | Master communicator of complex systems |
| **(SDEL) Leadership** | No evidence of influence | Limited mentoring/influence | Develops others, shapes decisions | Visionary leader, grows organizational capacity |

---

## Red Flags to Watch For

| Red Flag | What It Means | Severity |
|----------|---------------|----------|
| **No failure mode analysis** | Hasn't thought about production reality | 🔴 Critical |
| **Single points of failure in design** | System will definitely fail | 🔴 Critical |
| **No observability strategy** | Can't debug in production | 🔴 Critical |
| **Secrets in code** | Security violation | 🔴 Critical |
| **No resilience patterns** (circuit breakers, retries, timeouts) | Will fail under load | 🟡 High |
| **Can't articulate architectural trade-offs** | Didn't really think through design | 🟡 High |
| **Dismissive of operations/monitoring** | Won't support the system in prod | 🟡 High |
| **Over-engineered for scope** | Won't communicate why complexity exists | 🟠 Medium |
| **No data consistency strategy** | Potential for data corruption | 🟠 Medium |
| **Can't explain decisions in simple terms** | Poor communication skills | 🟠 Medium |
| **(SDEL) No evidence of mentoring others** | Won't help team grow | 🟠 Medium |
| **(SDEL) Dismissive of other engineers' ideas** | Won't collaborate effectively | 🟠 Medium |

---

## Special Notes for SDE3 vs. SDEL

### SDE3 Focus
- **Technical Depth:** Do they have mastery in their domain?
- **System Thinking:** Do they understand how everything connects?
- **Problem-Solving:** Can they tackle hard technical problems?
- **Independence:** Do they identify and solve problems without hand-holding?

### SDEL Focus
- **Leadership:** Can they influence and guide others?
- **Vision:** Do they set direction for teams/systems?
- **Development:** Do they grow others' capabilities?
- **Judgment:** Can they balance technical purity with business needs?

---

## Summary Notes

**Questions to Ask Yourself After the Interview:**

- Would I trust this person to make architectural decisions that affect the whole org?
- Could they lead a team of strong engineers?
- Do they balance speed with quality appropriately?
- Can they simplify complex problems?
- Would they ask for help when facing unknown challenges, or go in blind?
- Do they have a track record of growing others?
- Can they communicate with both engineers and business leaders?

**Remember:** A good SDE3/SDEL:
- ✅ Thinks in systems, not components
- ✅ Anticipates failure and designs for it
- ✅ Makes trade-offs consciously and can articulate them
- ✅ Raises the bar for everyone around them
- ✅ Simplifies without sacrificing correctness
- ✅ Listens and learns, even from junior engineers
- ✅ Ships code that survives production
