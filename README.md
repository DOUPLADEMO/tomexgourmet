# Tomex Gourmet karácsonyi hírlevelek 2026

Jelszóval védett előnézeti galéria a Tomex Gourmet 2026-os karácsonyi hírlevél-kampányához. Készítette: DOUPLA Creative & Digital, 2026. november. A szövegírói javításokat (2026. november 6.) tartalmazza.

## Mi van benne

```
index.html        belépő oldal; a galéria és mind a 15 levél titkosítva van benne
emails/images/    a levelek képei (nyilvánosak, az EmailOctopus-levelek innen töltik be őket)
doupla-logo.png   a fejléc logója
.nojekyll         kikapcsolja a GitHub Pages Jekyll-feldolgozását
```

## A jelszóvédelem

A galéria és a levelek szövege AES-256-GCM titkosítással van az `index.html`-ben. A kulcs a jelszóból származik (PBKDF2-SHA256, 310 000 kör), és a böngésző oldja fel. A jelszó egyik fájlban sincs benne, és nyílt levélszöveg sincs a repóban, így nyilvános repóból is csak jelszóval olvasható a tartalom.

A jelszót külön csatornán add át, ne írd be a repóba, issue-ba vagy commit-üzenetbe.

A képek szándékosan nyilvánosak: az e-mailek csak nyilvános URL-ről tudják betölteni őket.

Belépés után a böngésző a lap bezárásáig megjegyzi a jelszót, újratöltéskor nem kéri újra.

## Közzététel GitHub Pages-en

1. Töltsd fel a mappa tartalmát egy repó gyökerébe, úgy, hogy az `index.html` a gyökérben legyen.
2. A repóban: **Settings → Pages → Build and deployment → Deploy from a branch**, ág: `main`, mappa: `/ (root)`.
3. Pár perc múlva elérhető: `https://<felhasználó>.github.io/<repó>/`

A képek címe ezután: `https://<felhasználó>.github.io/<repó>/emails/images/`. Az EmailOctopus-csomagok erre a címre hivatkoznak.

## Módosítás

A tartalom titkosítva van, ezért közvetlenül nem szerkeszthető. Szövegváltozásnál a galériát újra kell generálni és titkosítani, és az új `index.html` felülírja a régit.
