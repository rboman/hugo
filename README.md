# My Hugo Website

A basic Hugo website using the Ananke theme as a git submodule, deployed on GitHub Pages.

![Hugo Website](https://github.com/user-attachments/assets/7d2b0915-136e-4f24-bd48-14453c2733d6)

## Features

- Static site generation with Hugo
- Ananke theme via git submodule
- Automated deployment to GitHub Pages via GitHub Actions
- Sample content included

## Local Development

1. Clone the repository with submodules:
```bash
git clone --recurse-submodules https://github.com/rboman/hugo.git
cd hugo
```

2. If you already cloned without submodules, initialize them:
```bash
git submodule update --init --recursive
```

3. Install Hugo (if not already installed):
- Visit [Hugo Releases](https://github.com/gohugoio/hugo/releases)
- Download and install the extended version for your platform

4. Run the development server:
```bash
hugo server
```

5. View the site at `http://localhost:1313/hugo/`

## Building for Production

Build the static site:
```bash
hugo
```

The generated site will be in the `public/` directory.

## Deployment

This site is configured to automatically deploy to GitHub Pages when changes are pushed to the `main` branch.

### Setup GitHub Pages

1. Go to your repository Settings > Pages
2. Set Source to "GitHub Actions"
3. The workflow will automatically build and deploy on push to `main`

## Adding Content

Create a new post:
```bash
hugo new content/posts/my-post.md
```

Edit the post and set `draft = false` to publish it.

## Theme

This site uses the [Ananke theme](https://github.com/theNewDynamic/gohugo-theme-ananke) as a git submodule.

## Configuration

The site configuration is in `hugo.toml`. Key settings:

- `baseURL`: Set to your GitHub Pages URL
- `title`: Your site title
- `theme`: Set to "ananke" (the git submodule)
