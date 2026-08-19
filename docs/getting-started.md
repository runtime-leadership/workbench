# Getting Started

Create a private repository before adding employee, company, customer, project, or code context.

## Recommended: Use the GitHub Template

1. Open the [Workbench repository](https://github.com/runtime-leadership/workbench).
2. Select **Use this template**, then **Create a new repository**.
3. Choose your account or organization as the owner.
4. Set the new repository visibility to **Private**.
5. Create the repository, clone it, and open it with your preferred tool.

This creates an independent repository without connecting it to Workbench's public fork network.

## Alternative: Clone and Replace the Remote

If you prefer to start from the command line, clone Workbench and preserve the canonical repository as `upstream`:

```bash
git clone https://github.com/runtime-leadership/workbench.git my-workbench
cd my-workbench
git remote rename origin upstream
```

Create a private GitHub repository and push the local copy in one step with GitHub CLI:

```bash
gh repo create YOUR-NAME/my-workbench --private --source=. --remote=origin --push
```

Or create an empty private repository through GitHub, then connect it manually:

```bash
git remote add origin git@github.com:YOUR-NAME/my-workbench.git
git push -u origin main
```

Afterward:

- `origin` is your private working repository.
- `upstream` is the public canonical Workbench repository.
- Review upstream changes before adopting them; updates are options, not mandatory migrations.

Do not add private context while `origin` still points to the public Workbench repository.
