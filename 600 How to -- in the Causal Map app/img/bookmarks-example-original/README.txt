PNG files: bookmark-{id}.png (stable names).

If you see tiny grey 1x1 placeholders, run the export script below to replace them with real screenshots.

Generate from repo causal-map-extension:
  python scripts/export_bookmark_images.py --use-database --env-file webapp/.env --out-dir "<this-folder>"
or with a browser session JWT instead of --use-database.

See webapp/README.md section "Export bookmark images for documentation (Garden)".

After export, manifest.json lists id + description for captions.
For a human-readable planning list, see bookmark-image-manifest.txt. It is .txt so Garden builds do not render it as a page.
