# hugo-mock-landing-page

This repo shows a mockup of a landing page for a learning management system. It is based on Felipe Carneiro's Hugo Bootstrap Theme. Visit https://ang-won.github.io/hugo-mock-landing-page/ to see the result.

### Description of Workflow

The YAML file is a GitHub Actions workflow that automatically builds and deploys a Hugo website to GitHub Pages. Here are the key points:

1. The workflow triggers whenever code is pushed to the main branch
2. It uses Ubuntu 22.04 as the build environment
3. Key actions:
   - `actions/checkout` fetches your repository code and Hugo themes
   - `peaceiris/actions-hugo` sets up Hugo (version 0.144.1)
   - `hugo -D --gc --minify` builds the site with drafts included and minimizes file sizes
   - `peaceiris/actions-gh-pages` deploys to GitHub Pages

The workflow automates what would otherwise be manual steps: setting up Hugo, building the site, and deploying to GitHub Pages. The `--minify` flag is particularly useful as it reduces file sizes by removing unnecessary whitespace, comments, and optimizing code, resulting in faster page loads.

The workflow uses GitHub's automatic authentication token and commits changes using a bot account, making it secure and maintainable.
