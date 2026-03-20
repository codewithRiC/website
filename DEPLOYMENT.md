# GitHub Pages Configuration for Rishi Raj Sahoo's Website

## Deployment Instructions

### Option 1: Using username.github.io Repository (Recommended)

1. **Create Repository**
   - Go to github.com and create a new repository
   - Name it: `your-username.github.io`
   - Make it public

2. **Clone and Setup**
   ```bash
   git clone https://github.com/your-username/your-username.github.io.git
   cd your-username.github.io
   ```

3. **Add Website Files**
   ```bash
   # Copy all files from this project
   cp -r /home/rishi/projects/website/* .
   git add .
   git commit -m "Add personal website"
   git push origin main
   ```

4. **Access Your Site**
   - Visit: `https://your-username.github.io`

### Option 2: Using Custom Repository with Custom Domain

1. **Create Repository**
   - Create any public repository (e.g., `website` or `portfolio`)

2. **Configure GitHub Pages**
   - Go to Settings → Pages
   - Select: "Deploy from a branch"
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`

3. **Add CNAME File** (if using custom domain)
   ```
   yourdomain.com
   ```

4. **Push Files**
   ```bash
   git add .
   git commit -m "Add website"
   git push origin main
   ```

5. **Configure Custom Domain**
   - Go to Settings → Pages
   - Add your custom domain
   - Configure DNS records with your domain provider

## File Structure for GitHub Pages

```
repository-root/
├── index.html          ← Main entry point
├── styles.css          ← Styling
├── script.js           ← JavaScript
├── _config.yml         ← Jekyll config (optional)
├── README.md           ← Repository documentation
├── package.json        ← Project metadata
├── CV.pdf              ← Your CV
└── .gitignore          ← Git ignore rules
```

## Important Notes

1. **GitHub Pages Requirements**
   - Repository must be public
   - Use correct file names (case-sensitive)
   - index.html must be in repository root

2. **HTTPS**
   - GitHub Pages serves HTTPS automatically
   - No configuration needed

3. **Custom Domain**
   - Update `_config.yml` with your domain
   - Update contact links in `index.html` if needed

4. **SEO**
   - Update meta tags in `<head>` section of index.html
   - Update description in `_config.yml`

## Testing Locally

Before deploying, test the website locally:

```bash
# Option 1: Using Python
cd /home/rishi/projects/website
python -m http.server 8000

# Option 2: Using Node.js
npx http-server

# Then visit: http://localhost:8000
```

## Maintenance

1. **Update CV**: Replace CV.pdf file
2. **Update Content**: Edit index.html sections
3. **Update Styling**: Modify styles.css
4. **Add Features**: Extend script.js

## Troubleshooting

- **Site not showing**: Ensure repository is public
- **Styling not loading**: Check file paths in index.html
- **Images not showing**: Use relative paths
- **Custom domain not working**: Check DNS and CNAME configuration

## Additional Resources

- [GitHub Pages Documentation](https://pages.github.com/)
- [GitHub Pages Custom Domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Jekyll Documentation](https://jekyllrb.com/)

---

Last Updated: January 2026
