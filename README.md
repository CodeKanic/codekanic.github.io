# codekanic.github.io
Static site for codekanic.com. Plain HTML/CSS, no build step. Edit the .html files directly; replace [placeholders] before launch.

## Buy buttons: swapping in real IDs
Only vendor scripts are used (gumroad.js on Home and Templates). No other JS.

**itch.io (game templates)**
1. Get the project slug from its URL: `codekanic.itch.io/<slug>`.
2. In each `card g`, replace `[game-slug]` in the Buy and Details links. `/purchase` opens itch's buy page.
3. Optional widget: on itch go to the project's Edit page > Distribute > Embed/Widget, copy the numeric ID, and uncomment the `<iframe src="https://itch.io/embed/[GAME_ID]?dark=true">` block. Official format (itch.io/docs/creators/widget): `<iframe src="https://itch.io/embed/ID" width="552" height="167" frameborder="0">`.

**Gumroad (apps, websites, Notion, Sheets)**
1. Gumroad > Widgets > Modal Overlay, choose the product, copy the URL inside the snippet (`https://<user>.gumroad.com/l/<permalink>`).
2. Replace `https://[gumroad-user].gumroad.com/l/[permalink]` in the card. Keep `<script src="https://gumroad.com/js/gumroad.js">` once per page (loading it twice opens double popups).
3. We leave off the `gumroad-button` class so the pixel style applies (Gumroad documents this as "custom buttons"). Add `?wanted=true` to the URL to skip straight to checkout.

Replace every `[price]` too. Search the repo for `[` to find all placeholders.
