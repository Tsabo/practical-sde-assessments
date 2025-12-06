# SDE1/SDE2 Assessment - Interviewer Guide

## Interview Structure (60 minutes)

**Warm-up (5 min)** → **Code Walkthrough (20 min)** → **Deeper Questions (20 min)** → **Their Questions (10 min)** → **Wrap-up (5 min)**

---

## Part 1: Code Walkthrough (20 minutes)

Start with the candidate walking you through their solution. Listen more than you talk. You're evaluating:

### Key Areas to Explore

**1. Architecture & Separation of Concerns**
- *Ask:* "Walk me through how a request flows from the frontend through your API to the backend services."
- *What to listen for:*
  - Do they clearly explain the layers (controller → service → data access)?
  - Are there clear boundaries between frontend API and backend APIs?
  - Is the async/await pattern used correctly?
  - Can they explain *why* they structured it this way?
- *Red flags:*
  - Vague answers or inability to trace a request
  - Logic scattered across multiple layers with unclear boundaries
  - Misunderstanding of async/await (blocking calls, improper task handling)

**2. Code Quality & Maintainability**
- *Ask:* "Show me a piece of code you're proud of. Why?"
- *What to listen for:*
  - Naming clarity (do variable/function names make sense?)
  - DRY principle—are they repeating code unnecessarily?
  - Error handling—how do they deal with failures?
  - Comments—are they explaining *why*, not *what*?
- *Red flags:*
  - Generic names (data, result, temp)
  - No error handling or generic try/catch blocks
  - Over-commented obvious code, or no comments on complex logic

**3. Testing Approach**
- *Ask:* "What did you test? What would you test if you had more time? Why?"
- *What to listen for:*
  - Do they understand the difference between unit and integration tests?
  - Are they testing behavior or just coverage?
  - Did they test failure cases (service timeout, bad input)?
  - Do they have a testing strategy, or just "write tests"?
- *Red flags:*
  - Only testing the happy path
  - Tests that don't actually verify anything
  - Coverage ≠ understanding (high coverage, but shallow tests)
  - No tests at all

**4. Security Implementation**
- *Ask:* "Walk me through how JWT authentication works in your code. What could go wrong?"
- *What to listen for:*
  - Do they understand JWT basics (claims, expiration, token storage)?
  - Are tokens being validated on every protected endpoint?
  - Where is the secret stored? (Should NOT be in code)
  - Do they understand the difference between authentication and authorization?
- *Red flags:*
  - Storing secrets in code or version control
  - No token expiration
  - No validation on protected endpoints
  - Confusion about what JWT does/doesn't do

---

## Part 2: Deeper Technical Questions (20 minutes)

Use these to probe beyond what's in the code:

### Question Set A: Design Thinking

1. **"Why did you choose this technology/pattern over alternatives?"**
   - *Evaluating:* Do they understand trade-offs? Or just picked something familiar?
   - *Good answer:* "I used X because Y, though Z would have been better for [specific scenario]"
   - *Bad answer:* "That's just what I know" or "It was in the tutorial"

2. **"If one of your backend APIs becomes very slow, what happens to your frontend API?"**
   - *Evaluating:* Do they think about failure modes? Timeouts? User experience?
   - *Good answer:* Mentions timeouts, circuit breakers, or returning partial data
   - *Bad answer:* "It would just wait" or "I didn't think about that"

3. **"How would you handle adding a third backend API without breaking existing clients?"**
   - *Evaluating:* API versioning? Backwards compatibility? Deployment strategy?
   - *Good answer:* Clear plan for versioning or feature flags
   - *Bad answer:* "Just add the endpoint" or no clear strategy

### Question Set B: Real-World Concerns

4. **"How would a new developer on your team add a new endpoint?"**
   - *Evaluating:* Is code self-documenting? Are there patterns they can follow?
   - *Good answer:* Clear examples in codebase, patterns, documentation
   - *Bad answer:* "Just copy existing code" without explanation, or unclear patterns

5. **"What's the hardest part of this codebase to understand?"**
   - *Evaluating:* Self-awareness? Do they recognize areas that need better documentation?
   - *Good answer:* Specific area + plan to improve it
   - *Bad answer:* "Everything is easy" or can't identify any complexity

6. **"If this code broke in production tomorrow, how would you debug it?"**
   - *Evaluating:* Do they have logging? Monitoring? Can they troubleshoot?
   - *Good answer:* Mentions logs, correlation IDs, ability to trace requests
   - *Bad answer:* "Just add Console.WriteLine" or no debugging strategy

### Question Set C: Learning & Growth

7. **"What would you do differently if you started over?"**
   - *Evaluating:* Growth mindset? Reflection? Learning from the project?
   - *Good answer:* Specific improvements + reasoning
   - *Bad answer:* "Nothing, it's perfect" or vague regrets

8. **"What part of this assessment did you find challenging?"**
   - *Evaluating:* Humility? Can they articulate what they struggled with?
   - *Good answer:* Specific challenge + how they approached it
   - *Bad answer:* "Nothing was hard" or avoiding the question

---

## Part 3: Evaluation Rubric

Rate each category on a scale: **1 = Weak, 2 = Acceptable, 3 = Strong, 4 = Exceptional**

| Category | 1 (Weak) | 2 (Acceptable) | 3 (Strong) | 4 (Exceptional) |
|----------|----------|---|---|---|
| **Code Organization** | Scattered logic, hard to follow | Organized but some unclear boundaries | Clear layers, good separation | Well-structured, easy to extend |
| **Code Quality** | Poor naming, no error handling | Adequate naming, basic error handling | Good naming, thoughtful error handling | Clean code, handles edge cases |
| **Testing** | No tests or irrelevant tests | Basic tests, mostly happy path | Good coverage with some edge cases | Comprehensive testing strategy |
| **Technical Understanding** | Confused about key concepts | Understands basics, gaps remain | Solid grasp of concepts | Deep understanding, can explain trade-offs |
| **Problem-Solving** | Struggles with challenges | Completes requirements literally | Thinks about implications | Anticipates future needs |
| **Communication** | Hard to follow, vague | Clear but could be more articulate | Clear explanations | Excellent at explaining complex ideas |

---

## Red Flags to Watch For

| Red Flag | What It Means | Severity |
|----------|---------------|----------|
| **Can't explain their own code** | Didn't write it, copied it, or doesn't understand | 🔴 Critical |
| **No error handling** | Doesn't think about failure cases | 🔴 Critical |
| **Secrets in code/config** | Security risk | 🔴 Critical |
| **No tests or bad tests** | Won't catch regressions | 🟡 High |
| **Can't articulate why decisions** | Just copying patterns, not thinking | 🟡 High |
| **Async/await misuse** | Deadlocks, performance issues | 🟡 High |
| **Generic variable names** | Hard to maintain | 🟠 Medium |
| **No comments on complex logic** | Knowledge silos | 🟠 Medium |
| **Defensive/dismissive answers** | Won't take feedback | 🟠 Medium |

---

## Summary Notes

**Questions to Ask Yourself After the Interview:**

- Would I want this person reviewing my code?
- Could they mentor a junior developer?
- Would they ask for help when stuck, or silently deliver broken code?
- Do they care about quality or just "getting it working"?
- Can they communicate technical ideas clearly?

**Remember:** A good SDE1/SDE2 doesn't need to know everything, but they need to:
- ✅ Write code others can understand
- ✅ Think about failure cases
- ✅ Be willing to learn
- ✅ Take responsibility for quality
- ✅ Communicate clearly
