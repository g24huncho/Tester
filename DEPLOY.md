# Going fully official — dpcoaching.uk

Everything technical is already done: the public site lives in `docs/` and is
pre-configured for **dpcoaching.uk** (the `docs/CNAME` file). Two things need
Gbolahan's card and login — about 10 minutes total.

## Part 1 — Buy the domain (~£10/year, 3 min)

1. Go to **namecheap.com** (or any registrar).
2. Search **dpcoaching.uk** → availability confirmed against the Nominet registry on 19 Jul 2026; dpcoaching.co.uk and diversepaths.co.uk are taken — backup choice: diversepaths.uk → buy it.
   Skip every add-on they offer (hosting, email, SSL — not needed).

## Part 2 — Switch the site on (2 min)

1. Go to **github.com/g24huncho/Tester → Settings → Pages**.
2. Source: **Deploy from a branch**.
3. Branch: **claude/fable-5-business-tool-ko3y8i** · Folder: **/docs** → Save.
   (Site is immediately live at https://g24huncho.github.io/Tester/ even before
   the domain connects — bio-ready from this moment.)

## Part 3 — Point the domain at the site (5 min)

In the registrar's DNS settings for dpcoaching.uk, add exactly these records:

| Type  | Host | Value               |
|-------|------|---------------------|
| A     | @    | 185.199.108.153     |
| A     | @    | 185.199.109.153     |
| A     | @    | 185.199.110.153     |
| A     | @    | 185.199.111.153     |
| CNAME | www  | g24huncho.github.io |

(Delete any pre-filled "parking" records first.)

## Part 4 — Tell GitHub the domain (1 min)

Back on **Settings → Pages**: type **dpcoaching.uk** into *Custom domain* →
Save. Wait for the DNS check (can take a few minutes to a few hours), then tick
**Enforce HTTPS**.

Done: **https://dpcoaching.uk** — put it in the Instagram and Facebook bios.

## Notes

- Buy a different domain instead? Change one line in `docs/CNAME` to match and
  use that name in Part 4 — nothing else changes.
- Future site updates: any push that changes `docs/index.html` republishes
  automatically. The build source is `site/index.html` (they are kept in sync).
