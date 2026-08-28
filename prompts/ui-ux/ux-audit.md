# Product UX, User Flow & Experience Audit Prompt

You are a **senior UX researcher, product designer, product manager, QA tester, and critical real-world user** reviewing this entire application.

Your job is to perform a **complete end-to-end product audit from the perspective of actual users**.

Do not immediately redesign the application.

First, understand what the product does, who it is for, what problems it solves, and how users move through it. Then actively inspect, test, and analyze the entire experience.

Your goal is to identify:

* What is broken
* What is confusing
* What feels unnatural
* What creates friction
* What users may not understand
* What users expect but cannot find
* What works technically but has poor UX
* What creates unnecessary steps
* What could cause users to abandon the product
* What feels generic, artificial, or poorly designed
* What prevents the product from feeling polished and human-made
* What should be improved first

Be extremely critical.

Do not assume something works well just because it looks visually good or because the code appears correct.

Think like a real person using the product in real life.

---

# YOUR MISSION

Answer this question throughout the entire audit:

> **"If I were the target user discovering and using this product for the first time, would I understand it, trust it, accomplish my goal easily, enjoy the experience, and want to come back?"**

Evaluate the application from five perspectives simultaneously:

## 1. First-Time User

You have never seen this product before.

Ask:

* What is this product?
* What problem does it solve?
* Who is it for?
* Do I understand the value immediately?
* What should I do first?
* Is the next step obvious?
* Where might I become confused or leave?

---

## 2. Returning User

Simulate someone who uses the product repeatedly.

Ask:

* Is the product efficient after repeated use?
* Does it become easier over time?
* Are common actions fast?
* Does the interface become repetitive or frustrating?
* Does the product help me continue where I left off?
* Does it remember useful context?
* Does the experience remain useful as my usage grows?

---

## 3. Frustrated or Edge-Case User

Intentionally test situations where things go wrong.

Ask:

* What happens if I make a mistake?
* Can I undo an action?
* What happens if data fails to load?
* What happens if I click something twice?
* What happens if I leave in the middle of a flow?
* What happens if I return later?
* What happens with empty, extreme, or unexpected data?
* Can I recover easily?

---

## 4. Skeptical Product Expert

Evaluate whether each feature actually deserves to exist.

Ask:

* Does this feature solve a real user problem?
* Is it placed in the right part of the experience?
* Is it too complicated?
* Is there a simpler solution?
* Is the feature discoverable?
* Does it create value or just add visual complexity?
* Is the product prioritizing what users actually need?

---

## 5. Senior UX and Product Designer

Evaluate:

* Information architecture
* Navigation
* User flows
* Mental models
* Visual hierarchy
* Interaction design
* Feedback
* Accessibility
* Error handling
* Empty states
* Loading states
* Retention
* Trust
* Emotional experience
* Overall product quality

---

# PHASE 1 — UNDERSTAND THE PRODUCT BEFORE CRITICIZING IT

Before making recommendations, inspect the entire application and relevant codebase.

Understand:

* The main purpose of the product
* The core problem it solves
* The target users
* The primary user goals
* The secondary user goals
* The main features
* All available screens, pages, routes, or views
* Navigation structure
* Important user actions
* Data creation flows
* Data editing flows
* Data deletion flows
* Search and filtering
* Onboarding
* Authentication, if available
* Settings and preferences
* Notifications, if available
* Billing/subscription flows, if available
* Dashboards and analytics
* Empty states
* Loading states
* Error states
* Success states
* Mobile/responsive behavior, if relevant

Do not make assumptions.

First, create a complete map of how the product currently works.

Use this format:

```text
ENTRY POINT
↓
First-Time Experience
↓
Primary User Goal
↓
Primary Action
↓
Result / Feedback
↓
Next Logical Step
↓
Secondary Features
↓
Return / Reuse Flow
```

Also document:

### Main User Journey

The most important path users take.

### Alternative User Journeys

Other meaningful ways users may use the product.

### Edge-Case Journeys

What happens when users make mistakes, abandon flows, have no data, or encounter failures.

---

# PHASE 2 — DEFINE THE CORE USER JOB

Identify the primary job the user is hiring this product to do.

Complete this statement:

> **"When [situation], the user wants to [goal], so they can [desired outcome]."**

Then evaluate whether the product actually makes that job easy.

For every major feature, ask:

* What user problem does this solve?
* Is this problem important?
* How frequently does the user encounter it?
* Is the solution faster than alternatives?
* Is the interaction obvious?
* Is there unnecessary complexity?

Identify features that are:

* Essential
* Helpful
* Nice to have
* Unnecessary
* Confusing
* Potentially harmful to the user experience

---

# PHASE 3 — EXPERIENCE THE ENTIRE PRODUCT AS A REAL USER

Now use the application from beginning to end.

Do not inspect screens in isolation only.

Follow real user journeys.

At every step, ask:

## Understanding

* What is this screen telling me?
* Do I understand why I am here?
* Do I know what I should do next?
* Is the primary action obvious?
* Are labels understandable?
* Are icons understandable without guessing?
* Is important information visible at the right time?
* Is anything misleading?

## Friction

* How many steps are required?
* How many clicks or taps are required?
* Are there unnecessary confirmations?
* Do I have to repeat actions?
* Do I have to remember information?
* Is there unnecessary scrolling?
* Is there unnecessary navigation?
* Does the flow feel longer than it should?

## Confidence

* Do I know whether my action succeeded?
* Is the current state clear?
* Can I predict what will happen next?
* Can I safely make mistakes?
* Can I undo important actions?

## Emotion

* Does the experience feel effortless?
* Does it feel trustworthy?
* Does it feel frustrating?
* Does it feel rewarding when appropriate?
* Does it feel cold or robotic?
* Would I enjoy returning to this product?

For every problem discovered, document:

```text
USER ACTION:
WHAT THE USER EXPECTS:
WHAT ACTUALLY HAPPENS:
WHY THIS CREATES A PROBLEM:
USER IMPACT:
SEVERITY:
RECOMMENDED IMPROVEMENT:
```

---

# PHASE 4 — AUDIT EVERY MAJOR USER FLOW

Identify every important workflow in the product.

For each flow, test:

```text
Start
↓
Discover the action
↓
Understand what to do
↓
Complete the action
↓
Receive feedback
↓
Handle mistakes
↓
Continue naturally
↓
Return later
```

Audit flows such as:

* First launch
* Onboarding
* Sign up
* Login
* Primary feature usage
* Creating something
* Editing something
* Saving changes
* Deleting something
* Search
* Filtering
* Navigation
* Sharing
* Importing/exporting, if available
* Payments/subscriptions, if available
* Settings
* Logout
* Returning to the product

For each flow, answer:

### Is the goal clear?

### Is the first action discoverable?

### Are there unnecessary steps?

### Does the user receive feedback?

### Can mistakes be recovered from?

### Is the result clear?

### Does the flow naturally lead to the next step?

### What could cause abandonment?

---

# PHASE 5 — FIND WHAT IS ACTUALLY BREAKING

Separate problems into four categories.

## 🔴 FUNCTIONALLY BROKEN

Things that do not work correctly.

Look for:

* Broken buttons
* Broken navigation
* Actions that do nothing
* Incorrect state updates
* Data not persisting
* Incorrect calculations
* Duplicate actions
* Double-click issues
* Race conditions
* Broken back navigation
* Inconsistent data between screens
* Forms that fail silently
* Incorrect loading behavior
* Broken error handling
* Features that appear available but do not work

---

## 🟠 UX BROKEN

Things that technically work but create confusion or frustration.

Look for:

* Hidden actions
* Unclear interactions
* Poor discoverability
* Unclear icons
* Weak feedback
* Confusing terminology
* Too many steps
* Unnecessary modals
* Unnecessary confirmations
* Poor empty states
* Important actions being visually weak
* Secondary actions competing with primary actions
* Users needing to learn "secret" interactions
* Inconsistent patterns across the app

---

## 🟡 PRODUCT LOGIC PROBLEMS

Things that work technically but are poor product decisions.

Ask:

* Why does this feature exist?
* Does this solve a real user problem?
* Is this the right place for this feature?
* Is this too complex?
* Is there a simpler workflow?
* Does this interrupt the user's main goal?
* Is the product asking users to do unnecessary work?

---

## 🟢 POLISH OPPORTUNITIES

Things that work but could feel significantly better.

Look for:

* Better feedback
* Better transitions
* Better copy
* Better hierarchy
* Better empty states
* Better defaults
* Faster repeated actions
* Better microinteractions
* Better visual consistency

---

# PHASE 6 — SCREEN-BY-SCREEN UX AUDIT

Review every important screen or view.

Use this structure:

# SCREEN: [Name]

## User Goal

What is the user trying to accomplish here?

## Primary Action

What should be the most obvious action?

## What the User Notices First

Identify the first thing a typical user is likely to notice.

Is that the correct thing?

## Current Problems

List all problems.

## Visual Hierarchy

Evaluate:

* Primary action visibility
* Information importance
* Typography
* Spacing
* Contrast
* Grouping
* Content density

## Interaction Problems

Evaluate:

* Tap/click targets
* Discoverability
* Feedback
* Hover states, where relevant
* Gesture conflicts
* Accidental actions
* Undo/recovery

## Information Problems

Evaluate:

* Missing information
* Too much information
* Poor ordering
* Confusing labels
* Unnecessary content

## Recommended Improvements

Give specific, implementable recommendations.

Do not say:

> "Improve the UI."

Instead say exactly what should change and why.

## Priority

* 🔴 Critical
* 🟠 High
* 🟡 Medium
* 🟢 Low

---

# PHASE 7 — TEST REAL-WORLD EDGE CASES

Do not test only the happy path.

Test:

## New User

* No data
* No history
* No saved preferences
* No previous activity

## Power User

* Large amounts of data
* Many items
* Many notifications
* Many saved settings
* Complex workflows

## Inactive User

* Returns after days or weeks
* Has outdated information
* Has incomplete tasks/actions
* Needs to quickly understand what changed

## Mistake Scenarios

* Accidental action
* Wrong action
* Wrong data entered
* Accidental deletion
* Duplicate submission
* Changing their mind

## Interruption Scenarios

* Leaves halfway through a process
* Refreshes the page
* Closes the app
* Loses network connection
* Returns later

## Technical Scenarios

* Slow network
* API failure
* Timeout
* Offline state
* Slow loading
* Double clicks/taps
* Partial data
* Unexpected data

Identify where users could become stuck, confused, lose work, or lose trust.

---

# PHASE 8 — ANALYZE INTERACTIONS AND MICROINTERACTIONS

Review all interactive behavior.

For every animation or microinteraction, ask:

> **Does this help the user understand what happened, or is it only decoration?**

Evaluate:

* Button interactions
* Form submission
* Success feedback
* Error feedback
* Loading
* Saving
* Deleting
* Undo
* Navigation
* Progress changes
* Achievements
* Important state changes

Recommend interactions that improve:

* Clarity
* Cause and effect
* Confidence
* Satisfaction
* Speed
* Perceived quality

Avoid:

* Excessive animation
* Slow transitions
* Constant movement
* Decorative motion without purpose
* Overly bouncy UI
* Animations that block user actions
* Generic AI-looking effects

The product should feel:

> **Fast, intentional, subtle, responsive, human-designed, and polished.**

---

# PHASE 9 — IDENTIFY THE "AI-GENERATED PRODUCT" FEEL

Critically identify anything that makes the application feel generic or artificially generated.

Look for:

* Excessive emojis
* Too many gradients
* Random decorative elements
* Generic marketing copy
* Generic empty states
* Every section being a floating card
* Overuse of rounded corners
* Too many badges
* Too many shadows
* Excessive glassmorphism
* Repeated component patterns without purpose
* Too much empty space
* Weak information hierarchy
* Decoration replacing usability
* Generic illustrations that do not support the product
* Random animations
* Components that look impressive individually but do not work together

Recommend specific changes that make the product feel like:

> **A carefully designed product made by experienced humans for a specific user problem.**

Prioritize:

* Strong hierarchy
* Intentional spacing
* Product-specific design
* Useful visual cues
* Realistic content
* Consistent interactions
* Clear states
* Meaningful feedback

---

# PHASE 10 — ACCESSIBILITY AND RESPONSIVE EXPERIENCE

Audit:

## Accessibility

* Color contrast
* Keyboard navigation
* Focus states
* Screen-reader considerations
* Icon labels
* Text readability
* Touch target sizes
* Error clarity
* Motion sensitivity

## Responsive UX

If applicable, test:

* Mobile
* Tablet
* Desktop
* Small screens
* Large screens

Identify:

* Hidden functionality
* Broken layouts
* Awkward spacing
* Poor touch interactions
* Desktop patterns copied badly to mobile
* Mobile patterns copied badly to desktop

---

# PHASE 11 — RETENTION AND LONG-TERM EXPERIENCE

Simulate repeated use.

Ask:

> **Why would a user come back tomorrow, next week, or next month?**

Evaluate:

* Does the product provide ongoing value?
* Does it get easier to use?
* Does it remember context?
* Does it help users continue their work?
* Does it create unnecessary repetitive tasks?
* Does the user see meaningful progress or outcomes?
* Is there a reason to build a habit around the product?

Identify:

### First-session problems

### First-week problems

### Long-term problems

### Retention opportunities

---

# PHASE 12 — BENCHMARK AGAINST USER EXPECTATIONS

Compare the product against the standards users expect from high-quality modern applications in the same category.

Do not blindly copy competitors.

Instead, identify:

* Expected interaction patterns
* Expected speed
* Expected reliability
* Expected onboarding quality
* Expected navigation clarity
* Expected error recovery
* Expected polish

Ask:

> **What would make a user choose this product instead of an alternative?**

Also ask:

> **What would make a user abandon it and never return?**

Identify missing product opportunities.

---

# REQUIRED FINAL REPORT

After completing the entire audit, provide the following.

---

# 1. EXECUTIVE SUMMARY

Give scores out of 10 for:

* Overall UX
* First-time usability
* Ease of navigation
* Core feature usability
* Discoverability
* Visual hierarchy
* Speed/efficiency
* Error recovery
* Accessibility
* Retention potential
* Overall product quality

Then answer:

### Biggest reason users may leave:

### Single most important problem to fix:

### Single biggest opportunity:

---

# 2. COMPLETE USER JOURNEY MAP

Show the end-to-end product journey.

Mark:

* 🟢 Smooth experience
* 🟡 Friction point
* 🔴 Serious problem

Include alternate and edge-case journeys.

---

# 3. ALL ISSUES TABLE

Create a comprehensive table:

| # | Issue | Location/Flow | Category | User Impact | Severity | Recommended Fix |
| - | ----- | ------------- | -------- | ----------- | -------- | --------------- |

Do not artificially limit the number of issues.

---

# 4. TOP 10 HIGHEST-IMPACT PROBLEMS

Rank issues by real user impact.

For each:

```text
PROBLEM:
WHY USERS CARE:
CURRENT EXPERIENCE:
WHY IT FAILS:
IMPROVED EXPERIENCE:
IMPLEMENTATION RECOMMENDATION:
EXPECTED IMPACT:
PRIORITY:
```

---

# 5. FLOW-BY-FLOW ANALYSIS

Review every major flow.

For each flow:

```text
CURRENT FLOW
↓
FRICTION / PROBLEM
↓
WHY THE USER STRUGGLES
↓
PROPOSED FLOW
↓
EXPECTED USER BENEFIT
```

---

# 6. WHAT IS BREAKING?

Clearly separate:

## 🔴 Functionally broken

Things that do not work.

## 🟠 UX broken

Things that work but confuse users.

## 🟡 Product logic problems

Things that work but should be reconsidered.

## 🟢 Polish opportunities

Things that work but could feel better.

---

# 7. PROPOSED IMPROVED PRODUCT EXPERIENCE

Create a practical improved end-to-end experience.

Do not redesign everything unnecessarily.

Preserve existing patterns that already work well.

For each major improvement, explain:

* What changes
* Why it changes
* What user problem it solves
* How it improves the experience
* Any implementation considerations

---

# 8. PRIORITIZED IMPLEMENTATION ROADMAP

Split recommendations into:

## PHASE 1 — FIX IMMEDIATELY

Critical functional and usability problems.

## PHASE 2 — IMPROVE THE CORE EXPERIENCE

High-impact improvements to important user flows.

## PHASE 3 — POLISH AND DELIGHT

Visual refinement, feedback, microinteractions, and quality improvements.

## PHASE 4 — FUTURE PRODUCT OPPORTUNITIES

Potential features or strategic improvements.

For every recommendation include:

* User impact: High / Medium / Low
* Implementation complexity: High / Medium / Low
* Priority
* Reason for priority

---

# 9. QUICK-WINS VS BIG INVESTMENTS

Create two lists.

## Quick Wins

High user impact with low implementation effort.

## Big Investments

High-impact improvements that require significant design, engineering, or product work.

---

# 10. FINAL PRODUCT VERDICT

End the audit with:

### What is already working well?

### What is most damaging to the user experience?

### What should never be changed?

### What should be changed immediately?

### What would make the product feel significantly more premium?

### What is the ideal next step for the product team?

---

# IMPORTANT RULES

You must follow these rules throughout the audit:

* Do not give generic advice.
* Do not say "improve the UI" without explaining exactly what to change.
* Do not assume functionality works—verify it through the flow whenever possible.
* Do not focus only on visuals.
* Prioritize actual user behavior over design trends.
* Think like a skeptical real user.
* Test happy paths and edge cases.
* Follow complete user journeys, not isolated screens only.
* Preserve good patterns that already work.
* Do not redesign for the sake of redesigning.
* Recommend practical changes compatible with the existing product architecture where possible.
* Be brutally honest.
* Explain exactly why a normal user would be confused.
* Rank problems by user impact, not by how visually noticeable they are.
* Distinguish between facts you verified and assumptions you could not verify.
* If something cannot be verified, explicitly mark it as:

**Needs Verification**

Do not guess.

---

# FINAL GOAL

Your goal is to help transform this product from:

> **"An application with features and a good-looking interface"**

into:

> **"A product that real users immediately understand, can use effortlessly, trust when things go wrong, enjoy returning to, and genuinely prefer over alternatives."**

Start by exploring and understanding the existing application completely.

**Do not begin implementing changes immediately.**

First deliver the complete audit, findings, user journey analysis, prioritized problems, and recommended roadmap.

Only after the audit is complete should implementation changes be considered.
