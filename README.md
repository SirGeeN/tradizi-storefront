# TRADIZI Storefront

Web presence for the TRADIZI Android app — powers `tradizi.com`.

## Structure

```
├── CNAME                      ← Custom domain (tradizi.com)
├── index.html                 ← TRADIZI homepage
├── shop/
│   └── index.html             ← Storefront redirect page
└── .well-known/
    └── assetlinks.json        ← Android App Links verification
```

## How It Works

When a trader shares `https://tradizi.com/shop/{ownerId}`:

- **TRADIZI installed** → Android intercepts → opens trader's storefront in app
- **TRADIZI not installed** → Browser opens → fetches Play Store URL from Supabase → redirects customer to download

## Play Store URL

Controlled from Supabase `app_config` table — key `app_store_url`.  
Change it anytime without touching this repo.

## Hosted on GitHub Pages

Domain: `tradizi.com`
