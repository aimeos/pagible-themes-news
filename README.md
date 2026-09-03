# News Theme

A newspaper theme for [Pagible CMS](https://pagible.com), designed for daily reporting, business desks, and editorial publications.

This package is part of the [Pagible CMS monorepo](https://github.com/aimeos/pagible).

## Installation

```bash
composer require aimeos/pagible-themes-news
php artisan vendor:publish --tag=cms-theme
```

## Design

- **Style**: Authoritative, information-dense newspaper layout with a utility band, centered masthead, section rail, lead-story split, and ruled story grids
- **Colors**: Light-grey canvas (`#ECEFF1`), soft newsprint surfaces (`#F8F9FA`), ink (`#172126`), crimson accents (`#A02B33`), and slate-blue utility areas (`#35566A`)
- **Typography**: System serif masthead and headlines with compact sans-serif navigation, dates, metadata, and controls
- **Geometry**: Sharp corners, thin editorial rules, and no decorative shadows
- **Layout**: A responsive 1280px news desk with a larger lead story and compact supporting coverage
- **CSS framework**: Pico CSS with `--pico-*` custom property overrides

The visual hierarchy takes cues from established financial newspapers while retaining original branding, content, colors, and component treatment.

## Demo

The package includes `Database\Seeders\NewsDemo`, an English-language business newspaper named **The Ledger**:

```bash
php artisan cms:demo --theme=news --tenant=news
```

It creates Economy, Money, Property, and Work desks with original articles, an editorial page, subscription options, shared footer navigation, accessible media descriptions, and search metadata.

## Page Types

| Type | Description |
|------|-------------|
| `page` | Front page, publication, and subscription pages |
| `docs` | Long-form dossiers with sidebar navigation |
| `blog` | News desks and individual articles |

## Customization

| Property | Default | Description |
|----------|---------|-------------|
| `--pico-color` | `#172126` | Body and headline ink |
| `--pico-background-color` | `#ECEFF1` | Light-grey page canvas |
| `--pico-primary` | `#A02B33` | Section and action accent |
| `--pico-secondary` | `#35566A` | Utility accent |
| `--pico-border-radius` | `0` | Sharp editorial geometry |

## License

MIT
