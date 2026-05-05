# Lambda - A Half-Life Inspired Hugo Theme
A dark, minimalist Hugo theme featuring Half-Life's iconic dark green and orange color scheme.

![Thumbnail](https://raw.githubusercontent.com/koenemans/repo/main/images/tn.png "Thumbnail")

## Features
- **Half-Life Aesthetic**: Dark green backgrounds (#0d1410), orange accents (#ff6600), and green links (#00ff66)
- **Responsive Images**: Automatic WebP conversion with 1x/2x srcsets
- **Clean Typography**: Monospace fonts throughout for a terminal-like feel
- **Breadcrumb Navigation**: Automatic breadcrumb generation

## Installation
### As a Git Submodule
```bash
cd your-hugo-site
git submodule add https://github.com/koenemans/lambda.git themes/lambda
```

### Manual Installation
```bash
cd your-hugo-site/themes
git clone https://github.com/koenemans/lambda.git lambda
```

## Configuration
Add the theme to your `hugo.toml`:

```toml
theme = 'lambda'

[params]
description = 'Your site description'
author = 'Your Name'
```

## Customization
### Colors and Spacing
The theme uses CSS custom properties for consistent styling. Override them in your site's `static/css/custom.css`:

```css
:root {
  /* Spacing scale (8px base unit) */
  --space-xs: 0.5rem;   /* 8px */
  --space-sm: 1rem;     /* 16px */
  --space-md: 1.5rem;   /* 24px */
  --space-lg: 2rem;     /* 32px */
  --space-xl: 3rem;     /* 48px */

  /* Colors */
  --color-green-primary: #00ff66;
  --color-orange-primary: #ff8c00;
  --color-orange-accent: #ff6600;
  --color-orange-light: #ff9933;
  --color-text-primary: #c5d1cf;
  --color-text-dim: #6b7975;
  --color-bg-dark: #0d1410;
  --color-bg-medium: #1a2420;
  --color-bg-darker: #0f1814;
  --color-border: #2d3d35;
}
```

All theme styles use these custom properties for consistency. You can customize any of these values to match your preferences while maintaining the design system.

## Dependencies
- **Hugo**: v0.112.0 or later (required for WebP image processing)

## License
MIT License - See [LICENSE](https://raw.githubusercontent.com/koenemans/repo/main/LICENSE) file for details

## Credits
Inspired by the Half-Life video game series by Valve Corporation.

Theme structure inspired by [Blank](https://github.com/Vimux/blank) by Vimux.

Theme created by [Koenraad](https://koenra.ad).

## Contributing
Issues and pull requests are welcome at the [GitHub repository](https://github.com/koenemans/lambda).
