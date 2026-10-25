# Alex Hill Woodworks — customer care pages

Public-facing care and instruction pages only. Technical documentation, compliance evidence and production records remain in the private `alexhillwoodworks-lighting` repository.

## Publishing

The private repository owns the source files under `site/`. Its `Publish customer care site` GitHub Actions workflow synchronises that directory to this repository using a fine-grained token stored as `CARE_REPO_TOKEN` in the private repository's Actions secrets.

A separate workflow in this repository deploys `site/` to GitHub Pages when changes reach `main`.

**Do not edit pages in this repository:** the next source publication can replace them.

## One-time activation

1. In this repository's **Settings → Pages**, select **GitHub Actions** as the build/deployment source.
2. Create a GitHub fine-grained personal access token restricted to **alexhillsre/alexhillwoodworks-care** with **Contents: Read and write**. Choose a sensible expiration and calendar a renewal. No Actions/administration permissions are required.
3. In the **private** repository's **Settings → Secrets and variables → Actions**, create a repository secret named **CARE_REPO_TOKEN** containing that token.
4. In the private repository's **Actions**, run **Publish customer care site** with **Run workflow** (or update a file under `site/`).
5. Verify the public repo's **Deploy care site to GitHub Pages** workflow succeeds before producing printed QR codes.

The default project URL is `https://alexhillsre.github.io/alexhillwoodworks-care/` with product instructions at `care/beaver/`. If you later connect a custom domain, configure it in the public repo's Pages settings and update your planned QR destination before printing.

## Caution

The Beaver Lamp care instructions are draft product guidance. Verify the bulb rating, electrical safety requirements and required physical markings/instructions before putting the lamp on sale.
