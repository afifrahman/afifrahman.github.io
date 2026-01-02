# GitHub Pages Deployment Troubleshooting

## ⚠️ ACTION REQUIRED

**If your website is not live, you need to complete one manual configuration step.**

## Quick Diagnosis

### Is your site live?
Visit [https://afifrahman.github.io](https://afifrahman.github.io)

- ✅ **Site loads**: Deployment is working correctly!
- ❌ **404 or DNS error**: Follow the steps below (this is expected if you haven't configured the Pages source yet)

## Most Common Issue: Pages Source Not Set to GitHub Actions

### The Problem
GitHub Pages can deploy from two sources:
1. **Branch deployment** (legacy method)
2. **GitHub Actions** (modern method, used by this repository)

If the repository is configured for branch deployment but your workflow uses GitHub Actions deployment, the site won't be published even though the workflow succeeds.

### The Solution

**Step 1: Check Current Settings**
1. Go to your repository on GitHub
2. Click **Settings** (top right)
3. Scroll down and click **Pages** (left sidebar)
4. Look at the **Source** section

**Step 2: Configure for GitHub Actions**
If the Source shows "Deploy from a branch":
1. Click the dropdown under **Source**
2. Select **"GitHub Actions"**
3. Click **Save** (if there is one)
4. Wait 2-3 minutes for the change to take effect

**Step 3: Trigger a Fresh Deployment**
After changing the settings:
1. Go to the **Actions** tab
2. Click on "Deploy static content to Pages"
3. Click "Run workflow"
4. Select the `main` branch
5. Click "Run workflow" button

**Step 4: Wait and Verify**
1. Wait for the workflow to complete (usually ~1 minute)
2. Visit [https://afifrahman.github.io](https://afifrahman.github.io)
3. The site should now be live!

## Verification Checklist

Before troubleshooting, verify these basics:

- [ ] GitHub Pages is enabled in repository settings
- [ ] The repository is named `afifrahman.github.io` (correct format: `username.github.io`)
- [ ] The `main` branch exists and has the website files
- [ ] The workflow file exists at `.github/workflows/static.yml`
- [ ] Recent workflow runs show success (check Actions tab)

## Other Possible Issues

### Issue: Workflow Fails
**Symptoms:** The "Deploy static content to Pages" workflow shows failures in the Actions tab

**Solutions:**
1. Check the workflow logs for specific errors
2. Ensure the workflow has proper permissions (already configured in `static.yml`)
3. Verify the `GITHUB_TOKEN` has Pages write permissions

### Issue: DNS Not Resolving
**Symptoms:** Browser shows "DNS_PROBE_FINISHED_NXDOMAIN" or similar

**Solutions:**
1. GitHub Pages DNS can take 10-15 minutes to propagate after first deployment
2. Try clearing your browser's DNS cache
3. Try accessing the site from a different network or using a mobile device

### Issue: 404 Error
**Symptoms:** Site loads but shows "404 - File not found"

**Solutions:**
1. Verify `index.html` exists in the repository root (it does)
2. Check that `.nojekyll` file exists (it does)
3. Ensure the workflow uploaded the correct files (check workflow logs)

## Advanced Diagnostics

### Check Deployment Status via API
```bash
curl -H "Accept: application/vnd.github+json" \
  https://api.github.com/repos/afifrahman/afifrahman.github.io/pages
```

Look for:
- `"status": "built"` - Pages is ready
- `"html_url"` - Should be "https://afifrahman.github.io"

### Verify Workflow Deployment
```bash
curl -H "Accept: application/vnd.github+json" \
  https://api.github.com/repos/afifrahman/afifrahman.github.io/deployments
```

Should show recent deployments with `"environment": "github-pages"`

## Still Not Working?

If you've tried everything above and the site still isn't live:

1. **Check GitHub Status**: Visit [https://www.githubstatus.com/](https://www.githubstatus.com/) to see if Pages is experiencing issues

2. **Repository Visibility**: Ensure the repository is public (GitHub Pages doesn't work on private repos for free accounts)

3. **Contact GitHub Support**: If all else fails, open a support ticket at [https://support.github.com](https://support.github.com)

## Summary

The most likely fix is:
1. Go to Settings > Pages
2. Change Source to "GitHub Actions"
3. Wait a few minutes
4. Your site will be live at [https://afifrahman.github.io](https://afifrahman.github.io)

✨ That's it!
