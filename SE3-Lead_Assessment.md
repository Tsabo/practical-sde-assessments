# SDE3 & Software Developer Engineer Lead Assessment

## Overview

This assessment is designed to evaluate candidates for Software Developer Engineer 3 (SDE3) and Software Developer Engineer Lead (SDEL) positions. We're looking for evidence of **systems thinking**, **architectural decision-making**, **team impact**, and **forward-thinking design**. You have **one week** to complete this assessment.

This is not just about building working code—it's about demonstrating how you design systems that scale, survive failures, and enable teams to grow.

## Deliverables

Submit one of the following:
- **Priority 1:** GitHub repository with working code, architectural documentation, and design decisions recorded
- **Priority 2:** Zipped Visual Studio solution with comprehensive README and architecture documentation

During the follow-up interview, we'll discuss your architectural choices, trade-offs, scalability thinking, and how you'd lead a team building on this system.

## What We're Looking For

During the interview, we'll discuss:

1. **Architectural Vision** - How you designed for growth, failure modes, and team extensibility
2. **Trade-off Analysis** - Why you chose certain patterns over alternatives; what you optimized for
3. **Scalability & Operations** - How your design handles growth; monitoring, logging, and debugging
4. **Team Enablement** - How your code structure and documentation help others contribute
5. **Risk & Security** - Deep thinking on security threats, data flow, and operational risks
6. **Communication & Leadership** - How you explain complexity; evidence of mentorship or thought leadership in code

## Technical Requirements

Build a system that demonstrates mature engineering practices:

- **Multi-Service Architecture:** A front-end API orchestrating 2+ back-end services asynchronously. Design for resilience—what happens when one service is slow or fails?
- **REST API Development:** RESTful endpoints with proper versioning strategy; Entity Framework with thoughtful migration patterns
- **Frontend:** Blazor application with component architecture that enables team contribution; clear patterns for routing and state management
- **Frontend choice:** Blazor is preferred for consistent evaluation; if you select another framework (React/Angular/etc.), provide run instructions, document how routes/components map to API interactions, and be ready to explain your state management, data loading, and error-handling patterns during the interview
- **Security:** JWT authentication with thoughtful consideration of token lifecycle, refresh strategies, and API threat model
- **Observability:** Structured logging, correlation IDs across service calls, and clear operational insights
- **Testing Strategy:** Unit tests, integration tests, and documented testing approach (not just coverage %)
- **Code Organization:** Clean separation that enables team scaling; documented patterns; reusable, well-named abstractions

## Architectural Expectations

Beyond the basic requirements, show your thinking on:

- **Resilience Patterns:** Circuit breakers, retries, timeouts, graceful degradation. How does your system behave under failure?
- **API Design Evolution:** How would versioning and backwards compatibility work as requirements change?
- **Data Consistency:** How do you handle eventual consistency between services? What are the guarantees?
- **Operational Concerns:** How would someone deploy, monitor, and debug this in production? What metrics matter?
- **Team Scalability:** If a junior engineer or new team member needs to add a feature, what friction do they encounter?

## Deliverable Checklist

- [ ] Code compiles and runs without errors
- [ ] **Architecture Decision Records (ADRs)** or README section explaining key design choices and why
- [ ] Architecture diagram showing service interactions, failure points, and data flow
- [ ] All endpoints documented with examples (including error cases)
- [ ] Git history with meaningful commits showing iterative thinking (not a dump)
- [ ] Comprehensive test coverage with documented testing strategy
- [ ] Operational documentation: how to deploy, configure, debug, and monitor
- [ ] Evidence of team-first thinking: clear patterns, reusable components, good naming

## Optional Stretch Goals (Not Required)

These demonstrate SE3/Lead-level thinking:

- **Deployment & Infrastructure:** Docker/K8s setup showing production readiness
- **Advanced Resilience:** Chaos engineering example (e.g., what breaks when a service is down?)
- **Performance Analysis:** Documented performance characteristics and where optimization matters
- **Cost/Efficiency:** Thoughtful discussion of trade-offs between features, performance, and operational cost
- **Mentorship Evidence:** Clear code comments explaining *why* decisions were made, not just *what* the code does

## Interview Focus

We'll spend time on questions like:

- "Walk us through a request from the frontend. What are the failure points?"
- "How would you handle a 10x increase in traffic?"
- "If a new team member joined, what would be hardest to understand about this system?"
- "What would you do differently if you could start over?"
- "How do you know this system is healthy in production?"
