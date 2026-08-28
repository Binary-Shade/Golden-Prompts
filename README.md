## Golden Prompts

> A curated collection of powerful, practical, and reusable AI prompts for developers, vibe coders, builders, designers, researchers, and creators.

**Golden Prompts** is an open prompt library designed to help you get better results from AI tools like ChatGPT, Claude, Gemini, Cursor, Codex, and other AI assistants.

Instead of repeatedly writing prompts from scratch, find a useful prompt, copy it, adapt it to your project, and start building.

---

## What's Inside?

This repository contains prompts for:

*  **Development** — code reviews, debugging, refactoring, system design, Next.js, and more
*  **Security** — application security audits, vulnerability reviews, OWASP checks
*  **UI / UX** — redesigns, dashboards, landing pages, UX audits, mobile experiences
*  **Business** — product strategy, competitor analysis, SaaS pricing, customer feedback
*  **Marketing** — SEO, landing page copy, social media, app descriptions
*  **Writing** — professional emails, rewriting, summarization
*  **Research** — deep research, product research, technology comparisons
*  **Automation** — AI agents, workflows, and data analysis

---

## 📁 Repository Structure

```text
Golden-Prompts/
│
├── README.md
├── CONTRIBUTING.md
├── LICENSE
│
├── prompts/
│   │
│   ├── development/
│   │   ├── code-review.md
│   │   ├── security-audit.md
│   │   ├── bug-fixing.md
│   │   ├── system-design.md
│   │   ├── nextjs.md
│   │   └── refactoring.md
│   │
│   ├── ui-ux/
│   │   ├── ui-redesign.md
│   │   ├── landing-page.md
│   │   ├── dashboard.md
│   │   ├── mobile-app.md
│   │   └── ux-audit.md
│   │
│   ├── business/
│   │   ├── product-strategy.md
│   │   ├── competitor-analysis.md
│   │   ├── customer-feedback.md
│   │   └── saas-pricing.md
│   │
│   ├── marketing/
│   │   ├── seo.md
│   │   ├── landing-page-copy.md
│   │   ├── social-media.md
│   │   └── app-description.md
│   │
│   ├── writing/
│   │   ├── professional-email.md
│   │   ├── rewrite.md
│   │   └── summarization.md
│   │
│   ├── research/
│   │   ├── deep-research.md
│   │   ├── technology-comparison.md
│   │   └── product-research.md
│   │
│   └── automation/
│       ├── agent-prompt.md
│       ├── workflow-design.md
│       └── data-analysis.md
│
├── templates/
│   ├── universal-prompt-template.md
│   ├── code-prompt-template.md
│   └── research-template.md
|______
```

---

# How to Use

Using a prompt is simple:

### 1. Browse a category

Navigate to the `prompts/` directory and find a prompt relevant to your task.

For example:

```text
prompts/development/security-audit.md
```

### 2. Copy the prompt

Copy the complete prompt into your preferred AI assistant.

### 3. Add your context

Replace placeholders or add details about your project.

For example:

```text
Project: [YOUR PROJECT NAME]
Tech Stack: [YOUR TECH STACK]
Goal: [WHAT YOU WANT TO ACHIEVE]
```

### 4. Iterate

The best results usually come from giving the AI relevant context about your project, requirements, constraints, and expected output.

---

#  Prompt Categories

##  Development

Prompts designed to help developers build, debug, review, and improve software.

| Prompt         | Description                                 |
| -------------- | ------------------------------------------- |
| Code Review    | Perform a detailed review of a codebase     |
| Security Audit | Identify vulnerabilities and security risks |
| Bug Fixing     | Investigate and fix issues methodically     |
| System Design  | Design scalable application architectures   |
| Next.js        | Build and improve Next.js applications      |
| Refactoring    | Improve code quality and maintainability    |

---

##  UI / UX

Prompts for building interfaces that feel polished, intentional, and human-designed.

| Prompt       | Description                                |
| ------------ | ------------------------------------------ |
| UI Redesign  | Completely improve an existing interface   |
| Landing Page | Create or improve landing page experiences |
| Dashboard    | Design better SaaS dashboards              |
| Mobile App   | Improve mobile application experiences     |
| UX Audit     | Identify usability and experience problems |

---

##  Business

Prompts for product builders, founders, and SaaS teams.

* Product strategy
* Competitor analysis
* Customer feedback analysis
* SaaS pricing
* Product decision-making

---

##  Marketing

Prompts for growing and positioning products.

* SEO optimization
* Landing page copy
* Social media content
* App and product descriptions

---

##  Writing

Prompts for clearer and better communication.

* Professional emails
* Rewriting and polishing
* Summarization
* Content improvement

---

##  Research

Prompts for structured research and decision-making.

* Deep research
* Technology comparisons
* Product research

---

##  Automation

Prompts for designing AI-powered workflows.

* AI agents
* Workflow design
* Data analysis

---

#  Prompt Format

Each prompt should ideally follow a consistent structure:

````md
---
title: Prompt Name
category: development
tags:
  - example
  - reusable
status: tested
---

# Prompt Name

## Purpose

Explain what this prompt is designed to accomplish.

## Best For

- Use case one
- Use case two
- Use case three

## Prompt

```text
Your complete prompt goes here...
````

## Notes

Additional information, limitations, or tips for getting better results.

## Tags

`tag-one` `tag-two` `tag-three`

````

---

# Prompt Quality

Prompts may be labelled with a status:

-  **Tested** — Used and validated with good results
-  **Needs Testing** — Added but requires more validation
-  **Deprecated** — No longer recommended

The goal is not to collect thousands of random prompts.

The goal is to build a collection of **useful prompts that actually produce good results**.

---

# Contributing

Contributions are welcome!

If you have a useful prompt that has helped you:

1. Fork this repository
2. Create a new branch
3. Add your prompt to the appropriate category
4. Follow the prompt template
5. Submit a Pull Request

Before submitting a prompt:

- Make sure it has a clear purpose
- Give it a descriptive filename
- Avoid unnecessary filler
- Include useful context or instructions
- Test it when possible
- Remove any private API keys, credentials, or sensitive information

See [CONTRIBUTING.md](./CONTRIBUTING.md) for contribution guidelines.

---

# Naming Guidelines

Use clear and descriptive filenames:

```text
full-security-audit.md
nextjs-ui-ux-redesign.md
debug-production-issue.md
deep-codebase-analysis.md
saas-landing-page.md
customer-feedback-analysis.md
````

Avoid filenames like:

```text
prompt1.md
new-prompt.md
final-v2.md
good-prompt.md
```

---

# Philosophy

A good prompt should be:

* **Clear** — The AI should understand the goal
* **Specific** — Important requirements should be explicit
* **Reusable** — Easy to adapt to other projects
* **Practical** — Focused on real-world outcomes
* **Structured** — Clear input, instructions, and expected output
* **Tested** — Improved based on actual usage

> **Good prompts don't just ask AI to do something. They provide enough context, constraints, and direction to help AI do it well.**

---

# Roadmap

Future improvements may include:

* [ ] More tested prompts
* [ ] Prompt quality ratings
* [ ] Better tagging and search
* [ ] Model-specific prompt variants
* [ ] Example inputs and outputs
* [ ] A searchable web interface
* [ ] Community contributions
* [ ] Prompt versioning
* [ ] AI agent workflow prompts

---

# Support the Project

If you find this repository useful:

* ⭐ Star the repository
* 🍴 Fork it
* 🐛 Report issues
* 💡 Suggest new prompt ideas
* 🤝 Contribute your best prompts

Your support helps grow **Golden Prompts** into a useful open collection for builders and developers.

---

## License

This project is licensed under the terms of the license included in the [LICENSE](./LICENSE) file.

---

<div align="center">

### Golden Prompts

**A growing collection of useful AI prompts for people who build.**

Made for developers, vibe coders, founders, designers, and creators.

[Explore the Prompts](./prompts) · [Contribute](./CONTRIBUTING.md) · [Report an Issue](https://github.com/Binary-Shade/Golden-Prompts/issues)

</div>
