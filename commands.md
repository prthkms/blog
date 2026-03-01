# Hugo Blog — Common Commands

## Local Development

```bash
# Serve with drafts visible
hugo server -D

# Serve published content only
hugo server
```

Site is available at http://localhost:1313

## Build

```bash
hugo
```

Outputs static files to `public/`.

## New Post

```bash
hugo new posts/my-post-title.md
```

Edit the generated file in `content/posts/`. Change `draft = true` to `draft = false` when ready to publish.

## Submodule Init (fresh clones)

```bash
git submodule update --init --recursive
```

Run this after cloning the repo to pull in the `themes/terminal` submodule.

## Cloudflare Pages Setup (Dashboard)

When connecting the GitHub repo in the Cloudflare Pages dashboard:

| Setting | Value |
|---|---|
| Framework preset | Hugo |
| Build command | `hugo` |
| Build output directory | `public` |
| Environment variable | `HUGO_VERSION = 0.157.0` |

## Publishing Workflow

```bash
git add .
git commit -m "your message"
git push
```

Cloudflare Pages automatically detects the push and deploys the new build.
