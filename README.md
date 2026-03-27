# Screenshot Service

GitHub Actions workflow for capturing website screenshots.

## Usage

This repository contains a GitHub Actions workflow that captures screenshots of websites via `workflow_dispatch`.

### Workflow: `.github/workflows/screenshot.yml`

**Inputs:**
- `url` - Website URL to capture
- `width` - Viewport width (default: 1920)
- `height` - Viewport height (default: 1080)
- `request_id` - Unique request identifier

**Output:**
- Screenshot saved as base64-encoded PNG in `screenshot.txt`
- Uploaded as artifact with 1-day retention

## Integration

This workflow is used by the ZeO Proofing SPFx WebPart for capturing website screenshots.

The WebPart triggers this workflow via GitHub API and downloads the resulting screenshot artifact.
