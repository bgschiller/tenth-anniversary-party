This html was made in Canva, but I copied it out of the published site. To update:

1. publish site and visit in chrome
2. Save webpage, complete.
3. Copy the HTML from the html file, and the images and js from the \_Files directory that was made alongside it.
4. To get fonts, run

```sh
for ff in $(< index.html grep -Eo '(fonts\/[0-9a-f]+\.woff2)' | sort -u); do
mkdir -p fonts
curl https://morganbrian10anniversary.my.canva.site/$ff > $ff
done
```

5. Delete the `fetch('_footer')` script tag from the bottom of the page.
