# Tomex Gourmet karácsonyi hírlevelek 2026

A Tomex Gourmet 2026-os karácsonyi hírlevél-kampányának előnézeti galériája. Készítette: DOUPLA Creative & Digital, 2026. november. A szövegírói javításokat (2026. november 6.) tartalmazza.

## Mi van benne

```
index.html        a galéria: szegmensek, A/B változatok, asztali és mobil nézet
emails/           a 15 levél mintaadattal kitöltve (kitalált címzett és értékesítő)
emails/images/    a levelek összes képe
export/           ugyanaz a 15 levél éles, EmailOctopus-mezőkkel ({{FirstName}}, {{SalesName}} …)
doupla-logo.png   a galéria fejlécének logója
```

A levelek csoportjai és kiküldése:

| Csoport | Levelek | Kiküldés |
|---|---|---|
| A · Szegmenslevelek | meleg-a/b/c, langyos-a/b/c, sosem-a/b/c | november 10., kedd 9:00 |
| B · Automatikus | welcome | feliratkozás után azonnal |
| C · Kampánylevelek | tortenet, mikulas | november 17. és 24. |
| D · Gourmet vs Office sorozat | sztori-1/2/3 | november 24., december 1. és 8. |

## Közzététel GitHub Pages-en

1. Töltsd fel a mappa tartalmát egy repó gyökerébe, úgy, hogy az `index.html` a gyökérben legyen.
2. A repóban: **Settings → Pages → Build and deployment → Deploy from a branch**, ág: `main`, mappa: `/ (root)`.
3. Pár perc múlva elérhető: `https://<felhasználó>.github.io/<repó>/`

A `.nojekyll` fájl kikapcsolja a Jekyll-feldolgozást, hogy minden fájl változtatás nélkül menjen ki.

Nyilvános repóból a galéria bárki számára látható. Privát repóból GitHub Pages-t csak fizetős GitHub-csomaggal lehet közzétenni.

Helyben, szerver nélkül is megnyitható, de a böngészők egy része a `file://` alatt nem engedi az előnézet magasságának automatikus igazítását. Ilyenkor: `python3 -m http.server` a mappában, aztán `http://localhost:8000`.

## Az éles levelek képei

Az `export/` levelei relatív úttal hivatkoznak a képekre (`../emails/images/…`). EmailOctopusba másolás előtt ezeket nyilvános, abszolút URL-re kell cserélni. Ha a galéria GitHub Pages-en fut, a képek onnan is kiszolgálhatók:

```
../emails/images/  →  https://<felhasználó>.github.io/<repó>/emails/images/
```

A `{{LastPkgImg}}` és `{{UpPkgImg}}` mezők a meleg-a és meleg-c levélben címzettenként töltődnek, ezek értéke is ilyen abszolút URL legyen.
