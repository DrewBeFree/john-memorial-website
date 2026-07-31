# Cloudflare Pages Migration — 2026-07-31

Host/worktree: `/home/drew/workspace/john-memorial-website`
Branch: `main`
Commit: `cb3f291 chore: untrack local symlink to prevent deployment failures`
Remote: `https://github.com/DrewBeFree/john-memorial-website.git`

## Outcome

Factual summary of what changed:
1. **GitHub Repository Renamed:** Changed the repository name back to `john-memorial-website` from `DrewBeFree.github.io` via `gh repo rename`.
2. **Local Remote Synchronized:** Local repository's remote tracking configuration updated automatically to sync with the new repo name.
3. **Legacy GitHub Pages Artifact Removed:** Deleted the `CNAME` file from the repository as it was specific to GitHub Pages and is ignored by Cloudflare Pages.
4. **Resolved Cloudflare Build Conflict:** Discovered and fixed a build failure (`build output directory contains links to files that can't be accessed`) caused by a tracked local symlink `source -> /mnt/data/Documents/12-john`. Untracked the symlink and added it to `.gitignore` to keep it local-only and clean.
5. **Cloudflare Pages Deployment:** Connected and configured the repository with Cloudflare Pages as a pure static HTML deployment with no build command.
6. **DNS Management Migrated to Cloudflare:** Transferred nameserver control for the apex domain `johnthepianoman.com` to Cloudflare Custom DNS (`camilo.ns.cloudflare.com` and `emma.ns.cloudflare.com`) to support automatic SSL, performance caching, and proper CNAME flattening for the apex domain.
7. **Cleaned Up Legacy DNS Records:** Removed old GitHub Pages A/CNAME records from Cloudflare during DNS setup to prevent conflicts.
8. **Linked Custom Domain:** Added the apex domain `johnthepianoman.com` to the Cloudflare Pages project.
9. **Production Verification:** Verified that `https://johnthepianoman.com` resolves correctly over HTTPS with an `HTTP/2 200 OK` response.

## Why this was done

GitHub Pages imposes strict limitations on custom apex domains (domains without a subdomain like `www.`), often requiring manual hacks or leading to 404 errors during routing updates. Cloudflare Pages offers a far more robust, free static-hosting platform with native support for CNAME flattening, automatic edge SSL certificate provisioning, and high-performance caching.

## Commands run

```bash
# Check initial git remote state and GitHub CLI authorization status
git status && git remote -v && gh auth status

# Rename GitHub repo back to the clean project name
gh repo rename john-memorial-website --yes

# Verify automatic remote URL updates
git remote -v

# Clean up legacy CNAME file
rm CNAME && git add CNAME && git commit -m "chore: remove GitHub Pages CNAME file" && git push origin main

# Find all symlinks causing Cloudflare Pages build errors
find . -maxdepth 3 -type l

# Untrack local symlink from Git but preserve it on local disk
echo -e "\n# Local workspace symlinks\nsource" >> .gitignore
git rm --cached source
git add .gitignore
git commit -m "chore: untrack local symlink to prevent deployment failures"
git push origin main

# Live production verification
dig @1.1.1.1 johnthepianoman.com NS +short
curl -I https://johnthepianoman.com
```

Observed result:

```text
dns1.registrar-servers.com.
dns2.registrar-servers.com.
...
camilo.ns.cloudflare.com.
emma.ns.cloudflare.com.

HTTP/2 200 
date: Fri, 31 Jul 2026 11:18:07 GMT
content-type: text/html; charset=utf-8
server: cloudflare
```

## Safety notes

- No private investigation or sensitive documents were exposed.
- The `source` directory link is preserved locally for Drew's workspace use, but is completely excluded from the public GitHub repository.
- Legacy Namecheap email forwarding records (MX and TXT records) were preserved exactly as-is to ensure email continues to function.

## Next recommended step

1. Curate and copy public-safe images into `assets/slideshow/` to replace the placeholder slides in the slideshow.
2. Generate the production-ready QR code using `https://johnthepianoman.com` as the target URL, then save the QR asset to the repo.
