# dailyfindings.site

Central GitHub Pages repo serving all landers under `dailyfindings.site/<slug>/`.

Replaces the prior subdomain-per-lander model (`fb49.dailyfindings.site/`, etc.).
Legacy subdomain landers continue to live on the wildcard CNAME pointing at
`nataadsua-maker.github.io` and are NOT migrated here.

## Layout

```
/                      → index.html (homepage stub)
/privacy.html          → shared privacy page
/terms.html            → shared terms page
/<lander-slug>/        → individual lander (deployed by integrations/landers/deploy.py)
  index.html
  (assets in same folder)
```

## Deployment

Auto-deployed by the landers bot. Don't commit landers manually — the bot
clones this repo, drops files into `<slug>/`, commits, pushes.
