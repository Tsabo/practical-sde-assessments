# SDE1 Assessment

## Overview

We'd like you to build a working application that demonstrates your approach to real-world software engineering. You have **one week** to complete this assessment. We're evaluating how you design, build, and communicate—not how fast you can code.

### Time Expectation

Most candidates spend **8–15 hours** on this assessment. You don't need to polish every detail—we'd rather see solid fundamentals with rough edges than a gold-plated solution that took 40 hours. If you're spending significantly more time, step back and focus on the core requirements.

## Deliverables

Submit one of the following:
- **Priority 1:** GitHub repository with working code and clear documentation
- **Priority 2:** Zipped Visual Studio solution that compiles and runs

During the follow-up interview, we'll discuss your design decisions, code organization, and trade-offs you made.

## What We're Looking For

During the interview, we'll discuss:

1. **Architecture & Design Decisions** - How you structured the solution and why
2. **Code Quality** - Clarity, maintainability, proper use of patterns
3. **Testing Strategy** - What you tested and how you approached it
4. **Security Reasoning** - Your thoughts on JWT implementation and API security
5. **Communication** - How you explain your choices and trade-offs

## Technical Requirements

The solution should demonstrate competency across these areas:

- **Multi-API Integration:** Build a front-end API that calls 2 back-end APIs asynchronously (with artificial delays to simulate real workloads)
- **REST API Development:** Implement RESTful endpoints with GET/POST support; include Entity Framework and migrations
- **Frontend:** A web application with component architecture, routing, and data binding
- **Security:** JWT authentication protecting the APIs
- **Testing:** Unit tests for API endpoints and components
- **Code Organization:** Clean separation of concerns, reusable components, proper dependency injection and middleware configuration

### Frontend Framework

Choose the frontend framework you're most productive in:

- **Blazor** (Server or WebAssembly)
- **React** or **Angular**
- **Other modern SPA frameworks** (Vue, Svelte, etc.)

If you choose something other than Blazor, include clear run instructions and be ready to walk us through your component structure, state management, and how the UI interacts with your APIs during the interview.

We care more about clean architecture and your ability to explain your choices than which specific framework you use.

## What "Good" Looks Like

### Minimum Viable Submission (Passing)
A passing submission demonstrates fundamental competency:
- Code compiles and runs without errors
- Multi-API integration works (frontend API calls backend APIs)
- JWT authentication is implemented and protects endpoints
- Basic unit tests exist for key functionality
- README explains how to run the project
- Code is reasonably organized (not all in one file)

### Strong Submission
A strong submission shows deeper engineering maturity:
- Clear separation of concerns with well-defined layers
- Thoughtful error handling (not just try/catch everywhere)
- Tests cover both happy paths and failure cases
- Good naming and code organization—easy to navigate
- README includes architecture explanation or diagram
- Git history shows iterative development

### Exceptional Submission
An exceptional submission demonstrates senior-level thinking:
- Architecture decisions are documented with rationale
- Edge cases and failure modes are considered
- Security implementation shows understanding beyond "JWT exists"
- Testing strategy is intentional, not just coverage-driven
- Code is something you'd be proud to maintain long-term

## Deliverable Checklist

- [ ] Code compiles and runs without errors
- [ ] README explaining the project structure and how to run it
- [ ] Architecture diagram or written explanation of the code flow
- [ ] All endpoints documented (what they do, how to call them)
- [ ] Git history shows meaningful commits (not one big dump)
- [ ] At least basic unit tests included

## Questions?

If anything is unclear, ask. We'd rather clarify expectations upfront than have you guess wrong and waste time.
