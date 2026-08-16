# BEAST+ preview clips

Muted 720p hover-preview WebMs for [BEAST+](https://beast.com.se), served through
the free [jsDelivr](https://www.jsdelivr.com) CDN.

    previews/<ytId>.webm        tile hover previews
    previews/hero/<ytId>.webm   HD hero clips

## Why this repo exists

These were hosted on Vercel Blob until 2026-08-16, when every object began
answering `403 "Your store is blocked"`. All four Blob stores on the account
reported "Limits reached" at the same moment — the Hobby cap is account-level,
not per-store, so adding another store could not have helped.

The binding constraint is **egress**, not storage: every hover on the site
streams a clip. jsDelivr serves public GitHub repos with no bandwidth meter, so
the ceiling is removed rather than moved.

Files are immutable — the filename is the YouTube id and the content never
changes for a given id — so they are safe to cache indefinitely.
