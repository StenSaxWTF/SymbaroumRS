# Symbaroum Rollpersoner

Character manager for the Symbaroum RPG: characters with automatic secondary
attributes and XP, a filterable rules library in Swedish and English, and
sync between devices. Runs as a static site on GitHub Pages with Supabase for
login and storage. The rules texts are **not** in this repository; they live
in the Supabase database and can only be read after signing in.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `config.js` | Supabase project URL and publishable key |
| `vendor/` | Supabase JS client 2.45.4 |
| `sw.js`, `manifest.webmanifest`, `icons/` | Makes the app installable and fast to open |
| `.github/workflows/keepalive.yml` | Pings Supabase every 3 days so the free project isn't paused |

## Adding a player

Supabase → Authentication → Users → **Add user** → **Create new user**.
Enter their email and a password, tick **Auto Confirm User**, then send them
the link and password. They can change the password under Inställningar.

## Updating the app

Replace the changed files in the repository. GitHub Pages republishes within
a minute or two; the app picks up the new version the next time it's opened.
