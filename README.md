# ClinixPro by RYDE Labs: online demo

Static HTML build of ClinixPro: the clinic workspace (appointments, patient records, dental chart,
prescriptions, inventory, billing, reminders, patient portal) and the public "Find a doctor" site.

There is no server. Each visitor's data is saved only in their own browser (localStorage).
"Find a doctor" also looks up real clinics near the chosen place from OpenStreetMap.

## Pages
- `#/welcome`: ClinixPro home (patients and clinics)
- `#/find`: find a doctor on the map
- `#/login`: clinic sign-in (one-click demo accounts, password `demo1234`)
- `#/inventory`: stock room for doctors, front desk and admins (after signing in)

## Publish on GitHub Pages
1. Create a new repository on GitHub (for example `clinixpro`).
2. Upload **everything in this folder** (including the hidden `.nojekyll` file) to the repository root.
3. In the repository, open **Settings → Pages**, set **Source** to *Deploy from a branch*,
   pick branch `main` and folder `/ (root)`, then **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

It also runs from any static web host, or by opening it through a local web server.
