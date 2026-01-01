# From Inflammation to Healing: Bram's Journey

A free, open-source health resource for contractors and blue-collar workers dealing with chronic inflammation, mold illness, and joint pain.

## Local Development

```bash
# Install dependencies
pip install mkdocs-material

# Serve locally (with live reload)
mkdocs serve

# Build static site
mkdocs build
```

Site will be available at `http://127.0.0.1:8000`

## Deployment

This repo uses GitHub Actions to automatically build and deploy on push to `main`.

### Setup (one-time)

1. Go to your repo → **Settings** → **Secrets and variables** → **Actions**
2. Add these repository secrets:

| Secret Name | Value |
|-------------|-------|
| `FTP_SERVER` | Your FTP host (e.g., `ftp.example.com`) |
| `FTP_USERNAME` | Your FTP username |
| `FTP_PASSWORD` | Your FTP password |
| `FTP_SERVER_DIR` | Remote directory (e.g., `/public_html/` or `/htdocs/`) |

3. Push to `main` — the action will build and deploy automatically.

### Manual Deploy

You can also trigger a deploy manually:
1. Go to **Actions** tab
2. Select "Build and Deploy" workflow
3. Click "Run workflow"

## Project Structure

```
docs/
├── index.md              # Home page
├── disclaimers.md        # Medical/legal disclaimers
├── journey/              # Bram's story (11 chapters)
├── exercises/            # Daily 8, Invisible 8, Office adaptations
├── protocols/            # Diet, supplements, cannabis, mushrooms
└── resources/            # Quick references, templates, reading list
```

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)

Share freely. Adapt as needed. Help others heal.
