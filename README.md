# Digi Baba Academy – Private Source Repo

This is the **private source repository** for the Digi Baba Academy website.

- Edit `index.html` and any other source files here.
- A GitHub Action in `.github/workflows/publish.yml` will push the built/static files to your **public** repository.

## Setup steps

1. Create a **Personal Access Token (PAT)** on GitHub with scopes: `repo`, `workflow`.
2. In this private repo, go to **Settings → Secrets and variables → Actions → New repository secret**:
   - Name: `PUBLIC_PUSH_TOKEN`
   - Value: _your PAT token_
3. Edit `.github/workflows/publish.yml` and replace:
   - `YOUR_GITHUB_USERNAME` → your actual GitHub username
   - `PUBLIC_REPO_NAME` → your public repo name (for example: `digibabaacademy-public`)
   - `your-email@example.com` → your email for git commits.
4. Push changes. On every push to `main`, the workflow will sync static files to the public repo.
