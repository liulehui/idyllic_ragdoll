# Idyllic Ragdoll Cattery Website

A Hugo-based website for Idyllic Ragdoll Cattery, built with the Vex Hugo theme. This website showcases ragdoll cats, kings, queens, kittens, and provides contact information for potential adopters.

## Prerequisites

Before you can run this website locally, you need to install:

1. **Hugo** (Extended version) - [Installation Guide](https://gohugo.io/getting-started/installing/)
2. **Git** - [Download Git](https://git-scm.com/downloads)

## Local Development Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/idyllic-ragdoll.git
cd idyllic-ragdoll
```

### 2. Initialize Theme Submodule (if needed)

If the theme is included as a submodule, run:

```bash
git submodule update --init --recursive
```

### 3. Install Hugo (if not already installed)

**macOS (using Homebrew):**
```bash
brew install hugo
```


### 4. Run the Development Server

Start the Hugo development server:

```bash
hugo server
```

The website will be available at: **http://localhost:1313**

### 5. View Different Language Versions

This website supports multiple languages:
- **English**: http://localhost:1313/
- **Chinese**: http://localhost:1313/zh/

## Development Commands

### Build the Website

```bash
hugo
```

This creates a `public/` directory with the compiled website.

### Build with Draft Content

```bash
hugo server -D
```

### Build with Future Content

```bash
hugo server -F
```

### Clean Build Cache

```bash
hugo mod clean
```

## Project Structure

```
idyllic-ragdoll/
├── archetypes/          # Content templates
├── assets/             # CSS, JS, and other assets
├── content/            # Website content
│   ├── english/        # English content
│   ├── chinese/        # Chinese content
│   └── french/         # French content
├── data/               # Data files (homepage content)
├── i18n/               # Internationalization files
├── layouts/            # Hugo templates
├── public/             # Generated website (after build)
├── resources/          # Hugo generated resources
├── static/             # Static files (images, etc.)
├── themes/             # Hugo themes
│   └── vex-hugo/       # Vex Hugo theme
├── config.toml         # Main configuration file
└── README.md           # This file
```

## Content Management

### Adding New Content

1. **Kittens**: Add new kitten profiles in `content/english/kittens/` or `content/chinese/kittens/`
2. **Kings**: Add king profiles in `content/english/kings/` or `content/chinese/kings/`
3. **Queens**: Add queen profiles in `content/english/queens/` or `content/chinese/queens/`

### Content Format

Each content file should include front matter:

```yaml
---
title: "Kitten Name"
date: 2024-01-15
draft: false
image: "images/kittens/kitten-name.jpg"
description: "Description of the kitten"
---
```

## Configuration

Main configuration is in `config.toml`. Key settings include:

- **Base URL**: Set your production URL
- **Languages**: Configure English, Chinese, and French versions
- **Navigation**: Customize menu items
- **Theme Settings**: Logo, colors, and other theme-specific options

## Images

Place images in:
- `static/images/` for general images
- `static/images/kittens/` for kitten photos
- `static/images/kings/` for king photos
- `static/images/queens/` for queen photos

## Deployment

This website is configured for easy deployment to:

1. **Netlify**: Use the `netlify.toml` configuration
2. **GitHub Pages**: Build and deploy using GitHub Actions
3. **Any static hosting**: Upload the `public/` directory

## Troubleshooting

### Common Issues

1. **Theme not loading**: Ensure the theme is properly installed in `themes/vex-hugo/`
2. **Images not showing**: Check image paths in content files
3. **Language switching not working**: Verify language configuration in `config.toml`

### Getting Help

- Check [Hugo Documentation](https://gohugo.io/documentation/)
- Review [Vex Hugo Theme Documentation](https://docs.gethugothemes.com/vex/)
- Check the theme's [GitHub Repository](https://github.com/themefisher/vex-hugo)