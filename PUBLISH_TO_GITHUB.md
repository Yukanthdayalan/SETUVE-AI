# Publishing the Round 1 documentation on GitHub

The connected GitHub tool currently available for this conversation can **add files to an existing repository** but cannot create a new repository. This package has therefore been prepared as a ready-to-push folder.

## Option A — GitHub website and Git (recommended)

1. Sign in to GitHub and visit **https://github.com/new**.
2. Create a new repository named **`Setuve-AI`**. Add description: “Round 1 documentation for a multilingual agentic AI market-readiness assistant for micro food processors.”
3. Choose visibility intentionally: **Public** if sharing a documentation-only submission; **Private** if still reviewing. Do **not** initialize it with a README, because this package contains one.
4. Download and extract the project ZIP supplied in the chat.
5. Open a terminal inside the extracted **Setuve-AI** folder and run:

```bash
git init
git add .
git commit -m "docs: initialize Setuve AI Round 1 proposal"
git branch -M main
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/Setuve-AI.git
git push -u origin main
```

Replace `YOUR_GITHUB_USERNAME` with your actual GitHub username. You may need to authenticate with GitHub's supported credential manager. These commands publish **documentation**, not application code.

## Option B — Create the empty repository, then ask ChatGPT to populate it

Once the repository exists, share the exact `owner/Setuve-AI` name. The connected GitHub tools may then be able to commit the Markdown documents directly, subject to repository permissions.

## Before publishing

- Add actual team names only if members consent to public display.
- Remove any secret, private recipe, address, API key, FSSAI number or unapproved evidence from public assets.
- Review legal claims, links, logos, competition rules and the project-name conflict.
- Pick a license if you want to allow reuse. No open-source license is assumed here.
- Keep prototype claims accurate: Round 1 = **documentation only**.
