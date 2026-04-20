# Contributing to Product Development Playbook

First off — thank you for taking the time to contribute. 🙌

This guide exists to help developers and product builders do their best work. Every improvement, no matter how small, makes it more useful for everyone.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [What Can I Contribute?](#what-can-i-contribute)
- [What Should I NOT Change?](#what-should-i-not-change)
- [How to Contribute](#how-to-contribute)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Issue Guidelines](#issue-guidelines)
- [Content Standards](#content-standards)
- [Commit Message Format](#commit-message-format)

---

## Code of Conduct

By participating in this project, you agree to follow the [Code of Conduct](./CODE_OF_CONDUCT.md).

The short version: be respectful, be constructive, assume good intent.

---

## What Can I Contribute?

All of the following are welcome:

| Type | Examples |
|------|---------|
| 📚 **Add a reference** | A relevant book, research paper, or documentation link that is missing from a phase |
| 🔗 **Update a link** | Fix a broken or outdated URL |
| ✏️ **Improve clarity** | Reword a confusing checklist item or explanation |
| 🐛 **Fix inaccurate content** | Correct information that is outdated or factually wrong |
| ➕ **Add a TODO item** | Suggest a missing best-practice step to an existing phase |
| 💡 **Add a tip** | Contribute a practical tip that is relevant and actionable |
| 🌐 **Improve formatting** | Fix typos, broken Markdown, table alignment, heading structure |
| 📖 **Add a new section** | Propose a new phase or sub-section (open an issue first for discussion) |

---

## What Should I NOT Change?

To keep this guide focused and high-quality, please **avoid**:

- ❌ Adding references that are not publicly verifiable (personal blogs without citations, YouTube videos, etc.)
- ❌ Adding tool-specific or stack-specific content that is not general — this guide is intentionally technology-agnostic
- ❌ Replacing existing valid references with alternatives simply based on personal preference
- ❌ Adding promotional content, affiliate links, or links to paid products without a free equivalent
- ❌ Making large structural changes without opening an issue for discussion first

---

## How to Contribute

### Option 1 — Fix something small (typo, broken link, minor wording)

1. Fork the repository
2. Make your change directly in the relevant file
3. Submit a Pull Request with a clear title and description

### Option 2 — Add or change content

1. **Open an Issue first** — describe what you want to add or change and why
2. Wait for a response or approval before writing
3. Fork the repository
4. Create a new branch:
   ```bash
   git checkout -b add/security-reference-cwe
   # or
   git checkout -b fix/broken-link-owasp
   # or
   git checkout -b improve/phase-5-architecture-clarity
   ```
5. Make your changes
6. Commit using the [commit format](#commit-message-format) below
7. Push your branch and open a Pull Request

### Option 3 — Propose a new section

1. Open an Issue with the label `proposal`
2. Describe: what phase/section you want to add, why it is missing, and what sources you would use
3. After discussion and approval, follow Option 2 steps above

---

## Pull Request Guidelines

When submitting a Pull Request, please:

- [ ] Use the PR template (it will load automatically)
- [ ] Keep the PR focused — one change or addition per PR
- [ ] Reference any related issue (`Closes #12` or `Related to #8`)
- [ ] Ensure all links you add are working and publicly accessible
- [ ] Do not include unrelated changes in the same PR
- [ ] Be patient — this is a maintained side project

**PR title format:**
```
add: OWASP ASVS reference to Phase 16
fix: broken link in Phase 14 deployment section  
improve: reword acceptance criteria explanation in Phase 2
remove: outdated NIST link replaced with current version
```

---

## Issue Guidelines

When opening an issue, please:

- Use one of the provided **Issue Templates** for the best experience
- Be specific — include the phase number, section name, or line reference
- For broken links, include the current broken URL and, if possible, a replacement
- For factual corrections, include the source that supports your correction

Available issue templates:
- `Add Resource` — Suggest a new reference or online resource
- `Fix Content` — Report inaccurate, outdated, or broken content

---

## Content Standards

Any content added to this guide must meet these standards:

### References (Books)
- Must be a published book, not a blog post or course
- Must include: Title, Author, Year of edition used
- Must be genuinely relevant to the phase it is added to — explain why in your PR

### References (Online Resources)
- Must be from a recognized institution, standards body, or reputable engineering organization
- Examples of accepted sources: OWASP, W3C, NIST, IETF, Google, Microsoft, Martin Fowler's blog, GitHub Engineering, Stripe Engineering, Netflix Tech Blog
- Must be publicly accessible without a paywall
- Avoid linking to tools/products unless the link goes to documentation or a free resource

### Checklist Items (TODO)
- Must be actionable — start with a verb (Define, Create, Implement, Validate, etc.)
- Must be general enough to apply across different tech stacks and product types
- Should not assume a specific framework, language, or cloud provider

---

## Commit Message Format

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>: <short description>

[optional body]
```

| Type | When to use |
|------|------------|
| `add` | Adding new content, reference, or section |
| `fix` | Fixing broken link, typo, or inaccurate content |
| `improve` | Rewording, restructuring, or clarifying existing content |
| `remove` | Removing outdated or irrelevant content |
| `chore` | Repo maintenance (README, templates, LICENSE) |

**Examples:**
```
add: circuit breaker reference to Phase 10
fix: typo in Phase 3 journey mapping section
improve: clarify normalization explanation in Phase 4
remove: deprecated tool link in Phase 9
chore: update PR template
```

---

## Recognition

All contributors will be visible in the GitHub Contributors graph.

Significant contributions (new sections, major additions) will be acknowledged in the release notes.

---

Thank you for helping make this guide better. 🙏

— **Kuril dev** ([@heyitskuril](https://github.com/heyitskuril))
