# News Theme

A newspaper theme for [Pagible CMS](https://pagible.com), designed for daily reporting, business desks, and editorial publications.

This package is part of the [Pagible CMS monorepo](https://github.com/aimeos/pagible).

## Installation

```bash
composer require aimeos/pagible-themes-news
php artisan vendor:publish --tag=cms-theme
```

## Design

- **Style**: Dense financial-newspaper layout with a utility band, compact centered masthead, section rail, lead story with an editor’s-picks rail, top-story columns, and a numbered most-read rail
- **Colors**: One continuous cool-grey newsprint surface (`#F8FBFF`), ink (`#33302E`), editorial-blue links (`#2E6E9E`), claret kickers (`#9E2F50`), and a near-black utility header (`#262A33`)
- **Typography**: System serif masthead and headlines with compact sans-serif navigation, dates, metadata, and controls
- **Geometry**: Sharp corners, thin editorial rules, and no decorative shadows
- **Layout**: A responsive 1210px, 12-column news desk with tight vertical rhythm, compact side rails, and no floating page sheet
- **CSS framework**: Pico CSS with `--pico-*` custom property overrides

The visual hierarchy takes cues from established financial newspapers while retaining original branding, content, a light-grey palette, and original component treatment.

## Demo

The package includes `Database\Seeders\NewsDemo`, an English-language business newspaper named **The Ledger**:

```bash
php artisan cms:demo --theme=news --tenant=news
```

It creates Companies, Markets, Real Estate, and Work & Careers desks with original articles, an editorial page, subscription options, shared footer navigation, accessible media descriptions, and search metadata.

## Page Types

| Type | Description |
|------|-------------|
| `page` | Front page, publication, and subscription pages |
| `docs` | Long-form dossiers with sidebar navigation |
| `blog` | News desks and individual articles |

## Customization

| Property | Default | Description |
|----------|---------|-------------|
| `--news-accent` | `#9E2F50` | Kicker, date, and ranking accent |
| `--news-header` | `#262A33` | Utility header, subscription control, and footer |
| `--pico-color` | `#33302E` | Body and headline ink |
| `--pico-background-color` | `#F8FBFF` | Continuous cool-grey newsprint |
| `--pico-primary` | `#2E6E9E` | Standard links and interactive states |
| `--pico-secondary` | `#262A33` | Utility bars and dark controls |
| `--pico-border-radius` | `0` | Sharp editorial geometry |

## License

MIT
