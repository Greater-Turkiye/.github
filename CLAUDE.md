# Repository rules — Greater-Turkiye/.github

This repository holds the organisation profile, the community health files that every repository inherits, the issue and discussion templates, and the membership workflow.

## 1. Keep the documentation true

**The README is part of the change, not an afterthought.**

- Any pull request that adds or changes a template, a workflow, a label, a variable or a community file **must update `README.md` in the same pull request**, and `profile/README.md` when the organisation's public front page is affected.
- Contributor-facing changes also update `CONTRIBUTING.md` or `SUPPORT.md` where those describe the same flow.
- Never leave a document describing a template or a workflow that no longer exists.

## 2. Membership workflow

- `ISSUE_TEMPLATE/06-membership.yml` plus `.github/workflows/membership.yml` turn a membership request into an invitation to the read-only `katilimcilar` team.
- Approval is the default (`vars.GT_JOIN_MODE`); only repository admins may approve, and the workflow removes the approval label if anyone else adds it.
- New members never receive write access. Contributions stay pull-request based and reviewed.
- Issue text is untrusted input: read it inside `github-script`, never interpolate it into a shell command, and keep every action pinned to a commit SHA.
- The invitation needs the organisation's GitHub App token; `GITHUB_TOKEN` cannot invite members. When the App is not configured the workflow must degrade to a manual invitation instead of failing.

## 3. Red lines

- Templates must keep their warnings: the forms are public, and personal data, leaked material or information about Turkish forces belongs in the private security channel instead.
- Never weaken a template's required agreement checkboxes.

## 4. Git and pull requests

- Never commit to `main`; `main` is protected. Work on a branch and squash-merge a pull request.
- Commit messages and PR bodies are in English and end with the attribution lines used across this org.
- Never commit secrets, tokens or private keys; credentials are added to GitHub secrets by a human.

## 5. Closing a task

- End every finished task with a short, factual summary: what changed, what you verified, what is merged, and what is still open.
- Then offer the next steps as a numbered list (1, 2, 3), each one sentence, with your recommendation marked, so the owner can choose by number.
- Name anything the owner must do themselves as its own option rather than burying it in prose.

## 6. Environment notes

- Windows PowerShell 5.1 is the default shell here: pass multi-line commit messages and PR bodies through files, and avoid `jq` expressions containing spaces.
