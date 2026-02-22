# Layout Mobile Documentation

Public-facing documentation for **Layout Mobile**—a white-label mobile ordering platform for multi-location coffee shops using Square. Built with [Mintlify](https://mintlify.com).

## Audience

- Multi-location coffee shop owners using Square who want a branded mobile app
- Technical evaluators (reliability, security, Square integration)
- Early-stage investors reviewing technical credibility

## Run locally

Requires Node.js v20.17+ and the Mintlify CLI.

Install the CLI (run once):

```bash
npm i -g mint
```

Start the dev server:

```bash
mint dev
```

Then open [http://localhost:3000](http://localhost:3000).

## Deploy (GitHub → Mintlify)

1. **Push this folder to your GitHub repo** (if you haven’t already):

   ```bash
   cd /path/to/LayoutDocs
   git init
   git add .
   git commit -m "Initial docs"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git branch -M main
   git push -u origin main
   ```

2. **Connect the repo to Mintlify:**
   - Go to [mintlify.com/start](https://mintlify.com/start).
   - Sign in and connect your GitHub account.
   - Choose “Connect existing repository” and select this repo (or create a new Mintlify project and link it).
   - Install the Mintlify GitHub App when prompted so it can deploy on push.

3. **Done.** Mintlify will build and deploy on every push to the default branch. Your site will be at `https://YOUR_PROJECT.mintlify.app`. You can add a [custom domain](https://mintlify.com/docs/custom-domain) later in the Mintlify dashboard.

## Structure

- **docs.json** — Mintlify config (name, colors, navigation).
- **index.mdx** — Introduction and entry point.
- **overview.mdx** — Product scope and key concepts.
- **getting-started/quickstart.mdx** — Merchant onboarding flow.
- **architecture/** — System components, integration flow.
- **integrations/square.mdx** — Square connection, sync, payments.
- **multi-location.mdx** — Company and location model.
- **reliability.mdx** — Idempotency, order state, sync.
- **security.mdx** — Tenant isolation, auth, payments, webhooks.
- **business-value.mdx** — Value for owners, evaluators, investors.
- **public/** — Static assets (favicon, logo light/dark) served with the site so the logo doesn’t reload on every page change.

Content is high-level and avoids internal implementation details, schemas, and secrets.
