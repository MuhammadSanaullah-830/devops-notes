# Recommended File Name

`templates/documentation-prompt.md`

---

# GitHub Documentation Generation Prompt

Act as a Senior DevOps Engineer and Technical Documentation Writer.

Create a professional GitHub-ready Markdown (.md) document for the following topic:

`[TOPIC NAME]`

---

## Requirements

* Use proper Markdown formatting.
* Add a clear title and introduction.
* Organize content with headings and subheadings.
* Include practical examples.
* Include command examples in code blocks.
* Explain each command briefly.
* Add a Best Practices section.
* Add a Troubleshooting section (if applicable).
* Add a Common Mistakes section (if applicable).
* Add a Security Considerations section (if applicable).
* Add a Quick Reference Cheat Sheet at the end.
* Structure the document so it can be directly saved as a .md file inside a GitHub repository.
* Use a concise but professional DevOps documentation style.
* Do not include unnecessary explanations.
* Make the document production-ready and useful for future reference.
* Include a recommended file name at the top.

---

## 🚀 Enhanced GitHub Notes Intelligence Layer

### 1. Auto File Naming Convention

Generate file names using this format:

* lowercase only
* hyphen-separated
* clear and descriptive
* include domain context when possible

Examples:

* mysql-user-management.md
* aws-iam-basics.md
* kubernetes-rbac-guide.md
* terraform-state-management.md
* linux-user-management.md

---

### 2. Auto Folder Classification

Automatically choose correct folder from:

* mysql/
* aws/
* kubernetes/
* terraform/
* linux/
* docker/
* cicd/
* networking/
* troubleshooting/

If topic spans multiple domains, choose the PRIMARY domain based on core purpose.

---

### 3. Visibility Recommendation (Important)

Always suggest whether the note should be:

* **Public** → generic DevOps knowledge, commands, concepts, tutorials
* **Private** → sensitive, internal, lab-specific, security-related, or environment-specific data

Also provide a 1-line reason for the decision.

---

### 4. Metadata Section (NEW)

At the top of every Markdown file, include:

```md
## Metadata
- Category: <AWS / MySQL / Kubernetes etc.>
- Difficulty: Beginner / Intermediate / Advanced
- Tags: <comma-separated relevant tags>
