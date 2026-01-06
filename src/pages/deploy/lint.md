**Automated**: Runs on PRs and deploy when `src/pages/**` files change

**Manual**: `npm run lint`

Validates markdown syntax, links, content structure, and Adobe style guidelines.

### Running from Another Repo

You can run the linter from any other repo using npx:

```bash
# Run all linting rules (errors and summary only)
npx --yes github:AdobeDocs/adp-devsite-utils runLint

# Run with verbose output (shows all files processed and details)
npx --yes github:AdobeDocs/adp-devsite-utils runLint -v

# Run all linting rules EXCEPT dead links (faster)
npx --yes github:AdobeDocs/adp-devsite-utils runLint --skip-dead-links

# Check only for dead external links
npx --yes github:AdobeDocs/adp-devsite-utils runLint --dead-links-only

```

**Options:**
- `-v` or `--verbose` - Show detailed output including all files processed
- `--dead-links-only` - Only check for dead external URLs (skips all other linting rules)
- `--skip-dead-links` - Run all linting rules EXCEPT dead links check (faster)

**Troubleshooting**: If pages are not showing up as expected, check lint errors or warnings to identify potential issues.