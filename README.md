# Rota Wrapped

A dashboard for Samaritans branches that use Three Rings. It shows rota cover, listening contribution and shift leader cover, drawn from a branch's own Three Rings reports.

Not an official Samaritans or Three Rings product.

## How it works

This repository holds code only. It contains no branch or volunteer data, and the website never receives any.

1. A rota manager fills in the set-up form on the website once, which produces a set-up link. The branch's settings travel in the part of the link after `#`, which browsers never send to a web server.
2. People open the set-up link and drag the **Rota Wrapped** button onto their bookmarks bar.
3. While logged in to Three Rings, they click the button. It runs inside Three Rings using their own login, so each person only sees what their Three Rings permissions allow. It fetches the reports, opens the dashboard in a new tab and passes the data straight to it.
4. The dashboard draws the figures in that tab. Nothing is stored or uploaded, and the data is gone when the tab is closed. The dashboard only accepts data sent from `https://www.3r.org.uk`.

If the dashboard tab can't receive the data, the button offers it as a single file, which can be dropped into the dashboard by hand.

## Three Rings

The button follows the Three Rings guidance for bookmarklets: it uses the person's own session and makes fewer than ten requests per click, well within the limit of 30 a minute.

## Fonts and logo

The Samaritans Varah font is licensed for Samaritans use and is not included here. Branches can upload it to their own Three Rings Files, visible to volunteers only, and the button will fetch it with the user's login. Otherwise the dashboard uses Calibri, as the Samaritans brand guide allows.

## Files

- `index.html`: the set-up form and install instructions
- `dashboard.html`: the dashboard
