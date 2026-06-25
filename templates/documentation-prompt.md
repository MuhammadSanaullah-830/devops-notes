# Recommended File Name

`templates/documentation-prompt.md`

---

# GitHub Documentation Generation Prompt

Act as a Senior DevOps Engineer and Technical Documentation Writer.

Create a professional GitHub-ready Markdown (`.md`) document for the following topic:

`[TOPIC NAME]`

## Requirements

* Use proper Markdown formatting.
* Add a clear title and introduction.
* Organize content with headings and subheadings.
* Include practical examples.
* Include command examples in code blocks.
* Explain each command briefly.
* Add a Best Practices section.
* Add a Troubleshooting section (if applicable).
* Add a Common Mistakes section.
* Add a Security Considerations section (if applicable).
* Add a Quick Reference Cheat Sheet at the end.
* Structure the document so it can be directly saved as a `.md` file inside a GitHub repository.
* Use a concise but professional DevOps documentation style.
* Do not include unnecessary explanations.
* Make the document production-ready and useful for future reference.
* Include a recommended file name at the top.

## Output Requirements

* Output only the Markdown document.
* Do not add explanations outside the document.
* Ensure the content is GitHub-ready and properly formatted.

---

## Example Usage

### Example 1

```text
Act as a Senior DevOps Engineer and Technical Documentation Writer.

Create a professional GitHub-ready Markdown (.md) document for the following topic:

MySQL User Management
```

### Example 2

Use the same prompt and only replace the topic:

```text
AWS IAM User Management
Terraform Basics
Kubernetes RBAC
Docker Commands Cheat Sheet
Linux User Management
Nginx Reverse Proxy Setup
Git Branching Strategy
Jenkins Pipeline Setup
AWS EC2 Troubleshooting
MySQL Backup and Restore
```

## Notes

Create a repository folder named:

```text
templates/
```

Save this prompt as:

```text
templates/documentation-prompt.md
```

Whenever you need new documentation, replace only:

```text
[TOPIC NAME]
```

and generate the document.
