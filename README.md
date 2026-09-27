# notice-book

Offline desk for a community association manager.

Log notices, file papers, put sittings on the wall, keep the yard crews honest, and print the monthly board packet. One HTML file. No account. No server.

Open `index.html` in a browser. That is the whole install.

## What it keeps

- **Notices** — unit, association, what happened, where it sits (open → letter out → cured → upstairs)
- **Papers** — governing docs, minutes, contracts, whatever else lives in the drawer
- **Sittings** — board / annual / committee dates, agenda, carry-overs
- **Yard help** — who does the work, when the contract dies, when the insurance dies
- **Board packet** — counts and lists pulled from the book, filtered by association, print-ready

## How the data lives

Everything stays in this browser on this machine (`localStorage`, key `notice_book_v1`).

That is the point. It also means:

- Switching browsers starts a new empty book
- Clearing site data wipes the book
- **Take a copy off the machine** before you do either of those

The copy is a JSON file. **Bring a copy back** restores it.

## Run it

Double-click `index.html`.

Or from a terminal:

```bash
python -m http.server 8080
Then open http://localhost:8080.
GitHub Pages
Settings → Pages → Deploy from branch main → / (root).
If the file is named index.html, the live page is:
https://<you>.github.io/notice-book/
Download the raw file from the repo and it still runs offline. Pages is just a convenience URL.
Packet
Open Board packet, pick an association or leave it on every association, hit Print the packet. The browser’s print dialog can save a PDF.
The packet shows:

Notices still open
Notices marked cured
Sittings on or after today
Crew insurance dying inside 90 days
The last ten papers filed

What this is not

Not accounting software
Not a replacement for the official association records
Not synced across phones unless you move the JSON yourself
Not legal advice and not a Florida statute engine

Walk the property. Keep the official minutes where the association already keeps them. This book is the working copy.
License
Use it. Fork it. Put it on a manager’s laptop. Keep a backup.
textName the HTML file **`index.html`** so Pages serves it at the repo root. Same two-file layout as C
