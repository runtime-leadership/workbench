# Security and Privacy in a Private Workbench

A private Workbench often accumulates real organizational, team, and personal context over time. That is the point, durable knowledge makes agents and skills more useful, but it also means a private instance may end up holding the kind of information that must never leave your control. This page lays out concrete rules for using a private Workbench safely, and for anyone who also maintains their own fork of the canonical repository.

## What Must Never Be Committed

- Credentials, API keys, tokens, passwords, private keys, or anything else that grants access to a system
- Customer data beyond what your organization's policy explicitly allows
- Confidential business information you are not authorized to disclose, even to your own private repository, if company policy restricts where it may be stored
- Personally identifiable information about colleagues or customers beyond what is necessary and approved (for example, avoid home addresses, personal phone numbers, or health information)
- Anything your employer's data handling policy designates as belonging in an approved company system rather than a personal tool

If you are unsure whether something belongs in a private Workbench, do not add it until you have confirmed it is appropriate under your organization's policies.

## `knowledge/` and `projects/` Are Private By Design

These directories exist specifically to hold your own working context. They are never part of the canonical repository's tree and should never be pushed to the canonical repository, a public fork, or any other shared remote. Treat anything placed here as staying local to your own private instance unless you deliberately decide to generalize and publish it, see below.

## Contributing Improvements Back to the Canonical Repository

If your private Workbench produces a template, resource, skill, or agent that would help others, and it contains nothing specific to your organization or personal context, you may want to contribute a generalized version back to the canonical repository.

The safe pattern for doing this:

1. If you track the canonical repository as a second remote in your private instance (commonly named `upstream`), disable its push URL entirely so it is not possible to push private history to it, even by mistake:
   ```
   git remote set-url --push upstream DISABLED
   ```
   Fetching and merging from `upstream` still work normally; only pushing is blocked.
2. Maintain a separate, personal fork of the canonical repository, unrelated to your private instance's history, used only for publishing.
3. When something is ready to share: manually copy the specific, reviewed file into the fork, confirm nothing organization-specific or private remains in it, commit, and open a pull request against the canonical repository's default branch.
4. The canonical repository enforces this path structurally: direct pushes to any branch are restricted for everyone, including maintainers, and the default branch requires a pull request before merging. The only way any change reaches the canonical repository is a reviewed pull request opened from a fork.
5. Opening a pull request and merging it are two separate decisions. Even if a tool or agent acting on your behalf has the technical ability to merge, merging into the canonical repository is always a distinct, explicit human decision made at the time, not something to infer from earlier context or from the pull request simply being open and ready.

This keeps the two histories independent, makes it structurally difficult to leak private content, and gives every change a reviewable diff before it becomes part of the shared, public resource.

---

For repository conventions and ownership boundaries, see the [Maintainer Guide](maintainer-guide.md).
