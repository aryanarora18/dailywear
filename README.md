# DailyWear

**[dailywear.nyc](https://dailywear.nyc)** answers one question before you get dressed: what is New York actually wearing right now?

We glance at the city's public street cameras, count outfits (never faces), and fuse that with the official forecast. The result is a morning verdict like "It's a hoodie kind of day," a plan for the whole day, and the receipts: real camera frames with every pedestrian boxed and labeled.

## What's in here

A single self-contained page (`index.html`) served by GitHub Pages on the custom domain:

- Home view: greeting, verdict, forecast disagreement line, day plan, one-line signup for the 7:40am morning note
- Today view: official forecast tile, advisories (humidity, wind, subway platform heat), what everyone's wearing in plain language, your day at a glance, camera photos with live detection boxes, feedback box
- `sw.js` and `manifest.json`: installable PWA with web push (the morning note)
- `icon-*.png`: the dw monogram

Data comes from the backend at [aryanarora18/dailywear-backend](https://github.com/aryanarora18/dailywear-backend) via one JSON call. If the API is unreachable the page falls back to its static content instead of breaking.

## Privacy

No account. No email. No name. Notifications store one thing: the device's anonymous delivery address, deleted when notifications are turned off. Camera analysis counts outfits in aggregate; individuals are never identifiable at traffic-camera resolution.

## Deploy

Push to `main`. GitHub Pages serves it on dailywear.nyc with HTTPS enforced.
