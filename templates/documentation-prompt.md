---

# 🚀 Enhanced GitHub Notes Intelligence Layer (Optional Upgrade)

If possible, also perform the following enhancements:

## 1. Auto File Naming Convention

Generate file names using this format:

- lowercase only
- hyphen-separated
- include domain prefix

Examples:

- mysql-user-management.md
- aws-iam-basics.md
- kubernetes-rbac-guide.md
- terraform-state-management.md

---

## 2. Auto Folder Classification

Automatically choose correct folder from:

- mysql/
- aws/
- kubernetes/
- terraform/
- linux/
- docker/
- cicd/
- networking/
- troubleshooting/

If topic is mixed, choose the PRIMARY domain.

---

## 3. Visibility Recommendation (Important)

Always suggest:

- Public → generic DevOps knowledge, commands, concepts
- Private → sensitive, internal, lab-specific, or security-related content

Add 1-line reason.

---

## 4. Add Metadata Section (NEW)

At the top of Markdown content, include:

```md
## Metadata
- Category: <AWS / MySQL / Kubernetes etc.>
- Difficulty: Beginner / Intermediate / Advanced
- Tags: <comma separated tags>
