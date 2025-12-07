# SDE2 Assessment

## Overview

We'd like you to build a working application that demonstrates your approach to real-world software engineering. You have **one week** to complete this assessment—we don't expect you to use all of it. We're evaluating how you design, build, and communicate—not how fast you can code.

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

## Deliverable Checklist

- [ ] Code compiles and runs without errors
- [ ] README explaining the project structure and how to run it
- [ ] Architecture diagram or written explanation of the code flow
- [ ] All endpoints documented (what they do, how to call them)
- [ ] Git history shows meaningful commits (not one big dump)
- [ ] At least basic unit tests included
